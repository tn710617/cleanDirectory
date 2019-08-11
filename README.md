English | [繁體中文](./README.zh-TW.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Introduction
A shell script with which you could delete files with specified condition in designated folder.

## Supported delete method
- Delete all
- Fuzzy matching
- File extension matching

## Usage
1. Clone this directory

```bash
git clone git@github.com:tn710617/cleanDirectory.git
```

2. Enter the designated folder's absolute path in the following double quotes, e.g. specifiedPath="$HOME/Downloads", after entering, please save and exit

```bash
cd cleanDirectory && vim cleanDirectory
```

3. Change the authority of the script 

```bash
sudo chmod 755 cleanDirectory
```

4. Move this script to one of the folders referenced by your $PATH, e.g. /usr/local/bin, and rename the script to the one you like

```bash
sudo move cleanDirectory /usr/local/bin/theScriptNameYouPrefer
```

5. Execute the script, and pass arguments, the passed arguments could be either singular or plural e.g. testClean jpg exe txt

```bash
scriptName jpg png
```
6. If you do NOT mean to perform deleting operation, enter either n or N to abort the script
7. If you mean to to delete files, enter either y or Y to continue
8. If no arguments are passed, this script will delete everything in the designated folder
9. If arguments detected, options will prompt to let you choose either 'fuzzy search' or 'file extension search', simply enter 1 for fuzzy search or 2 for extension search
    - If you choose fuzzy search, whatever matches the passed arguments will be deleted, e.g. All of the files whose name match the passed strings but ignore the file extension
    - If you choose extension search, whatever files with extension matching the passed strings will be deleted
10. And then this scrip will delete files according to the options you chose.

Note: If designated folder's absolute path is not specified, the script will abort.

