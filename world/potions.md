# Potions

**Author:** *flosha*, 20.08.2026

Todo: 
* Add Sequel names/values
* Add Alpha potions/values
* Add Phoenix potions/values


## Temp Potions (Gothic)

| Potion                    | Internal Name         | Effect  |
|---------------------------|-----------------------|---------|
| Essenz heilender Kraft    | ItFo_Potion_Health_01 | 25 HP   |
| Extrakt heilender Kraft   | ItFo_Potion_Health_02 | 35 HP   |
| Elixier heilender Kraft   | ItFo_Potion_Health_03 | 50 HP   |
| Essenz magischer Energie  | ItFo_Potion_Mana_01   | 25 Mana |
| Extrakt magischer Energie | ItFo_Potion_Mana_01   | 45 Mana |
| Elixier magischer Energie | ItFo_Potion_Mana_01   | 65 Mana |
| Trank der Geschwindigkeit	| ItFo_Potion_Haste_01  | 1 Min   |
| Trank der Schnelligkeit   | ItFo_Potion_Haste_02  | 2 Min   |
| Trank der Eile            | ItFo_Potion_Haste_03  | 5 Min   |


### Additional Phoenix Potions

| Potion                    | Internal Name         | Effect  |
|---------------------------|-----------------------|---------|
| Psi Essenz                | ItFo_Potion_Psi_01    | 25 Psi  |
| Psi Extrakt               | ItFo_Potion_Psi_02    | 45 Psi  |
| Psi Elixier               | ItFo_Potion_Psi_03    | 65 Psi  |

ToDo: Change Effect values to fit to the Alpha attribute values. 


## Perm Potions (Gothic)

| Potion                       | Internal Name               | Effect       |
|------------------------------|-----------------------------|--------------|
| Essenz des Lebens            | ItFo_Potion_Health_Perma_01 | +5 HP        |
| Extrakt des Lebens           | ItFo_Potion_Health_Perma_02 | +10 HP       |
| Elixier des Lebens           | ItFo_Potion_Health_Perma_03 | +15 HP       |
| Essenz des Geistes           | ItFo_Potion_Mana_Perma_01   | +5 Mana      |
| Extrakt des Geistes          | ItFo_Potion_Mana_Perma_02   | +10 Mana     |
| Elixier des Geistes          | ItFo_Potion_Mana_Perma_03   | +15 Mana     |
| Essenz der Geschicklichkeit  | ItFo_Potion_Dex_01          | +3 Dex       |
| Extrakt der Geschicklichkeit | ItFo_Potion_Dex_02          | +5 Dex       |
| Elixier der Geschicklichkeit | ItFo_Potion_Dex_03          | +8 Dex       |
| Essenz der Stärke            | ItFo_Potion_Strength_01     | +3 Str       |
| Extrakt der Stärke           | ItFo_Potion_Strength_02     | +5 Str       |
| Elixier der Stärke           | ItFo_Potion_Strength_03     | +8 Str       |
| Trank der Macht              | ItFo_Potion_Master_01       | +4 Str & Dex |
| Trank der Herrschaft         | ItFo_Potion_Master_02       | +6 Str & Dex	|


### Additional Phoenix Potions

| Potion               | Internal Name | Effect    |
|----------------------|---------------|-----------|
| Psi Perm. 1          |               | +1 Psi    |
| Psi Perm. 2	         |               | +2 Psi    |
| Psi Perm. 3	         |               | +3 Psi    |



## Phoenix Potions

**Balancing:**  
Due to the alpha attribute values, the potion values had to be heavily modified to fit into this scheme. 
When there is a maximum of 15 Strength, 30 HP, 30 Psi, 30 Mana etc., perm potions cannot give boni as high as they did in the release version (e.g. +5, +10, +15) where one could acquire three or more times as much points.

**Naming Convention:**  
Potions follow a new, simpler and more descriptive naming convention:  
`ItFo_Potion_[Name]` → `ItPo_[Name]`


