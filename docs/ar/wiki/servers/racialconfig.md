# Race-based Configuration

## _**Overview**_

Every race has its own unique configuration file that can be found in the `config/races` directory. These files are used to define different values for each race, so that they can have unique stats and other features. For example, having a Tank race, a Melee focused race, and a Ki focused Race.

In the `config/races` directory, you will find a file for every race that contains almost the same values. These values are used to define the "multiplier" for every stat. Also, you're gonna find a "Passive" section that contains the passive skill that each race has.

## **_Stats_ Configuration**

As mentioned before, in the `DMZ<Race>Config.toml` file, you'll find a section called `Warrior Class Multiplier` and a `Warrior Class Initial Stats`; along with other section called  `Spiritualist Class Multiplier` and a `Spiritualist Class Initial Stats`. These sections are used to define the multiplier for each stat for each class.

### **_`<Class>`_ Class Multiplier**

You'll have to define the multiplier for each stat for each class.\
The stats are: `STR - Strenght`, `DEF - Defense`, `CON - Constitution`, `PWR - Ki Power` and `ENE - Energy`.
These values are used to calculate the final stats, for example:\
If a race have a `CON` multiplier of 1.2 and 100 points in the CON stat, will have `144 HP`.\
If a race have a `CON` multiplier of 1.8 and 100 points in the CON stat, will have `216 HP`.

| Stat | Min Value           | Default Value       | Max Value             |
| ---- | ------------------- | ------------------- | --------------------- |
| STR  | 1.0 | 1.0 | 200.0 |
| DEF  | 1.0 | 1.0 | 200.0 |
| CON  | 1.0 | 1.0 | 200.0 |
| PWR  | 1.0 | 1.0 | 200.0 |
| ENE  | 1.0 | 1.0 | 200.0 |

##### This table can be used as reference for both classes.

Remember that, if you modify the `Warrior Class Multiplier` in the `DMZSaiyanConfig.toml` file, you have to create a Saiyan using the Warrior Class to see the changes.\
If you modify the `Spiritualist Class Multiplier` in the `DMZSaiyanConfig.toml` file, you have to create a Saiyan using the Spiritualist Class to see the changes.

### **_Passive Skill_ Configuration**

Every race has its own passive skill. This skill is defined in the `Passive` section.

1. `Humans` have a Passive Skill that increases the Ki Regeneration whilst holding the `Ki Charge` key by a 25%.
2. `Saiyans` have its iconic Zenkai Passive, that increases the player stats a 10% and heals a 25% HP after surviving 6 seconds below 10% HP. This passive has a cooldown of 45 minutes and a maximum of 2 uses per character.
3. `Nameks` have a Passive Skill that increases the passive Ki Regeneration by a 40%.
4. `Bio Androids` have a Passive Skill that heals a 5% of the damage dealt while being below 50% HP, increased by a 10% if below 25% HP.
5. `Cold Demons` have a Passive Skill that increases by x1.2 the TPs gained by every source. This works even better in the `Hyperbolic Time Chamber` or in the `King Kai's Planet`, due to the natural multiplier of these places.
6. `Majins` have a PAssive Skill that heals a 1% HP every second.

| Race Passive                                       | Min Value           | Default Value       | Max Value            |
| -------------------------------------------------- | ------------------- | ------------------- | -------------------- |
| Humans                                             | 1                   | 25                  | 100                  |
| Saiyans: Stat Boost                | 1                   | 10                  | 30                   |
| Saiyans: HP Heal                   | 1                   | 25                  | 100                  |
| Saiyans: Cooldown                  | 1                   | 45                  | 600                  |
| Saiyans: Max Uses                  | 1                   | 2                   | 10                   |
| Nameks                                             | 1                   | 40                  | 100                  |
| Bio Androids: Half HP LifeSteal    | 1                   | 5                   | 50                   |
| Bio Androids: Quarter HP LifeSteal | 1                   | 10                  | 50                   |
| Cold Demons                                        | 1.0 | 1.2 | 3.0  |
| Majins                                             | 1.0 | 1.0 | 10.0 |

### **_Transformations_ Configuration**

Also, inside the `config/races` directory, you'll find another directory called `transformations`. This directory contains the transformation files for every race and transformation.\
In those files, you'll find the `Multiplier` value, that is used to define the multiplier for the `STR`, `DEF` and `PWR` stats for each transformation.\
Also, you'll find the `Ki Cost` value, that is used to define the Ki cost for each transformation.

For example, in the `DMZTrBioAndroidConfig.toml` file, you'll find the `Bio Android` transformations, `Imperfect` being the base form.\
We're gonna use the `Imperfect` transformation as an example.

| Imperfect Value | Min Value           | Default Value       | Max Value             |
| --------------- | ------------------- | ------------------- | --------------------- |
| Multiplier      | 1.0 | 1.0 | 200.0 |
| Ki Cost         | 0                   | 0                   | 20000                 |

##### This table can be used as reference for every transformation.

While being in the `Imperfect` transformation (the Base form), the player will have normal stats, and no ki consume.\
If you transform into `Semi-Perfect` form, the player will have, for example: a 1.2 multiplier for the `STR`, `DEF` and `PWR` stats, and will consume 500 Ki.\
So, if in the `Imperfect` form, the player has 100 points in the `STR` stat, in the `Semi-Perfect` form, the player will have 120 points in the `STR` stat.

## **Important Notes**

The Transformations Multipliers are `additive` to **other types** of multipliers, like the `Effects Multipliers` or the `States Multipliers`.\
So, if you're in the `Semi-Perfect` form, and you have a `STR` multiplier of 1.2, and you use the `Majin` effect that gives you a 1.5 multiplier, you'll have a 1.7 multiplier for the `STR`, `DEF` and `PWR` stats.

The Transformations Multipliers **cannot** be added or multiplied by other `Transformations Multipliers`.
