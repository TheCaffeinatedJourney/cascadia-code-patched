# Cascadia Code Patched

This is a fork of the official Cascadia Code font. It replaces the greater-than less-than ligature (`<>`) with the not equal (`≠`) Unicode character.

The fonts are available for download from [/build/ttf/](https://github.com/TheCaffeinatedJourney/cascadia-code-patched/tree/main/build/ttf).

---



![Cascadia Code](images/cascadia-code.png)

# About Cascadia Code
Cascadia is a fun new coding font that comes bundled with [Windows Terminal](https://github.com/microsoft/terminal), and is now the default font in Visual Studio as well. 

# Font Variants
-  `Cascadia Code`: standard version of Cascadia
-  `Cascadia Mono`: a version of Cascadia that doesn't have ligatures
-  `Cascadia (Code|Mono) PL`: a version of Cascadia that has embedded Powerline symbols
-  `Cascadia (Code|Mono) NF`: a version of Cascadia that has Nerd Font symbols

For the italic, there is a standard `italic` and a `cursive` variant accessible via `ss01` (see [below](https://github.com/microsoft/cascadia-code/blob/main/README.md#to-enable-the-cursive-form-of-the-italic-heres-the-code-you-should-use)). 

# Font features
![Coding Ligatures](images/ligatures.png)
***Note**:* *`<>` is replaced with `≠` in this patched version.*

![Arrow Support](images/arrow_support.png)

![Stylistic Sets](images/stylistic_set.png)

Enabling stylistic sets will [vary between applications](https://github.com/tonsky/FiraCode/wiki/How-to-enable-stylistic-sets). For example, in VS Code, you can enable stylistic sets (and other OpenType features) via `settings.json`:

```
"editor.fontLigatures": "'ss01', 'ss02', 'ss03', 'ss19', 'ss20'"
```

#### To enable the Cursive form of the italic, here's the code you should use:
```
"editor.fontLigatures": "'calt', 'ss01'",
```
If you're using an environment that does not support the `ss01` OT feature, one option to consider is [opentype-feature-freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer/).

# Character Sets
![Cascadia Code](images/cascadia-code-characters.png)
![Cascadia Code Italic](images/cascadia-code-italic-characters.png)
![Symbols for Legacy Computing and other block elements](images/cascadia-legacycomputing-characters.png)

# Installation
**Note**: If you have previously installed a version of Cascadia Code, please uninstall the previous version *prior* to installing a new version. Not doing so can result in improper rendering. 

The patched fonts can be downloaded from: [/build/ttf/](https://github.com/TheCaffeinatedJourney/cascadia-code-patched/tree/main/build/ttf).

---
### Building the Fonts Yourself
To build the fonts yourself, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/TheCaffeinatedJourney/cascadia-code-patched.git
   cd cascadia-code-patched
   ```
2. **Set Up a Virtual Environment**:
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```
3. **Install Dependencies**:
    Use the requirements.txt file to install all necessary dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. **Buid the fonts**:
    Run the `build.py` script to generate the fonts:
    ```bash
    python build.py
    ```
4. **Locate the fonts**:
    The fonts will be located in the `/build/ttf/` directory.
