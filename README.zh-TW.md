[English](./README.md) | 繁體中文

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 介紹
這是一個可以依照指定條件來刪除指定資料夾內檔案的 shell script

## 支援的刪除方式
- 全部刪除
- 模糊刪除
- 副檔名刪除

## 使用方法
1. clone 專案

```bash
git clone git@github.com:tn710617/cleanDirectory.git
```

2. 請在變數 `specifiedPath` 後的 `double quotes` 當中輸入你想要執行刪除動作的絕對路徑, 例如 `specifiedPath="$HOME/Downloads"`, 輸入完後請存檔離開

```bash
cd cleanDirectory && vim cleanDirectory
```

3. 改變 script 的權限

```bash
sudo chmod 755 cleanDirectory
```

4. 將此檔案移動到 $PATH 變量的資料夾內，例如 /usr/local/bin, 並且將檔名改成你喜歡的名稱, 例如 `cleanDownloads` or `cleanDesktop`

```bash
sudo move cleanDirectory /usr/local/bin/theScriptNameYouPrefer
```

5. 執行檔案，並視需求帶入參數，參數可單個或多個，例如 testClean jpg png txt
6. 如果你沒有要執行刪除動作，請按 n 或 N 停止
7. 如果你的確想執行刪除動作，請按 y 或 Y 繼續
8. 如果沒有帶入任何參數，將自動刪除所有位於指定資料夾內的檔案
9. 如果參數有帶入，選擇視窗將會跳出，可選擇要根據帶入的參數進行 1) 模糊搜尋刪除或是 2) 副檔名搜尋刪除, 輸入 1 或 2 來決定你要刪除檔案的方式
    - 如果你選擇模糊刪除，只要檔名含有帶入的字串都會被刪除哦, 但是檔案的副檔名不會被列入搜尋範圍內
    - 如果你選擇副檔名刪除，那不管檔名是什麼，只要副檔名符合帶入條件的檔案就會被刪除哦
10. 輸入完畢後, 程序將會開始執行刪除動作

備註: 如果指定資料夾的絕對路徑沒有指定，程序將會終止並且退出。

