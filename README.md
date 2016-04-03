# git_simple_commit_message_editor

## What is this?

対話的にコミットメッセージを記入できるスクリプトです。
チーム内でコミットメッセージに書いて欲しいことをゆるく統一したい場合などに。

![](https://raw.githubusercontent.com/shimokei53/git_simple_commit_message_editor/master/tty.gif)

## How to use

```
$ chmod +x gscme
$ mv gscme /usr/local/bin/gscme
$ git config --local core.editor gscme
```

mergeやrebaseの際はエディタを起動します。
`CORE_EDITOR`という項目があるので、そちらへエディタを設定してください。

## 表示される質問リストについて
`.gscme_msglist` というファイルを自動で作成します。
一行毎に表示されるので、お好みに合わせて編集してください。
チーム内でこのファイルのみ共有すればいいかなと思います。
