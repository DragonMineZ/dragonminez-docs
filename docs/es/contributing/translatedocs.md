If you want to contribute towards DragonMine Z, you can do so by translating the documentation into your language. This can help other people that do not speak English to be able to read the DragonMine Z Documentation and play the mod in their language.

Instructions on how to translate the Mod can be found [here](translate.md).

## **Setup**:
To start translating the documentation, you will need to have a local environment for testing your translations.
1. Open a Visual Studio Code new folder.  
2. Open a Terminal and paste the following commands in order:  
      - `pyp -m venv venv`  
      - `pip install -r requirements.txt`  
3. Then, run this to start the server:  
      - `mkdocs serve -f ./config/mkdocs.yml`  
      - **Note**: This will start a local server, which you can access by going to `localhost:XXXX` in your browser. The port number will be displayed in the terminal.

You can now start translating the documentation.

1. Open the `mkdocs.yml` file in the `config` folder.  
2. Scroll down until you see the variable name `languages` and input a new line like this:  
```diff title="mkdocs.yml"
      languages:
      - locale: en
          default: true
          name: English
          build: true
+     - locale: fr
+         default: false
+         name: Français
+         build: true
```
3. You'll also have to add translations to the navigation elements for French. To do this, please copy and paste the `nav_translations` section from the English to the French section and translate the text.
```diff title="mkdocs.yml"
      - locale: fr
          default: false
          name: Français
          build: true
+         nav_translations:
+               Home: Home
+               About: About
+               Credits: Credits
+               License: License
```  
This codeblock includes English translations, in this case, you would need to translate the English words after the colon into French.

## **Creating a new translation folder**
Now that you have set up the environment and the navigation translations, you can start translating the documentation.
To start, you will need to create a new folder in the docs directory with your 2-letter [ISO 639-1 language code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) (e.g. `fr` for French):
```
├─ docs/
│    ├─ en/
│    │   ├─ about/
│    │   ├─ contributing/
│    │   ├─ wiki/
│    │   │ └─ wiki/servers
│    │   └─ index.md
│    │
│    └─ fr/
│        ├─ about/
│        ├─ contributing/
│        ├─ wiki/
│        │ └─ wiki/servers
│        └─ index.md
```

Or you can just simply copy the `en` folder and its contents, and rename it to your language code.

## Submitting your translation
Once you finished translating the documentation, you can submit your translation by creating a Pull Request on the [DragonMineZ Documentation Repository](https://github.com/DragonMineZ/dragonminez-docs). Make sure to include the language in the PR title, so it's easier for the maintainers to identify the language you translated the documentation to.  
Then, we will review your translation and merge it into the main repository.

**Thank you for contributing to DragonMine Z!**
```