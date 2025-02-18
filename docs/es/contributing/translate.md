If you want to contribute towards DragonMine Z, you can do so by translating the Mod's lang.json file. This file contains all the text that the mod uses, such as item names, descriptions, commands output, GUI text and more.  

To translate the mod, you need to follow these steps:

## **I. Check the current available translations**
Before starting a new translation, check if the language you want to translate is already available.
The mod by itself comes with the English language, Spanish (Latin América) and Spanish (Spain) translations.  
If you want to translate to a different language, you can check the 
mod Source Code on GitHub or Crowdin to see if the language you want to translate is already available.

- [DragonMine Z GitHub](https://github.com/DragonMineZ/dragonminez/tree/main/src/main/resources/assets/dragonminez/lang)
- [DragonMine Z Crowdin](https://crowdin.com/project/dragonmine-z)

## **II. Instructions for creating a new translation**
If the language you want to translate is not available, you can create a new translation:
1. Copy the `en_us.json` file from the `lang` folder in the mod's source code repository/crowdin project.
2. Rename the file to the language code you want to translate to. Acording to the [Locale Code](https://minecraft.wiki/w/Language) used by *Mojang*, for example: `fr_fr.json`.
3. Make sure to keep the same structure and format of the original file.
4. The .json file **must** be saved using a text editor that supports UTF-8 encoding. We recommend using [Notepad++](https://notepad-plus-plus.org/).

If your language uses a character set which needs to be handled with Unicode characters, you can type them directly into the file. There is **no longer a need** to use Unicode hexadecimal Numeric Character Reference (NCR) codes (like \u0202).

**Example:** 
```{.json .copy .select}
"commands.dmz.dmzpoints.add": "You added %d points to..."
```  
<span style="color:red">**Incorrect**</span>**:** 
```{.json .copy .select}
"commands.dmz.dmzpoints.add": "\u60A8\u5DF2\u6DFB\u52A0 %d \u70B9\u5230..."
```   
<span style="color:green">**Correct**</span>**:** 
```{.json .copy .select}
"commands.dmz.dmzpoints.add": "您已添加 %d 点到..."
```

### **III. How to translate a *.json* file**
- Open the .json file with a text editor that supports UTF-8 encoding, such as [Notepad++](https://notepad-plus-plus.org/). You'll see a structure like this:
```{.json .copy .select}
  "commands.dmz.dmzpoints.add": "You added %d points to...",
  "commands.dmz.dmzpoints.remove": "You removed %d points from...",
  "commands.dmz.dmzpoints.set": "You set %d points to..."
```

- Translate the text on the right side of the colon `:`. Do not translate the text on the left side of the colon `:`.  
**Example:**
```{.json .copy .select}
  "commands.dmz.example.translation": "This is an example translation"
```  
<span style="color:red">**Incorrect**</span>**:** 
```{.json .copy .select}
  "commands.dmz.exemple.traduction": "Ceci est une traduction d'exemple"
```
<span style="color:green">**Correct**</span>**:** 
```{.json .copy .select}
  "commands.dmz.example.translation": "Ceci est une traduction d'exemple"
```

- Many strings contain one or more ***placeholders***. For example, `%d` is a placeholder that will be replaced by a number when the string is displayed; and `%s` is a placeholder that will be replaced by a string. Also, some strings contain color codes, `\u00A7` is referred to as the section sign, `§`, the color code formatting character in Minecraft. You can see the [color codes here](https://minecraft.fandom.com/wiki/Formatting_codes), to make this work, you have to follow the color code by a letter or number, for example, `\u00A7b` will make the text blue, while `\u00A7r` will reset the color to white.  
You **must** keep these placeholders in the translated text, but you have the freedom to reorder these parameters if it is required by the grammar rules of your language. For Example:
```{.json .copy .select}
    "command.dmzpoints.set": "You have \u00A7bset \u00A7rthe %s's points to %d."
```

When the above phare is displayed ingame, the placeholders will be replaced by actual ingame values, like this:

**"You have <span style="color:cyan">set</span> the ezShokkoh's points to 1750."**

**Remember:**
- Do not add line breaks or HTML to any of the strings.
- Do not translate or remove the special characters combinations used by Minecraft to change colors. (\u00A7b = §b)

### **IV. Testing the translation**
1. Use a zip program like [WinRAR](https://www.win-rar.com/start.html?&L=0) or [7-Zip](https://www.7-zip.org/) to open your DragonMineZ.jar file.
2. Navigate to the `assets/dragonminez/lang` folder and put your translated file there.
3. Close the zip program and launch the game, then select the language you translated to in the game's language settings and check if the translation is working correctly.
4. Please test the translation as best as you can, specially to see if the placeholders are being replaced correctly and if the text fits in the GUI.
5. If you find any issues, you can fix them and test again.

### **V. Submitting the translation**
1. Once you have finished translating and testing the file, you can submit it to the mod's GitHub repository or Crowdin project.
2. If you are submitting to the GitHub repository, you can create a Pull Request with your changes.
3. If you are submitting to the Crowdin project, you can upload the file directly to the project.
4. Alternatively, you can contact us by opening a Ticket on the [DragonMine Z Discord](https://discord.gg/b5MgRNb3D7) and send us the file.

Also, you can check the Contributing Guidelines on the [DragonMine Z GitHub](https://github.com/DragonMineZ/dragonminez/blob/main/.github/CONTRIBUTING.md) for more information.

