# Design of the ASCII Art

**Authors:** *Flosha* & *Avallach*  
**Created:**: 2021-10-01   


**Flosha:** After the creation of the latest design of our [team website](https://phoenixtales.de), in which I decided to discard all images in favour of pure text and ASCII art, I told Avallach that I want to colourise the Phoenix that [I had designed in 2016](https://docs.phoenixthegame.com/appendix/behind-the-scenes/team-branding) and decided to use the newer "stalker" variant I had made in 2021. While the design of [gothicarchive.org](https://gothicarchive.org), [phoenixthegame.com](https://phoenixthegame.com) and our [documentation](/) was developed by me on my own, there are a few technical things that I couldn't manage to do myself. The colouration of the ASCII art is one of them, and I thought that the solution is interesting enough to tell you about.  

I generated the Phoenix ASCII with an online tool, since I couldn't see me doing that by hand. This uncolourised version was looking like this: 

![ASCII Phoenix](/appendix/behind-the-scenes/ascii/phnx-ascii.png)

For everything else I will just quote our conversation. No need to retell what you can read first hand (or first fingertips in that case). I was just finishing the design, showing it to Avallach and asking if he would be able to help me with the colouration.  

> [23.09.] **Flosha:** What do you say now?    
I want to add colour to the Phoenix. It's just quite hard to do.  

> [23.09.] **Avallach:** O wow, I really like it. I really like the ASCII art design of the main page. I can help colouring.  

... he said. And went straight to work. Two days later:  

> [25.09.] **Avallach:** This is harder than I thought. I have an idea how to achieve it, but it will take me a bit more time. / I will need to separate the ASCII art into multiple layers, each for one colour in the palette. So there will be 4-16 &lt;pre&gt; elements overlayed on top of each other with CSS.

> [26.09. 00:37] **Avallach:** It's really hard. This is a prototype with 6 layers, colours are not set yet. But I see that shape somehow got corrupted.  

![Test1-Distorted](/appendix/behind-the-scenes/ascii/test1-distorted.png)

> [26.09. 00:50] **Avallach:** I fixed the shape, but contrast and colours still require some work. / Still 6 layers. Gray + 5 colours. / Do you think this is enough colours or should there be more, like 16?

![Test2-ShapeFix](/appendix/behind-the-scenes/ascii/test2-shapefixed.png)

> [26.09. 12:29] **Avallach:** I'm doing already like the 4th prototype... this time trying to limit colour to areas with some minimum saturation and brightness on the input image:

![Black-White](/appendix/behind-the-scenes/ascii/phnx-bw.png)

> [26.09. 12:35] **Avallach:** Current idea: Pick the optimal colours only for these sections of the image, and leave the rest in greyscale:

![Colour-Choosing](/appendix/behind-the-scenes/ascii/colour-choosing.png)

> [26.09. 13:54] **Avallach:** I need gimp to calculate optimal colours. / But it is already on the same grid. / 98x95 /  As the ASCII will be. / So that the calculations for each character are exact. This is around 10 colours and IMO looks close enough.

![Colour-Choosing-2](/appendix/behind-the-scenes/ascii/colour-choosing-2.png)

> [26.09. 14:02] **Avallach:** All the brightness and sharpness will be handled by the ASCII art generator. This is just a template how to separate colours into layers. All the brightness information from here will be ignored.

![Step-1-Color-Mask-&-Step-2-Color-Map](/appendix/behind-the-scenes/ascii/step-1-and-2.png)
![Step-3-Seperate-Colours-WiP](/appendix/behind-the-scenes/ascii/step-3-separate-colors-wip.png)

> [26.09. 15:07] **Avallach:** This is the result of the separation:  

![Layers-Gif](/appendix/behind-the-scenes/ascii/layers.gif)

> **Avallach:** Now I will prepare the ASCII-art [again, via the online generator I (flosha) used] from each of these colour layers. / I think only this screenshot really explains how it works, right?

![Layers](/appendix/behind-the-scenes/ascii/thelayers.png)

Upon my request, Avallach has written a little documentation, that really shows the complicated process he came up with just to fullfill my wish to colourise the Phoenix:  

<hr>


## How Phoenix Tales colours ASCII arts

by Avallach  

Just like with making a mod for the zEngine, it's a tedious and manual process involving multiple tools. Could be made way easier if we were ok with cheating and making a bitmap picture where characters are represented as pixels. But no, we want a real old-school ascii art that is both retro and lightweight.  

We used a third party tool that can convert a grayscale image into ascii art. It does not matter which tool it is, the approach works with any.  

We came up with this exact procedure when preparing a coloured ascii art of the Phoenix in the "Stalker" variant. We tried out a few different approaches, and the below sequence of steps gave the best results.  


### Step 1 - prepare colour mask

1. Duplicate the input image into new layer "1"
2. Create new layer "2" filled with 50% saturated red (HSV)
3. Put "1" above "2" and set colour mixing mode to HSV saturation
4. Merge layers "1" and "2" into "2"
5. Desaturate and invert layer "2"
6. Duplicate the input image into new layer "3"
7. Desaturate layer "3"
8. Increase contrast of layer "3" to maximum and set brightness to the point when parts too dark to be coloured are all black
9. Put layer "3" above layer "2" and set colour mixing mode to "Darken only"
8. Increase contrast of layer "2" to maximum and set brightness to the point when only parts with visible colour are white
9. Merge layers "3" and "2" into "2"
10. Scale layer "2" to the size of target ASCII art in characters (e.g. 98px x 95px for Phoenix mascot) (proportions will appear stretched horizontally, because each character in rendered ascii art is naturally taller than wide)
11. Replace white with transparency
12. The layer "2" is now our "colour mask" that we will use in the next step


### Step 2 - prepare colour map

1. Slightly increase saturation of input image to compensate for coming partial colour loss
2. Scale input image to the size of target ASCII art in characters
3. Put "colour mask" prepared in step 1 above input image and merge it into it
4. Make sure that there is only one layer left in the image and no transparency
5. Change image mode to indexed, around 10 colours, with Floyd-Steinberg dithering
6. Replace black with transparency
7. The colour map is ready - we will use it for distributing available colours between "ascii pixels" (it will only affect hue/saturation, not brightness as expressed by choice of different ascii characters)


### Step 3 - separate layers on input image

1. Put colour map prepared in step 2 on top of input image
2. Use tool "select by colour" `shift-o` all the time, with 0% tolerance setting and no antialiasing
3. Scale colour map to image size, with no interpolation (it will look "pixelated")
4. Select black colour on colour map and remove it
5. Select any colour on colour map, delete that selection on colour map, then cut that selection from input image and paste it as new layer
6. Repeat step 5 until colour map is completely empty
7. Save each layer created in repeats of step 5 as separate file
8. Generate separate ascii art from each of these files, using a 3rd party tool of your choice
9. Generate last ASCII art from parts of input image that were not covered by colour map


### Step 4 - assemble with CSS

1. Display each ASCII art in separate divs
2. Position the divs absolutely on the same position, so that they perfectly overlap
3. Pick different colour for each ASCII art, except of the last one, which contains "grayscale" part
4. Carefully tweak the colours in CSS so that overall the art has the best reassemblance to the input image

---


Here our final colourised Phoenix:

<img class="phoenix-ascii" src="/appendix/behind-the-scenes/ascii/phoenix-ascii.svg" style="width: 481px; margin-right: -40px; cursor: normal; -webkit-user-drag: none">

And for your imagination: These are all the signs of the 12 layers if we do not let them overlap and do not put them in a `<pre>` tag:  

<div class="chaos-ascii">
<div style="color: #4c4c4c">                                                                                                  
                                                                                         ':!:'  
                                                                                       !v:;||s/'
                                                                                  ` ,\p).    lW:
                                         `.',~!))*r|?|/vs{C((vl|^:'`        ``.,,S)^!, `',   |W.
                                  ,!//  X"              |jCvlr!.oSdOa(svx(//?r'  ``   `.''   ^j 
                               ':  ```                  '>|!:`    :uEu|^l^`           `      \r 
                             , )                          ',::'   `:``...:?                `/|  
                           '   :e                            `,L   `',!vu'   ''`          !6;   
                         `*,`dQ                            ,,?R'   .'       ' `.````    '4u'    
                        `|'(E|   '.'''.'',. ``              rK!  ,`',,'    `' ..      ;o6r      
                       '|`` '* ,,::`       ',.'            '$: ','.''''.    ```    ,vOD/.       
                    `:v`   ,   ::.           ~,'       `   ",`,.,:''.``         '\ax!`          
                 .;/ev EHW'    !``           .!'           . ."! ,'`          ^aO7,             
               'zu           ``,`,           :,.     `    `  *vLL,         .lXa*`               
              ,dQQy 'y  s`  :  .,`,       ,|;',   !     `"  `|z(?`       '>jL,                  
             ;gd`:Bu,@g' q@, !   '``:r   r|,.'      `;`C'  `' `'`     `;z|`                     
            :E:ge'B8C `y. `($Oe`   ``````.,      `v   `'`.``'`      ,r?;.                       
           .S@:#QQOu6SQ#^.*vCvr>|!`,,,,                   ```    ,::.                           
           '?!,.:,!!!>jL?Cxzzv77vC/,          !      `,,`      `:'                              
               Cj?,?(rwL7jjs|?*r^rr, `   ``   `   '   ',     ``                                 
                ,:^,.'C6eC^,.  `  `',` ``     ,`  `` ```    ``                                  
              '::'.` /upu,`                        `` `.`                                       
              `,",.` `/js,              ```....`` ``' ^!'`                                      
         `''!  ```     !*,             ``...:!!`  :  `L:.  .`                                   
        `,:    ''        ',::`         `   ` :`'  .,        .                                   
        '!     '`           ``         ````  ,:`: `       `"```.`                               
        '.     '.          ,      ````` `''``':,':'    r;  :r'``.                               
          ,`  `'`                  ``.```.  `','       ,^,,,````'                               
           ,/.                      ````.'     `            `. ```                              
           `?\                       ` `.    '               ~:'``                              
          *a'      ,*"```       `    ```r      `  .`             ``                             
         `:!rs/Qg' ;D#Xr`  `     '`    `       ,       !          `                             
        .. `,``e@E` C6S!`         .````', `            !,   '     .                             
       ,`|jvvL,.)4: ,!'     `     ```         ,          `   '' `,.                             
          :^)s(L.:/,                `` '      : "         *.    ````                            
              `jw>?r`        `   ``.`.'''     ~ '        `*\     `                              
          (d.  `rHEo/'        `.``''`.'"      ' ,,           l`   `                             
          SB?`  ,|yaSo:       '`.'>;'..!         '                '`                            
          O! .  `">lHge!`     "`  :?:' ^`        `            j%r. `                            
          ^'v;'   ':?(O$>`     l```'```   `' ,   ,,,    !     ywzL:`                            
           jO"`    `''?aj|:    O'` ,` .'`',  .,,:!!,          aC   `                            
             ,      `` .:>|'   H:','.'"'.','',''`r^!:!,     u`  : '                             
            j'    `      `,"`  p,   :::~  ,!!!:`                C?                              
           d#.  ` `       `.`  a.   ::,,`'!                     \ '.                            
        `  (',   ,~,`          j,   ,~:.`,?  :               ^`   ,``                           
                  .,           z! ` ',~   ~  :                    :``                           
            q`  '` ``          vr   .'",:'`  .                    !``                           
            E,  '   `. !` `,`  C?   ','.'"  `                     ,`.`                          
           /@: ` .  :     ::`` ?;      `',                       .` .                           
            $` ``.           ` `, .`    `'         :`,          '"'                             
           \l  ``,         `   `.   ",.```          .`          , '``                           
           u. `'':           `  ,'   "'      `                     `                            
           7,  ` :,       ~?'.` ;!   '`      ``     ``         .',`                             
           C,  `,  `        `,` "u:`. `     `.'      .`   `.` `  `                              
           k,          .    `!` `|:``        ..       `       `   `                             
           x                ``   ':  ``      `         ` `.       .                            `
                        `    `.  `"           `          ```   `  ``    `                       
                ```     `     `   .                       ``      `    ```                      
           '    `  ` `          `                                 `    ```                      
                 `'            `                                       ``                       
       `        ``'```         `                `      '.``          `.``                       
       `       `'``   `      ''  ;,                    ..`````      ````                        
      `    .   .'``     `|`  '. `|       `.      `     ``  ````..``````                         
      ```  `   !:. `` .!.,    ` ^  `  ' .  '      `            `.````                           
      .`  )! `.,;r.``':, ":,` `!?`     .            `        ````        `   `.                 
      ``  y, ,::,`*!~:^:'''``'^:    ``            ``   `      ``        ``'''                   
      ``   ' ,:!!' ' ..` ',`.'`    `              `     `     ``   ``` `'~::.                   
             ,:;!!::~:,'`         `     :' `:     .`        ```.``'.````.,!~`                   
            ,!!;!!!:!!:,.``       ````  ?Lr~``.` `   `        ````.```,~:;``` .'.`              
        `   ;>r?!~` :^!:"''..``   `.    ^r**>:` '!r:'```   ````''```.,:;,;|;:!r*'``             
     `` `  ,^?r/'    rr:::,",` `  ``   ^|`^!,'`   ```.::,',.'``,,,.,::' '^/r;>:,.,              
      . ` ,*!"!,    ~r:,^!:'`   .``   ^|)vl:'`` ` `  `','''"~ '!''  `:"  '!^::.`^r              
    . ` ```.  :`     :!Lsl,     ".`    ro)/:'`.`  ```  :!: `! '         '  .''.`>:              
     .  ``   `,      :zu.       ::'     >l/^:,,   .. ''rl^            ,?`  `'   >`              
        `     .      '|!?       :;:     :x)|??!     ^r*zv`            `:,:      ?`              
     `. '              '*`       Lu,     "CzLLv      .77l    .z` :       ` ``    :,             
      '. ``            .:        ru!     ` |zz|.     sj7/     vj|:      `'`       ,.            
      ,'`'`             `         ):        :r :      `v^     '>C:        '~!'     :'           
      ``    `     ``     ,`       '            ,       ?'`    ` :           '.                  
                         '`      `         `.'         '        ,^                   .          
                ,`             ,.         `````        `         *                   `          
         `,          `                     ``.                   `     ```           `          
          ,'      '     `               ````'     '      .                          `           
               `..``   'r    .'        ```          `.`  ``   `           :`  `                 
            .  ,.    '"  .   :*!.',. `  ```,',''.`  ``   `   `       ;   .``                    
             ''    `''`         `*!,`.'''    ` `",.`` `,   `             `                      
        `         ``  `            .          ``..`  ':           .,                            
       .,'`      `   `'`       `           ``````                ."  `                          
                 `    ``                    `` `                ';                              
                `.       :  `              ,`                   !  .,,                          
                 ``      `                                             .'.`                     
                  `    `                                     '.                                 
                                        `         `          `'.                                
                               `       .          ``                                            

</div>

<div style="color: #736d5d">                                                                                                                                                                   
                                                                                                
                                                                                                
                                     ;qE^TGqn: *     -*                                         
                                :VXNNOgOggOrn_x    :l .                                         
                               ;mHOPGN@&KWOd^a^ _v  .           _a                              
                             *O.f@BE+3;y=YrY~V/  `              .-                              
                          'eg~ ~T~           sC `                                               
                         `I-                   :z`                                              
                       .-n;                     ,z`                                             
                       eEmE_                     _e                                             
                     _Zr:;G;      'x              `                                             
                 /$PgOOO$/qG,     'l=:ar.        ,1                                             
                 .!Oq_-Y*.'Z~     ;0c ..          `                                             
               ~pe.:'  TO^ qO~     ':_wVC_        :v    oC'                                     
              e.lU  ~GXrCC_':                  :3e~n:f  -_                                      
              b                     `. . .v_e:)  _1_)                                           
             '`                    'yx s-x_v:                                                   
            .YZ                                                                                 
           zMX_                                                                                 
          bMIe:                                                                                 
          la:.                                                                                  
          ..                                                                                    
                                                                                                
                                                                                                
           `                                                                                    
           s_                                                                                   
                                                                                                
                                                                                                
             C^                                                                                 
             '.                                                                                 
                                                                                                
                                                                                                
                                           s,        `     a;.                                  
                                                    ;e       I_                                 
                                                              )-                                
                                                          z:                                    
           n_                                             `                                     
           0/                                                                                   
           '                                                                                    
           u~                                                                                   
           P|                                                                                   
            '                                                   /z                              
            n_                                                                                  
           'w~                                                                                  
           C^                                                                                   
           q=                                                                                   
           '.                                                                                   
           n~                                                                                   
           `                                                                                    
          `                                                                                     
          4~                                                                                    
         .,              .                                                                      
         xZ~             y_                                                                     
                         3:                                                                     
          X^             '                                                                      
          's`                     'y                                                            
          b~                      .Te                                                           
          X~             e,        .^c                                                          
          _.             .                                                                      
          R^             c'                                                                     
          q/                                                                                    
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                   .                  `                                                         
                  _f                 _C-                                                        
                  _o     =.   n      ;X_                    )'   ^C                             
                   `     .    `       ,.                    *.   *q                             
                               o                           ok  z rV           vC                
                   `r          `                           `u' ` ~C           .'                
                               .                                 ;3                             
                               s                                                                
                                                                   .                            
                                                                  _e                                                                                    
</div>
<div style="color: #453a2b">                                                                                                                                                                                      
                                                                                                
                                             bO~NKOKU                                           
                                             ':$_/vKcDBU_                                       
                              n             mr &E~ODgg)K_                                       
                              _             _.XcOb_/*Y~E,                qOC                    
                              _            s,  X~4dgb;dq/             ~O$8/                     
                              d                z `'^Y   y/                                      
                            '.       . )_l,      1b/3                                           
                            8~      ~4 3_       :C                                              
                           e;    .) `/ 'o~o~     =U                                             
                           `     rg     4~'     _n,                                             
                                 ._    =/       .,/n                                            
                                                _Xp.                                            
                                            vY;4 __|3:*                                         
                                      :e|8v._&r&Cp=XrKx                                         
                                     =&^4_X^4b_3_1                                              
              .;                                                                                
              nb                                                                                
              '.                                                                                
            =a,               b3                                                                
            `.                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                         '      .                                               
                                         V;    _x                                               
                                         '      .       3~ v_ C;                                
                                              n         '  `  ,                                 
                                             3!                 z                               
                                        s:ng~C/y_1    /D^  v:   .                               
        d|..                                 C/y_z            nn'                               
          ny,                                ,.         `       a`                              
                                             V/         y~      _e                              
                                                                                                
                                               ;x                                               
                                                .                                               
                                                                                                
                                                                                                
          nr                                                                                    
                                  :v                                                            
          _.                                                                                    
          gl                                                                                    
                                                                                                
         n^                                                                                     
         gr                                                                                     
         V|        ~n     y/   c                                                                
         gl         `     n^     ,s                                                             
         8l                                                                                     
        .Y!           .   ,                                                                     
        Y^           .d|  g/          `                         .                               
        Cv.           Xc  a'         _o,                     `  s                               
         Rl          .Xx                                     ),                                 
        e!.           :; 4'       ^ga                        .  c                               
        `Ur           v_ qC:x_    .1Enb/                        `                               
        z|.              gg..      `1d,.                                                        
        .            :C  ,xKH_      .'                                                          
         _.            4:qbOd/                                                                  
         E=            n.  y/                                                                   
         '.            o. .`'                '        `                                         
         d*               dgK~               y_      ,1                                         
         '.               ':'             nUd8/                                                 
                                          ::dg/           z_                                    
                                            YOY           z_                                    
                                            '$O           .                                     
                                             '_                                                 
                                       Y^                                                       
                                                                                                
                                                                     .,'                        
                                                                     ~XD~                       
                        E|                                     ov     '_VEV'                    
                        _.         'r  y,                     dE.       '_b_                    
                                    .  ,.           ~U        __          ,                     
                                          d!         '                                          
                                          .p~        ~E                                         
                                          )_                                                    
                                                                                                
                                                                                                
                                                                                                
                          a;v:                                                                  
                          . .                                       :z     3_                   
                                                                     `     'n_                  
                               y         1_3;                  c  :)        'y8_                
          z_  x'       ''               x_          .    .       ')                             
               z       qU^'      ''                |3    p~     .                               
                        pEV_  '^Cd)     v^'      _lb     4*.   .y     `                         
                          a:  y3         dR^   :gMC      3$~   q     ;n                         
                               .         `nbp/ _Xo       .' x_ a      `                         
                          l,              .`` 3             .                                   
                                          y_  .:bx                                              
                                          .     .                                               
</div>
<div style="color: #855d5b">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                           C;u/ :4z                                             
                                           , '3  `'  :1                                         
                                   _x_n_y~T/k~`s      .                                         
                                               /V`                                              
                                                /u                                              
                                                                                                
                                                                                                
                                                                                                
                         d/                                                                     
                     ^K/ :Y^                                                                    
                     ._   ,.                                                                    
                                                                                                
                                                                                                
            `                                   .                                               
            y^                                  r                                               
                                                                                                
            u_                                                                                  
            ,                                                                                   
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                         `,        ;o ,T;   ,.                                  
                                         nZ;'      ,. '     C^                                  
                                          V~v:    ,wf_3       ,'                                
                                          9;                  Xm                                
                                        a_`              n~nK~:_                                
                                        .                y_eK=                                  
                                                         . `9Kr                                 
            4;                                             nc_.                                 
            '                                              nR^9^                                
          n=                                         ^w    d; n_,                               
          Cl                                      :'      'o:   Y                               
          `U~                                    |$C.,   'f:   .                                
          y/                                    ;n/n/C   C/    a                                
          `                                      ' ` `'y;9^    `                                
          v:                                   _wy;e   `.Y~                                     
          `                                     '` `     '   o_                                 
          o_                                                 `                                  
          3/                                                                                    
         `_                                                                                     
         aQ^                                                                                    
          ,.                                                                                    
          Or                                                                                    
         s=E/                                                                                   
         `Qs.                                                                                   
         sr.                                                                                    
         `                                                                                      
         *M^                                                                                    
         .                                                                                      
         r=.                                                                                    
          N~                                                                                    
          `                                                                                     
                                                                                                
</div>
<div style="color: #453639">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                    /V;X~      v                                
                                               :e    ` '       .                                
                                               .,       zn:                                     
                            *:                   /9nf_o a/                                      
                                  ./               `.`   .                c'                    
                              '                   `v~h.  v'                                     
                              C                     :y)  .                                      
                              )                          v'                                     
                            f;.          y:     'z|e     .                                      
                                         :.      '..                                            
                                               'nu                                              
                                                ''                                              
                                              v                                                 
                                        y_ y^    ._                                             
                                    .            ;f                                             
                                   :)                                                           
                                                                                                
                   't                                                                           
                    .                                                                           
                                                :f                                              
                                                /C                                              
                                               l                                                
                                                 . . ..                                         
                                                ,s;e:3) '                                       
                                                     .' f'                                      
                                                     /C                                         
               _l                         v; v:    `*.~b_   e:                                  
               .`                         . )~      .  ,    a:                                  
                                           vE/   :e      vE~.  e                                
                                           'h;    .     *:E~   .                                
                                         y^ u!   ,8d~Od  *_ Xq:`                                
                                        `_., u;  'l .sO    :_. C`                               
                                        yn:q|     ._!e.':z'CRv.uy                               
                                        TQ=)C_    :MQ=^dX^ z;9r                                 
            =.                          :OW|'):    :~Tqd=. _.$|                                 
            .                           |f~  .vz   ;p8CX~ u~ ;.                                 
          bt                             .    .`   _y;CE/C=$t   pVa                             
          '.                                   :e   . =O~e:_'btCrq`                             
             c.                                _p9hVv ~$;=Or O|d.,                              
                                           drT!_pn^Ts._ `l, U=:h                                
                                           ud_e:9C ~v,l c_ ,T~V9:                               
                                           'b/  :n .::*^v;,br.z3q                               
                                           *T_ .r  ~p     VdX~                                  
                                          *:.  s,^NXT     'n=e: ;e                              
                       s,                 `v:  = .:td3nT~  r_'vo..                              
                                           .       ..|bC_ !.  '`                                
                                                      ~uC/      _e                              
            ~              )`                             =_ `                                  
                                                             f:                                 
                   .                                                                            
                  :z                                                                            
                                                                                                
                      s_                                                                        
                      '.                                                                        
                                                                                                
                                                                                                
                             u_                                                                 
                            `    .,                                                             
                            z^  .fV                                                             
                             o: c8                                                              
         v_                  .   .                                                              
         `.                                                                                     
         *p:                                                                                    
         z^~                                                                                    
         `v'                                                                                    
         'u:                                                                                    
         aq:                                                                                    
                                                                                                
                                                                                                
                               r                                                                
                               .                                                                
                                                                                                
                                                                                                
                                '~                                                              
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                           l,                                        `*    o:                   
                           .                                          `    ,                    
                            t,                                     ,e                           
                            .  _a           s'                     ;o                           
                                 :v  '):                         .              v               
                                  ,s                      .     'v                              
                                                 ,)       o_                                    
                             v_                            y,                                   
                             .                             `                                    
                                               l                                                
                                               .                                                
                                                                                                
</div>
<div style="color: #1f724f">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                   =MBmO/                                                       
                                   .sP~;                                                        
                                     .                                                          
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
             z_                                                                                 
           v4d3                                                                                 
            -.                                                                                  
            x_                                                                                  
            f~,   . .  ` `'                                                                     
             aX' :o`f` 1:3G\.                                                                   
               d ^9'T1   n9:x_                                                                  
              Y''v` '.   .` .*-                                                                 
              :              `.=                                                                
                               .                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                            .z:     :a                                                          
               `zuVn       vu9p     .~q~                                                        
               .)4EmV      fCqX      _Y~                                                        
                .;3nlq     sC9PY     _nV$_      ,ne       rb~                                   
                    _gb`    *nTPO    -eTOg'     `apC.     .aN=                                  
                             1;^q      zwq_     `aCp3.    cnpg^    .'                           
                                                -an4pu     xbY$:   /b`                          
                                                 :ynq4`   `oC/$|    :v                          
                                                   /U8o   eb_xC\                                
                                                    `,`   .` r_3                                
                                                               .                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
</div>
<div style="color: #124a3c">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                   :C                                                           
                                   .;                                                           
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
              j                                                                                 
              ,                                                                                 
           ek^                                                                                  
             r.           ..                                                                    
                    ...^)'t_                                                                    
               ._'  ~e*=.  .rv`                                                                 
               rgn     C:  j;  t                                                                
               .'!e    .   .. e'                             e;                                 
                            ^vy                              ,.                                 
                             ror^              _)                                               
                              fCa!              . ,n                                            
                            . )v*^                 .-                                           
                            !'=                    _w                                           
                                                                                                
       *_                                                                                       
       ^.                                     o           Z~                                    
                                              .           :.                                    
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                   '+'*'                                                        
                                    . .e~                                                       
                                    .    '                                                      
                .'`                '+.   3_                                                     
               'nZu         .',     -j                            .                             
               ,EZC         3XO     -o                           ,T                             
               /NgV        oK*:      '         .)l         p!    .!f                            
               .__,^V     +>_. y                !n        jMl     :Ye         Z^                
                   .*a    l/   -    ,j g+      .VP       =Tl.     _Y3         ,.                
               `+*  .,    .    >y   'v :.       ',       .'       _wwn*       C~                
                 .t* ._    *^.'     :u'             .=   ~n/      ~gXdne-.     q_,'             
                     >H_   tC^z    .>GY>__                '.      >QXm$w>s_    CRmw'            
                           )_)_   ,n$EqNmg_     ''   .`   C^ '.    .tgDNqnz,   fZXXu            
                                 .~Cqnuq!.     -wC.' ~z   n~,f-'  .zO!Tnac`  r_.nYa             
                                 _f;f.  ):     _pC>E        C~ G  _Xd*        s-nz              
                                  . ;*  .       '`.,'Z3+  *yT;^~3  ..           ~c              
                                    .`               `.   .'.   ,                .              
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
</div>
<div style="color: #5e3131">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                               ' ._                                                             
                               v                                                                
                                        s,                                                      
                                                                                                
                                                                                                
                                         t'                                                     
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                               'f.                                              
                                                =r                                              
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                    \n                                          
                                                     `                                          
                                                                                                
                                                    ,v                                          
                                           `       `   'a'                                      
                                           a_     /T  /4:                                       
                                                      l4,                                       
                                                     /$                                         
                                                  ,Gy `                                         
                                       f:          '.                                           
                                       .                  x:                                    
          v_                                            3_n^                                    
          .                                         _py ` '.                                    
                                            ),   ~8'~U+O4~p=    .`                              
                                           '.    _bn_.   9B|,'  |C                              
                                           y~     :~KC//\U^ uNr rb                              
                                                 ^E  =MM@+   VH^Rh                              
          C/                                   /KU: ;Un:$+o:3|ugU'                              
          ,                               f:   ._*b  `` $=n:dG~'f                               
          u;                              l,    ,4h     dQr Ec4n                                
          '                                       .     ,h_eKgOE                                
                                                           TqqT:                                
                                                           +'                                   
                                                                                                
        `                                  .        .       `                                   
        u/                                 v'      _x       e_                                  
        '.                                 en: xy3xennv     .                                   
        x;                             ):cyVdue````~Va/o:                                       
        '                              '3qCTV~`,*:3f~v:uyy:                                     
         C^                             yh~'au: ._V) . ```                                      
                                          v:oo,.  ;nt                                           
                                          c:s: t  _z                                            
                                               f`                                               
                                               nv                                               
                                               `.                                               
                                               r                                                
                                               .                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
</div>
<div style="color: #322119">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                            r:'   . 'r'-cs`                                     
                                    .     -.  \ '';. :an_`.                                     
                                   '==f: 'x:   .r  ~ .`r~cr.                                    
                                         >z'      \*_v  !-                                      
                                          .>.     ./vt`s-~.                                     
                                          cx.  .+ ^s   '                                        
                                     `r';.'`    . .~*                                           
                   sM          ./     .       >_)   .                                           
                   ._                         . .                                               
                                                  ._'                                           
                                                  .*r                                           
                                                .                                               
                                                \                                               
                                                  ;                                             
                             /_                                                                 
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                .-                                              
                                                _s.:.                                           
                                                  :Cf                                           
                                                   ..                                           
                                                   .r>          =                               
                                                    _!       +' .                               
                                                     ;>                                         
                                                                                                
            /'                                                                                  
             t`                                   .              .                              
                                                 ;x             _z                              
                                           !r`    .              :r                             
                                           .   :c                 .                             
         >'                                     .   :*                                          
         .                                           .                                          
                                                                 '^                             
             c.                                      `                                          
                                                     _                                          
        :>-                                                                                     
       ~'r_                                                                                     
       ; .        .^                                                                            
                        ~.                                                                      
                     -y-`                       ;                                               
       +`         ._                                 .>                                         
       +r'         _z> a_;'                    .      'r`                                       
       .!'         ;   t-                      t. '=.                                           
       ;'                ~-                .   y)`;y*   ......                                  
                  .        .           +- rc. .ffaeo*`. !)cfxe'>'.                              
                 .!       _^:           r'e_  rx3y3f\n*    *_   ns                              
       '`        .=/   /  ;`.       :es`.!C; =:''''..'\s`  .    `.                              
       >:         ..       r'r'      '-.)/'  ..t!-fs _f'cv'    ~=                               
       !_              r'  =rs`      'y4+.   cye\s'~z_) ``r`   >)>                              
       .s;                 ..         `a\ so_`zzae _o)efe)s.                                    
        >'                '..          rC4;z_.sr'on.~a+                                         
       .t_              ~_!;r.          sa_x~fx .-f>4s                                          
       -.            .     t:  .'..     r' tfxn:t:souc                                          
                    '*           -^           z _s                                              
        =-  _.                                xeafs+                                            
        .s;                                   e;e!..                                            
         .                                    .:ar                                              
          ~`                                    ..                                              
         r-                                                                                     
           *_                                                                                   
         .                                                              .                       
         >_                                                             ='                      
                                                                                                
   .+                                                                                           
                                                                                                
                                                                                                
                                                                                                
           ~:                                                                                   
     _                                                                                          
                                                                                                
                                                                                                
                '>                                                                              
                 .           t'                                             >.                  
                         r'*-.                                       \z     ss'                 
             rf        re//'                                  *3  .~  `     `z));               
          =y:.`;        .                                     .'             .'xs               
         *-    _*        >`    .;   '`.   ~.            .                       -f\             
               -t        ss`     .^_uz)`            .  .z;          ....                        
                           r`  .`  '+ `t/          -~ .ru_         'zaeo=.                      
                               _c     ~zb\              >-    r:      ;nz`                      
                          t-+>. .       .>'  v-;          =a:          '.                       
                         *; . /-+           /y_            .r'                                  
                         .    . .              ~                                                
</div>
<div style="color: #25261a">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                           ^                    
                               M                         ~.                .                    
                                    ._ '.  ..                           .                       
                                           '.           .               ;.                      
                                                    . . !`                                      
                                        ^.         .>,=                                         
                             ~                      . .                                         
                                                                                                
                         p^         ,+                                                          
                         .          .,         =   '>                                           
                          E!               +'  .                                                
                                                                                                
           .                                                                                    
           >:                                   ..                                              
                                                -_                                              
                              -;                                                                
                              `_,                                                               
                                                                                                
                                         ^.                                                     
              ^                                                                                 
                           .                                                                    
         _'     `! ._   .:._                 .. .    .                                          
                      . r' ^  .           ' >r=-=.. ,>  .!l:. /.                                
                      f/      +           =_   *'sl     *czxo-                                  
                      .     ^'.^          . r'!,t=      .....  t=                               
                            .           =,=x/)~'r;a= ./ =' l,  ._+                              
                                         >'. `  . ';=`>    .  =',l                              
                                    'lv)')_    ,*'~ .          !                                
       ~`    `               /'.     .l'^.     . .                                              
             ~.            ~:. r/              l.^                                              
            !.              ;+`               .;                                                
                                              f,r                                               
                                              `s.                                               
        _.                                     .                                                
        /                        'l        t!                                                   
                                  .        ..                     '~                            
                                .tj!    ~l`             =`                                      
        ^.                      .vv.                                                            
                                .ljr          .                                                 
                                'r-r          *                                                 
                              ~ 'jvt                                                            
                                ,jcc                                                            
                     .!`         _fxlcr.                                                        
                   ;._ ==       '=..;av`                                                        
                   _l.  .       ,l'r ..                                                         
                .   .   ; t,     -exl                                                           
       ~.      .^  ,=   :        -vt!.         .^-+             .                               
                                    ,t          `t+            ~t                               
                   .       _.      .'^ .            `+          '>                              
                  ,s_             _ar  ='+'                    ^                                
                            ;      `.  _                    >!. '^                              
                       ;    .          .                        '>                              
                       ..                                        .                              
                             _.      '=`                                                        
                              +      `t`         .    .                                         
                                                '!   -t   .                                     
                   `r^~_  ~.             .. .      ..:r..=s-...                                 
                                         la,s,    `=*>:)lvjjjvc`                                
                                         .` .      . 'rvcjfzl-.                                 
                                                       .=e;vev'                                 
                                   ,l'=.       *         r'*x;                                  
            ~'                    .!:+.=:      ac>                                              
            .                        ,r:       _=-!c>                                           
         *'       :l.               'la_                                                        
                 `j)!              .,rz:                          ..   .                        
                                  `s*                 .      . . .+l..,)' .                     
             ^'                   'v*           `+   'r   !` r`rl  '==   tz'                    
                   _~              ,!            . 'r        >f_`_       .`                     
                   ..    ;        :r              `l.        .. /n         ='                   
                     `r.       `_  '~              .            *'      +. .                    
                     ~a. ^                        ';     /.     `                               
                   `^  _            .     +:       ';                                           
                       ^        -~ .^          .    '_                                          
                                               l>              ~                                
                                               >         +'                                     
                                                      _v.=,                                     
                                                       ` .            't'                       
                   .;     +'+.                                     `+  .                        
                          .                                         .                           
            ='                =           v:            -                                       
               l       /*`      .!     f_!':         `                         t                
                .                     ./.           -=                                          
               -r          .   ~ .,^ ._  ~.   !    `                                            
                           ~`   '^           :+   `_                                            
                           c-                                                                   
                        +' _   ^               .;                                               
                             _l'~        l-_    '                                               
                                        ~^                                                      
</div>
<div style="color: #333b3a">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                t^T                             
                                                                Ms                              
                                                                     '=                         
                                                                                                
                                                                                                
                                     :a_                                                        
                                      ,                         a                               
                                                                '                               
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                    _v                                          
                                                   ,az                                          
                                            *, 't,v                                             
          yr.3_                                 :r    `v,                                       
          ta,`                                    .                                             
             t`.                                 _o'. `.                                        
              `xl .'                      )n\ `  `ays/V8;                                       
              n   ~e                       na:c     'e\9:                                       
              ,                          v,y_        ~l` of'                                    
                                         s,.    :l    `  yn: lnT                                
                                              v):)~C     ',3;.`'                                
        y~                                    .` ..rz      `):                                  
         o_                               9^'                 .                                 
                                            d~    .           v:                                
                                             . . ,r      '. .                                   
                                             v:v         p^ C\                                  
                                               .        n=  ,                                   
                                                        '                                       
                                                        y_                                      
                                                        '                                       
                                                                                                
                                              x                                                 
                                                                                                
                                       c:                                                       
                                                                                                
                                                                                                
                                :*                                                              
                                 . 't                             '*                            
                                    .                                                           
                                                            `  c:*                              
                  `                                         c:                                  
                 ')                                                                             
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                   ~E                                                           
                                   .hE`                                                         
                                    :Ob.                                                        
                                     ,T~                                                        
                                       V_                                                       
                                       '4E_                                                     
                'l                      'n8h:                                                   
                 .                  '=   .aN/                                                   
                                           .                                                    
                                                                                                
                                                                                                
                   .                                         .                                  
            .     _f          tz                             s,    `                            
            3\                 3                                  _v                            
            v_                 .       *:                          .         r9:                
           l/  :                    :e .                 *'  v^              bl                 
           .  e                      `  r.       ;rlz    .   `.           t' n~                 
              a                         `         `:z                        ` yps              
                     .                     `  v              r.`  :           *_h93,`           
                    '|:`       :'         .c` n                r ;d,          .   _h3           
                     _9s.      pe       ''f:  r                . `ec          *\   |e           
                    '*     `          `'3n,       `            * ;e            +  ;9z           
                           v:        _n3:        ~b             *                 _x            
                         v:'          `.        :v|u            `                  .            
                         .      '*             t   `            +                               
                                 .             .                                                
                                                                                                
           *'                                                                                   
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
</div>
<div style="color: #1b272a">                                                                                                  
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                           !)'    .         |'                  
                               &                               I'   '+ '   /`='                 
                                                                      't.    +`                 
                                                                                                
                                  ._                                                            
                                   .                                                            
                                                   .:                                           
                                                    .                                           
                                                             |`                                 
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
         ..                                     .;                                              
                                               `t.'^                                            
                                        /.    t .     .~.                                       
                                           !s'    .|sr. ;..                                     
                                                  -vlr!  ^*'                                    
                 _r   ;.                       .~  '=                                           
                '+_r         .                                                                  
                        t,   t'                                                                 
            d^ C           ;`                                                                   
            '. '               -t                                                               
                                -!                                                              
                                                                                                
                                                        .                                       
                                                        /..                                     
                                                          r_    .                               
                                                                v                               
                                                 '=             .                               
                                                  .          Mc                                 
                                                             /.                                 
        ^.                                                    H^                                
        r`                                                    _                                 
                _/                                     ,     U+                                 
               `t                                     '=.                                       
                                        /                                                       
                                                                                                
                                                                                                
                                                                  ./                            
                                                           !;      /!                           
                                                           .                                    
                   /                                          . t'^                             
                                                              r'                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                                
           ^                      ./                                                            
           .                                                                                    
           |                                                                                    
                                     - ~`                                                       
                                                                                                
                                                                                                
                                        ;'                                                      
                 'r.~                    '.                  ='                                 
                  . .                                                                           
                                                                          ~.                    
                 .                                                                              
                '~                                                                              
                             ~'                                                                 
                           /,                                                                   
           *,              .                              =,       -+                           
           `ll-                                .t         .         _;         /                
           /,=_                                 .                   -r.r,      ._               
        ~. ^,..|                                _                    .'r`   _=: .               
              =+    .    r,                 `'                   '      ^.    .                 
              _r   '=       .               |t'                 /o      r'_`. ;'                
               ;   `s~'.   'a~^                         _.                .=*..                 
                    '-I*` cofsv. ,r` .   .     .                  .   .   , ^_~`  .             
                     'l' ~v-=t+^'r_)_v   +`   rv                 ./  `;      ~,^ :c             
                          ' ''= 'IIe*;ft.    ranc  '~           ,|..           .!'|             
                                 _fea+`.   ^cfx'. `/            :+                              
                                  ._*.     ....                                                 
                             ;.     .                                                           
                                                                                                
                                                                                                
                                                                                                
                                                                                                
                                                                                        
</div>
</div>

<hr>

Avallach put the colourised ASCII into a .svg in order to prevent having all that code on our page. But if you want to see how the final 12 layers look like, just rightclick and take a look at the sourcecode.  

<pre class="logo">
    <a href="https://phoenixtales.de">                      
                      ,.                                                                           
                     ,aBV                                                                           
                     ,wgm`                                                                          
                     ')]gQv                                                                          
                    ;+9Qga'                                                                         
                    ^tBQgB_                                                                         
                     `y@gQL                                        `                                
  :                   ']QQK'                       ;+.       `)L^'                                  
   ._:`      `.'^,_w)`:)lQgQ&amp;$pL`     `,,-.       `x).          ,j+,`      `.              .:        
   xV+h_^7jG#BB@&amp;%d^.,.'GgggQQBJ   `7$&amp;@g@G|    `+V`          `[R[Ll&gt;`     &gt;'   "x^     '+bv        
    |l&amp;%xjb["""XgG:     Jggg&amp;%QD-  vQQ@IDggB,  .+l-           _RG)`,aU!    )+`  `LRh_:'xGp,         
    |mPQQQQd.'IQ8-      +gQB_|@$,  agQj`vggQ_ ^CU_^^,__)_-   .wmv   ,fd-   _X^    '=#0#BD"          
   `  _9QgggQvXgB_       "B@x ,&amp;Q_  KggC)0gg@" _DRx:,,^'`     +K,     ;a,   ^fL`     ,mB&amp;&amp;R+.        
     _hp@QggQQBJ`        ``  :DQ|  _Qggggg&amp;x`  =5mx         ^a"      :I_   .)&gt;      I#y'"wmD7'      
        ,xBgggX'             ,&amp;Qx   ,ybRhx-  ')7)v]`        ,L.       L[.   )|`    La"   `^_lPv'    
          `;aBggm,            )BB_            ';|" -_.             `   `J,   '7,`   ``      .`._x!   
            Vggg&amp;)           LBd'             -"_ .`'.       `,^.^,`   `.'  `_-`                    
          "PmQggg&amp;"         .jBPIL           '^    -,'`  .`  -y"'.v: `   ,:                 ..      
           `w8gQhQgm`        _0&amp;j"            ``     ,=" .'`,""'  "L``'.``   `.               .'     
         `JB@QQbGgQ_       :5@D)                   _)|L&gt;.-,'''   -^,-C'`. `   `                     
          :yBgQ@QgQ&gt;      .y$QX`                "^ |xv7_^'&gt;.````-;__")`:, ``                        
          .)Bgggggj     `&gt;!+&amp;%"        ,&gt;_)v=,-,|L__!)7t)+v``:,.:fPf-  `:'`        .:               
            `_9QDQ&amp;^   ```',C#_        ')_V7Jj];`. '``.,]mIV&gt;   'bGBb   ._.-"^  ` `;_                
             LG&amp;g0L   ^:,,vd9:             `+bLv;..` ^+Vdb9].` _twDb' ^yVx7__":.`LdU7)`             
              [QDX9`  `' `x@X`              _mPy:   :hRll+Cmh+^  .Kx  ;fxL_' `   ,Kabmw.            
            'f@BK_,    .:.)@J               "GX.   ^P7;^)v"|bL&gt;' `a+``'|!v_"&gt;'  `]jIIf7-.           
           `x@DL'`;)     ``)@)              `_%Gh&gt;  &gt;:','`.':"+IhL :+.  "_,!!``'v;!JK,`              
          ,Bgw  `"^    ```^j,                t$I   ` `:`   `^',J).     !)+)!.`-v]UC"                
           :&amp;D'  .'.       '             `` .`xw!      `    `'`..       ,+++|)"_wjfv_:               
          -0j             ;`               "'                `       .!vL);^'+lx".`.                
          _Bj            `'               `,`                 `       .."'  )]_`                    
          .jy           `.:                                               `_+                       
           ;'            .`                                                                         
                                                                                                    
                                                                                           </a></pre>


<style type="text/css">
  
  @import url("https://fonts.googleapis.com/css?family=Inconsolata|Roboto+Mono|Ubuntu+Mono|Cutive+Mono");
  
  :root {
    --blood: #934a46;
    --text: #ad9e8a;
  }

  pre {
    display: block;
    overflow-x: hidden;
    border: none;
  }

  hr {
    border-top: 1px dashed;
  }

  main {
    color: var(--text);
    font-size: 16px;
    line-height: 1.6;
    font-family: 'Ubuntu Mono', monospace !important;
  }

  main .logo {
    margin-top: 0;
    padding-top: 0;
    font-size: 8px;
    text-align: center;
    text-rendering: optimizeSpeed;
    color: #844d44;
    line-height: 8px;
  }
    main .logo a:hover { color: #1dd588; }

  @media (max-width: 900px) {
    main. .logo {
      font-size: 7px;
      line-height: 7px;
    }
  }

  .unchanged-ascii {
    font-size: 7px;
    text-align: center;
    font-family: 'Ubuntu Mono', monospace !important;
    text-rendering: optimizeSpeed;
  }

  .chaos-ascii { font-size: 8px; }

  main h1, main h2, main h3, .blood { 
    color: var(--blood); 
    font-weight: normal;
    text-align: center;
    padding: 0.5em 0;
    margin-top: 2em;
  }

  .article h1 {
    font-size: 45px;
  }

  main > img {
    margin: inherit auto;
    width: 50%;
  }

</style>