# Gitの練習用リポジトリ
これはdevelopブランチ

## このリポジトリの構成
- developブランチ   
    開発はこのブランチを中心にする

- (featureブランチ)
    機能の実装はfeatureブランチの下で行う
    
- mainブランチ  
    公開できるものを入れておくブランチ

## 手順
1.  リモートのリポジトリをローカルにクローンして開く
    ```sh
    git clone https://github.com/tsubame-rustica/practice-git.git
    ```
    ```sh
    cd ./practice-git
    ```

2.  新しいブランチを作成
    ```sh
    git checkout -b feature/自分の名前/test
    ```
    今回はブランチ名を`feature/自分の名前/test`としているがプロジェクトの命名規則に従う  
    基本的には何をするブランチなのかが分かりやすい名前にする

3.  新しく`test.md`ファイルを作成

4. 現在のステータスを確認
    ```sh
    git status
    ```

5.  保存したらステージング（コミットするファイルを登録）
    ```sh
    git add test.md
    ```

6.  コミットする（ファイルの変更を保存する）
    ```sh
    git commit -m "add test.md"
    ```
    コミットメッセージにも何をしているのかがわかるような内容にする

7.  リモートにプッシュする（GitHubに変更を反映させる）
    ```sh
    git push origin feature/自分の名前/test
    ```

8.  GitHubでプルリクエストを作成

9.  承認されたらブランチを`develop`に切り替える
    ```sh
    git checkout develop
    ```

10. リモートからの変更を取り込む
    ```sh
    git fetch
    ```

11. リモートからの変更を取り込んで統合する
    ```sh
    git pull origin develop
    ```

12. ブランチ名を変えて手順2〜11を繰り返す
