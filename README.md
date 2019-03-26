# Todo-I-Learned

## 過去分2019年～2019/03/25
### slack
使い方、ファイル連携、チャンネル、ファイルアップロード制限、削除Scriptの実装手法、出来ることをINPUT

### Node.js
- 実装メモ
  - app.jsで読み込むファイルを指定する。(アクセスされたurlに対して呼び出すファイルを指定。)  
  - routes内で、アクセスされたurl・getかpostかで取得、処理するサーバーサイドjavascriptを処理する。  
  　必要であれば、module.exports = 処理メソッド名;で、他jsファイルで require(import)できるようにする。  
  - views/XXX.ejsはhtmlファイルとほぼ同義で、<%= routesのres.rendorで設定した値 %>で値設定できる。  

また勉強し直す必要あり。

### Vue.js
- 算出プロパティ：computed→キャッシュされているので、何度も値が変わらない。  
- メソッド：method→常に関数を実行する→必要以上に実行されるので、何度も実行の必要性がなければcomputed  
https://jp.vuejs.org/v2/guide/computed.html  

### vuex.jsについて
- store(state)→値が入っている。管理されてる
- computedを使うことでstore(state)の値を参照できる。
  →mapStateヘルパーを使うと、複数のstate値を参照できる。
- stateの値を変更・更新したい場合、mutations:ミューテーション(関数的なもの)を定義し、
   store.commit('関数名')で呼び出して変更する。
- アクションはミューテーションとは異なり、値を変更しない。アクションからstateにアクセス→store.commitでミューテーションを呼び出せる。
- アクションはディスパッチ:dispatchから呼び出せる。

##### Dispatch→Action→state
