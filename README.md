# git_simple_commit_message_editor

## What is this?

対話的にコミットメッセージを記入できるスクリプトです。
チーム内でコミットメッセージに書いて欲しいことをゆるく統一したい場合などに。

```
$ git commit
どのような変更ですか？ > Postに公開日時を追加
この変更によって,どんなことが起きますか？ > 記事の公開日時を保存できるようになった
なぜその変更が必要でしたか？ > created_atではなく、公開日でソートしたいという要望があったので
参考URLなど（あれば） > https://www.google.co.jp/
[master 8167561] Postに公開日時を追加 記事の公開日時を保存できるようになった created_atではなく、公開日でソートしたいという要望があったので https://www.google.co.jp/
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 hoge
```

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
