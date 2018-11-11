# git-study

## 1. ブランチを作ろう

Gitといえばブランチ！まずはブランチを作りましょう！

### コマンド派の人

```
git checkout -b new-branch
```

`git checkout` コマンドはブランチを移動するコマンドです。  
それに -b オプションを付けることで、「ブランチを作ってその作ったブランチに移動する」というコマンドになります。

### GUI(TortoiseGit)派の人

Gitリポジトリのフォルダを右クリック > TortoiseGit > Switch/Checkout  
Optionの「Create New Branch」にチェックを入れてブランチ名を入力してOK  
これで、上のコマンドと同じことをGUIで行うことができます。

![](img/1-cretae-branch.png)

### 2. 新しく作ったブランチで作業をしよう

ブランチを作ったらそこでやりたい作業を行います。  
ここでの作業はmasterブランチ（先ほどのブランチ）には影響しません。  
今回はファイルを作ってコミットしましょう！

### コマンド派の人

```
echo "Hello Git!" >> test.txt
git add test.txt
git commit -m "add test.txt"
git push origin new-branch
```

"Hello Git!" と記載された test.txt を作成  
`git add test.txt` で test.txt をステージング（コミットに含めたい変更に test.txt を追加）  
`git commit -m "add test.txt"` で"add test.txt"というメッセージでコミット  
`git push origin new-branch` リモート（GitHub）のnew-branchというブランチに変更を反映（この時にGitHub側にもnew-branchというブランチが作られます）

※ ちなみに、originとはデフォルトのリモートリポジトリの名前です。

```
# git remote -v
origin  https://github.com/k-nakayama-pg/git-study.git (fetch)
origin  https://github.com/k-nakayama-pg/git-study.git (push)
```

### GUI(TortoiseGit)派の人

test.txtを新規作成して "Hello Git!" と記述して上書き保存  
Gitリポジトリのフォルダを右クリック >


