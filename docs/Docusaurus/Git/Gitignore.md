---

sidebar_label: 'Gitignore'
sidebar_position: 2

---
# Gitignore

Gitignore 主要作用是告訴 Git 哪些檔案或目錄應該被忽略，不納入版本控制。
如果你在 GitHub 建立過專案， GitHub 就會預先幫你建立定義好的忽略清單

command

````code

touch .gitignore
````

示例

````code
# 忽略所有 .log 文件
*.log

# 忽略 build 目录
/build/

# 忽略 doc 目录下的所有 .txt 文件，但不忽略 doc/server/arch.txt
/doc/**/*.txt
!/doc/server/arch.txt

# 忽略所有 .tmp 文件和 .temp 目录
*.tmp
.temp/

````

各種語言的 .gitignore

github docs Ignoring files

https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files