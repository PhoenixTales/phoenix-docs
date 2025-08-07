# Phoenix Docs

## README

```  
PHOENIX DOCS

"Phoenix Design Concept"
2016-2022 by PhoenixTales

Authors:  Flosha, Logx, Arbax, Avallach
          Auronen, Dmitriy

Changed last:  24.11.2022
```  

These are the Design Documents of **Phoenix** (also known as *Project Nyx*), a radically immersive gothic RPG developed by [PhoenixTales](https://phoenixtales.de) and based on Gothic by Piranha Bytes. Here you find all our research and planning based on the original vision of Gothic (which had *Phoenix* as its working title) that we preserve and present in our [Gothic Archive](https://gothicarchive.org).  

Since we target an international audience and are an international team from Germany, Poland, Romania, Czechia and with associations to Ukraine, Russia and Slovakia, we write the documentation in English.  

The docs are work in progress, they are currently rewritten and will be unlocked over time. Plot documents will not be unlocked before release. Due to the current ongoing work on the order and internal structure of docs regular changes to the Index are to be expected. We plan for a physical print of the docs when we're done.  


### Links

* Dev: [phoenixtales.de](https://phoenixtales.de)
* Phoenix: [phoenixthegame.com](https://phoenixthegame.com)
* Gothic: [gothicarchive.org](https://gothicarchive.org)
* Git: [phoenixtales-github](https://github.com/PhoenixTales)
* Community: [phoenix-discord](https://discord.gg/CK4VAR7fpH)

### Local testing/development

1. Install Ruby on your machine. You will have to search how to do this yourself, since there are a lot of different OSs out there, and each Linux distro has its own way to install it, but one of these [guides](https://jekyllrb.com/docs/installation/#guides) may help. Also it is possible to instal a specific Ruby version and even several Ruby versions with ruby version managers, such as [rbenv](https://github.com/rbenv/rbenv), but it may be an overkill if you don't need several versions of Ruby installed on your machine. Currently it is required to use the Ruby version of `>= 3.0.0`, since the bundler version of `2.5.20` is used and requires this minimum version of Ruby.

2. After installing Ruby, install [bundler](https://rubygems.org/gems/bundler/versions/2.5.20) with this command `gem install bundler -v 2.5.20`. Currently this version is used to manage dependencies, so it is better for everyone to use the same version, but in the future it will be updated if needed. More info [here](https://bundler.io/).

3. From the root directory of the project, run this command to install the required gems `bundle install`.

4. Then run the development server `bundle exec jekyll serve`, or `bundle exec jekyll serve --force_polling` if you see that Jekyll does not rebuild the site on change, which is an issue on Windows, then open http://127.0.0.1:4000 in your browser. If not needed anymore, to stop the server press `ctrl/command + c`.

#### How it works

GitHub has a built in support for Jekyll sites, but it is very restrictive, since it only supports these [gems/plugins/etc](https://pages.github.com/versions/). To be able to enforce those versions while testing the site locally, [github-pages](https://github.com/github/pages-gem) gem is used to match GitHub Pages build environment as close as possible. Also this gem already includes most of the jekyll plugins and jekyll itself with the supported versions, those just have to be included in the `_config.yml`, so they could be used to test the site locally. More info about GitHub Pages and Jekyll [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).

Also, despite this built in support of GitHub Pages uses a specific version of Ruby, it doesn't mean that this exact version have to be used when testing the site locally, the only requirement is that all of the installed gems supported your locally installed version of ruby (See the first step in Local testing/development).

There is a second way of using Jekyll on Github with more flexibility by using custom [GitHub Actions](https://jekyllrb.com/docs/continuous-integration/github-actions/), though it has limited free "build minutes" per months per account, which may or may not be enough.
