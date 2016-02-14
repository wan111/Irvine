common\Utils.dms
================

名前空間:
=========

Utils
-----
ユーティリティ関数群  
Utilsオブジェクト

   * メンバー:  

      * < static, constant > UNDEFINED : {undefined}  

      * < static > isDorothy2A : {boolean}  
         実行環境がDorothy2Aならばtrue  

      * < static > isDorothy2set : {boolean}  
         実行環境がDorothy2setならばtrue  

      * < static > isDorothy2ListMenu : {boolean}  
         実行環境がOnListMenuClickのDorothy2set(「Dorothy2サイト設定」)ならばtrue  

      * < static > isDOA : {boolean}  
         実行環境がDOAならばtrue  

      * < static > isRentan : {boolean}  
         実行環境がDorothy2Rならばtrue  

      * < static > queueFolder : {string}  
         folderdata.Postのコメントオプションから取得したキューフォルダのパス  

   * メソッド:  

      * < static > error(message, fileName, line, name) → {String}  
         エラーメッセージを整形して返します

         * パラメータ:

         | 名前     | 型            | 引数   | 既定値                   | 説明             |
         |----------|---------------|--------|--------------------------|------------------|
         | message  | string        |        |                          | エラーメッセージ |
         | fileName | string        | 省略可 | Dorothy.matchFile+'.dms' | ファイル名       |
         | line     | string,number | 省略可 | ''                       | エラー発生箇所   |
         | name     | string        | 省略可 | 'Error'                  | エラー名         |
         

         * 戻り値:   

            * {String} : 整形した文字列のStringオブジェクト 各引数をプロパティに追加

      * < static > showError(message, fileName, line, name) → {String}  
         エラーメッセージを整形してalertで表示します

         * パラメータ:

         | 名前     | 型            | 引数   | 既定値                   | 説明             |
         |----------|---------------|--------|--------------------------|------------------|
         | message  | string        |        |                          | エラーメッセージ |
         | fileName | string        | 省略可 | Dorothy.matchFile+'.dms' | ファイル名       |
         | line     | string,number | 省略可 | ''                       | エラー発生箇所   |
         | name     | string        | 省略可 | 'Error'                  | エラー名         |
         

         * 戻り値:   

            * {String} : 整形した文字列のStringオブジェクト 各引数をプロパティに追加

      * < static > isStr(v) → {boolean}  
         文字列として扱えるか判定します string String StringBufferならばtrue

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | v    | *  |      |
         

         * 戻り値:   

            * {boolean}

      * < static > toStr(v) → {string}  
         文字列に変換

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | v    | *  |      |
         

         * 戻り値:   

            * {string}

      * < static > toNumber(v, def) → {number|T}  
         数値に変換 数値に変換できないものはNaNを返します。

         * パラメータ:

         | 名前 | 型 | 引数   | 説明                           |
         |------|----|--------|--------------------------------|
         | v    | *  |        |                                |
         | def  | T  | 省略可 | 数値に変換できない場合に返す値 |
         

         * 戻り値:   

            * {number|T}

      * < static > toInteger(v) → {number}  
         整数値に変換

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | v    | *  |      |
         

         * 戻り値:   

            * {number}

      * < static > objToPrimitive(v) → {string|number|boolean|null|undefined}  
         オブジェクトをプリミティブ値に変換

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | v    | *  |      |
         

         * 戻り値:   

            * {string|number|boolean|null|undefined}

      * < static > strToPrimitive(s) → {string|number|boolean|null|undefined}  
         文字列をプリミティブ値に変換
         例: "true" -> true

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | s    | *  |      |
         

         * 戻り値:   

            * {string|number|boolean|null|undefined}

      * < static > extractPath(s) → {string}  
         渡された値からパスを取り出します

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | s    | *  |      |
         

         * 戻り値:   

            * {string} : パス

      * < static > extractName(s) → {string}  
         渡された値からファイル名を取り出します

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | s    | *  |      |
         

         * 戻り値:   

            * {string} : ファイル名

      * < static > extractExt(s) → {string}  
         渡された値から拡張子を取り出します

         * パラメータ:

         | 名前 | 型 | 説明 |
         |------|----|------|
         | s    | *  |      |
         

         * 戻り値:   

            * {string} : 拡張子

      * < static > formatTemplate(s, map) → {string}  
         渡された文字列から 置換変数(%～%) を置換して整形します  
         mapのプロパティと同名の置換変数をその値で置き換えます mapに存在しない名前の置換変数は削除されます

         * パラメータ:

         | 名前 | 型     | 引数   | 説明                             |
         |------|--------|--------|----------------------------------|
         | s    | string |        |                                  |
         | map  | Object | 省略可 | 置き換えに使用されるオブジェクト |
         

         * 戻り値:   

            * {string} : 整形した文字列

      * < static > call(fn, selfObj, var_args) → {*}  
         .call()の代替 関数のモードを変更せずに呼び出します。 戻り値で渡される関数が内部で元とは別の関数として扱われるのを利用しています

         * パラメータ:

         | 名前     | 型       | 引数   | 説明                                 |
         |----------|----------|--------|--------------------------------------|
         | fn       | function |        | 呼び出す関数                         |
         | selfObj  | *        |        | 関数fnの内部でthisとして使用される値 |
         | var_args | *        | 可変長 | 関数fnに渡される引数                 |
         

         * 戻り値:   

            * {*} : 関数fnの返り値

      * < static > apply(fn, selfObj, argsArray) → {*}  
         .apply()の代替 関数のモードを変更せずに呼び出します

         * パラメータ:

         | 名前      | 型       | 引数     | 説明                                           |
         |-----------|----------|----------|------------------------------------------------|
         | fn        | function |          | 呼び出す関数                                   |
         | selfObj   | *        |          | 関数fnの内部でthisとして使用されるオブジェクト |
         | argsArray | Array    | null許容 | 関数fnに渡される引数                           |
         

         * 戻り値:   

            * {*} : 関数fnの返り値

      * < static > has(obj, key) → {boolean}  
         objがkeyを持っているか

         * パラメータ:

         | 名前 | 型     | 説明 |
         |------|--------|------|
         | obj  | object |      |
         | key  | string |      |
         

         * 戻り値:   

            * {boolean}

      * < static > getObject(name, obj, def) → {*}  
         指定した完全修飾名のオブジェクトを取得します objを指定した場合はobjのプロパティから取得します

         * パラメータ:

         | 名前 | 型     | 引数   | 説明                                                                                          |
         |------|--------|--------|-----------------------------------------------------------------------------------------------|
         | name | string |        | 完全修飾名 例: Global.Utils.UNDEFINED 等                                                      |
         | obj  | *      | 省略可 | このオブジェクを対象とします 省略した場合グローバルスコープとGlobalオブジェクトを対象とします |
         | def  | *      | 省略可 | 見つからなかった場合に返す値                                                                  |
         

         * 戻り値:   

            * {*}

      * < static > keys(obj) → {Array<string>}  
         オブジェクトの全てのプロパティ名を配列で返します。

         * パラメータ:

         | 名前 | 型 | 説明         |
         |------|----|--------------|
         | obj  | *  | オブジェクト |
         

         * 戻り値:   

            * {Array<string>}

      * < static > objectKeys(obj) → {Array<string>}  
         オブジェクト自身の全てのプロパティ名を配列で返します。  
         ArrayやArrayLike Objectの場合はその要素の添字も含みます  
         組込みオブジェクトの定義済みのプロパティやプロトタイプチェインのプロパティは除きます。

         * パラメータ:

         | 名前 | 型 | 説明         |
         |------|----|--------------|
         | obj  | *  | オブジェクト |
         

         * 戻り値:   

            * {Array<string>}

      * < static > extend(var_args) → {*}  
         <pre>
         指定した最初のオブジェクトに複数のオブジェクトをマージして返します。
         オブジェクトの指定が一つだけの場合はその時のthisに対してマージします
         マージ元で循環参照が有った場合はマージ先でも同様の循環構造を再現します
         マージ元にオブジェクト以外やString,StringBufferオブジェクトを指定した場合は空オブジェクト{}として扱います
         Utils.extend([deep,] [same,] [destination,] source1[, source2[, ...]])
          deep: 省略可 trueならば深いコピー(deep copy) デフォルトはfalse
          same: 省略可 trueならば同名のプロパティは同じ型の場合のみ上書き デフォルトはfalse
          destination: 省略可  マージ先 拡張するオブジェクト 省略した場合はthis
          source1,2...: マージ元 オブジェクト
         </pre>

         * パラメータ:

         | 名前     | 型 | 引数   | 説明 |
         |----------|----|--------|------|
         | var_args | *  | 可変長 |      |
         

         * 戻り値:   

            * {*} : マージしたオブジェクト

         * 使用例:  

            ```
            例1: Utils.extend(destination, source); //destinationにsoucreの内容をコピー
            例2: Utils.extend(true, destination, source, source2); //destinationにsoucreとsourc2の内容をディープコピー
            例3: Utils.extend(source); //Utilsにsourceの内容をコピー
            例4: Obj.extend = Utils.extend;
                 Obj.extend(source); //Objにsourceの内容をコピー
            ```  

      * < static > objCreate(ctorName, proto, prop) → {Object}  
         指定したプロトタイプとプロパティで新しいオブジェクトを生成します

         * パラメータ:

         | 名前     | 型     | 引数   | 説明                                                                                                                                              |
         |----------|--------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
         | ctorName | string |        | 内部で使用するコンストラクタ関数の名前。<br>    DMonkeyではprototypeは同名の関数同士で共有されます。 共有を避けたい場合は一意の名前にしてください |
         | proto    | Object | 省略可 | 新しいオブジェクトのプロトタイプとなるオブジェクト                                                                                                |
         | prop     | Object | 省略可 | このオブジェクトの各プロパティを新しいオブジェクトに追加する                                                                                      |
         

         * 戻り値:   

            * {Object}

      * < static > inherits(childCtor, parentCtor)  
         <pre>
         他のコンストラクタからプロトタイプを継承します。クラスの継承を擬似的に実現させます。
         親のprototypeに constructor プロパティを追加します。 親自身のコンストラクタ関数です。
         子のprototypeに _super プロパティを追加します。 親のコンストラクタ関数です。
         子のprototypeに _base メソッドを追加します。 親メソッドの呼び出しに使用します。
         function _base(selfObj, methodName, var_args)
          selfObj: 呼び出し先でthisとなる値 通常は自身を指定してください
          methodName: 呼び出す親のメソッドの名前
          var_args: 親メソッドに渡す引数
         </pre>

         * パラメータ:

         | 名前       | 型       | 説明                             |
         |------------|----------|----------------------------------|
         | childCtor  | function | 子クラスとなるコンストラクタ関数 |
         | parentCtor | function | 親クラスとなるコンストラクタ関数 |
         

         * 使用例:  

            ```
            function Parent(a){this.a = a;}
            function Child(a){
                //親の呼び出し例
                //例1:
                    this._base(this, 'constructor', a);
                //例2:
                    Utils.call(Parent, this, a);
                //例3:
                    Utils.call(Child.prototype._super, this, a);
                //例4(DMonkey固有の仕様):
                    var super_ = Child.prototype._super;
                    super_(a);
                //例5(DMonkey固有の仕様)
                    Parent(a);
                //駄目な例1:
                    this._super(a);
                //駄目な例2:
                    Child.prototype._super(a);
            }
            Utils.inherits(Child, Parent);
            ```  

      * < static > mixin(dest, src)  
         destオブジェクトにsrcオブジェクトの全てのメンバーをコピーします

         * パラメータ:

         | 名前 | 型     | 説明 |
         |------|--------|------|
         | dest | Object |      |
         | src  | Object |      |
         

      * < static > bind(fn, selfObj, var_args) → {function}  
         thisや引数が束縛された新たな関数を生成して返します

         * パラメータ:

         | 名前     | 型       | 引数   | 説明                                                                                                  |
         |----------|----------|--------|-------------------------------------------------------------------------------------------------------|
         | fn       | function |        | 対象とする関数                                                                                        |
         | selfObj  | Object   |        | 関数内でthisとして使用される値                                                                        |
         | var_args | *        | 可変長 | 関数に渡される引数。 生成された関数を呼び出す時に指定された引数はこれらの後の引数として使用されます。 |
         

         * 戻り値:   

            * {function}

      * < static > loadIni(def, path) → {Object}  
         iniファイルから設定値を読み込みオブジェクトで返します  
         各設定値は適切なプリミティブ値に変換されます  
         pathはiniファイルのパス又はIniオブジェクトを渡してください  
         Iniオブジェクトを渡した場合はそこから設定値を読み込みます  
         defを指定した場合は取得したオプションとdefをマージした新しいオブジェクトを返します

         * パラメータ:

         | 名前 | 型         | 引数   | 既定値              | 説明                                 |
         |------|------------|--------|---------------------|--------------------------------------|
         | def  | Object     | 省略可 |                     | デフォルト値                         |
         | path | string,Ini | 省略可 | Dorothy.userIniPath | iniファイルのパス又はIniオブジェクト |
         

         * 戻り値:   

            * {Object}

      * < static > saveIni(data, path)  
         iniファイルに設定値を保存します  
         dataオブジェクトに存在しないセクションやキーは削除されます  
         pathはiniファイルのパス又はIniオブジェクトを渡してください  
         Iniオブジェクトを渡した場合はそこに設定値を保存します。 Iniオブジェクトの内容は更新されます

         * パラメータ:

         | 名前 | 型         | 引数   | 既定値              | 説明                                          |
         |------|------------|--------|---------------------|-----------------------------------------------|
         | data | Object     |        |                     | iniファイルに保存する設定値を持つオブジェクト |
         | path | string,Ini | 省略可 | Dorothy.userIniPath | iniファイルのパス又はIniオブジェクト          |
         

      * < static > loadOption(def, path, var_args) → {Object}  
         iniファイルまたはJSONファイルから設定値を読み込みます

         * パラメータ:

         | 名前     | 型         | 引数   | 既定値              | 説明                                                         |
         |----------|------------|--------|---------------------|--------------------------------------------------------------|
         | def      | Object     | 省略可 |                     | デフォルト値                                                 |
         | path     | string,Ini | 省略可 | Dorothy.userIniPath | iniファイルのパス又はIniオブジェクト、又はJSONファイルのパス |
         | var_args | *          | 可変長 |                     | JSONファイルの場合にJSON.loadに渡す引数                      |
         

         * 戻り値:   

            * {Object}

      * < static > saveOption(data, path, var_args)  
         iniファイルまたはJSONファイルに設定値を保存します  
         pathはJSONファイルのパス又はiniファイルのパス又はIniオブジェクトを渡してください  
         Iniオブジェクトを渡した場合はそこに設定値を保存します。 Iniオブジェクトの内容は更新されます

         * パラメータ:

         | 名前     | 型         | 引数   | 既定値              | 説明                                                       |
         |----------|------------|--------|---------------------|------------------------------------------------------------|
         | data     | Object     |        |                     | ファイルに保存する設定値を持つオブジェクト                 |
         | path     | string,Ini | 省略可 | Dorothy.userIniPath | JSONファイルのパス又はiniファイルのパス又はIniオブジェクト |
         | var_args | *          | 可変長 |                     | JSONファイルの場合にJSON.saveに渡す引数                    |
         

      * < static > strToDateTime(str) → {number}  
         日時を表す文字列をIrvineで使用されているTDateTimeの数値に変換します

         * パラメータ:

         | 名前 | 型     | 説明                                                  |
         |------|--------|-------------------------------------------------------|
         | str  | string | 「yyyy/mm/dd hh:nn:ss」または「hh:nn:ss」形式の文字列 |
         

         * 戻り値:   

            * {number} : TDateTimeの数値

      * < static > dateTimeToStr(n, formatStr) → {string}  
         Irvineで使用されているTDateTimeの数値を日時を表す文字列に変換します

         * パラメータ:

         | 名前      | 型     | 引数   | 説明                                     |
         |-----------|--------|--------|------------------------------------------|
         | n         | number |        | TDateTimeの数値                          |
         | formatStr | string | 省略可 | Dateオブジェクトによる文字列変換時の書式 |
         

         * 戻り値:   

            * {string} : 日時を表す文字列

      * < static > setFolderData()  
         folderdataが存在しない場合にfolderdataを定義します

      * < static > getScriptVersion(path) → {string|number}  
         指定したスクリプトのバージョンを取得します  
         IrvineとDorothy2のスクリプトに対応しています

         * パラメータ:

         | 名前 | 型     | 説明                 |
         |------|--------|----------------------|
         | path | string | スクリプトのフルパス |
         

         * 戻り値:   

            * {string|number} : スクリプトのバージョン 数値に変換可能な場合は数値それ以外は文字列

      * < static > getSavePath() → {string}  
         実行環境別に適切なアイテムの保存先のパスを取得します  
         相対パスだった場合は絶対パスになるまで順に上位キューフォルダの保存パスと連結させていきます

         * 戻り値:   

            * {string}

      * < static > expandPath(path, base) → {string}  
         pathを実行環境別に適切な保存先の絶対パスに変換します  
         既に絶対パスだった場合は何もしません  
         ただし 'C:\aaa\..\bbb\' のような指定の場合は "C:\bbb\' に変換されます  
         baseを指定した場合はbaseを基準パスとして使用します  
         単純に連結させているだけなので基準パスにファイル名を含ませないで下さい

         * パラメータ:

         | 名前 | 型     | 引数   | 既定値 | 説明         |
         |------|--------|--------|--------|--------------|
         | path | string | 省略可 | ''     | 変換するパス |
         | base | string | 省略可 | ''     | 基準パス     |
         

         * 戻り値:   

            * {string}

      * < static > getQueueFolderPath() → {string}  
         現在のアイテムのIrvineのキューフォルダのパスを取得します

         * 戻り値:   

            * {string}

      * < static > getUserPath() → {string}  
         Dorothy.userPathを取得します Dorothy.userPathが使えないDOA用

         * 戻り値:   

            * {string}

      * < static > getUserIniPath() → {string}  
         Dorothy.userIniPathを取得します Dorothy.userIniPathが使えないDOA用

         * 戻り値:   

            * {string}

      * < static > getVersionDorothy2A() → {number}  
         Dorothy2A.dmsのバージョンを取得します Dorothy2Rの場合はDorothy.rVersionの値を返します

         * 戻り値:   

            * {number}

      * < static > getVersionDorothy2set() → {number}  
         Dorothy2set.dmsのバージョンを取得します Dorothy2Rの場合はDorothy.rVersionの値を返します

         * 戻り値:   

            * {number}

      * < static > getVersionDorothy2ListMenu() → {number}  
         Dorothy2ListMenu.dmsのバージョンを取得します Dorothy2Rの場合はDorothy.rVersionの値を返します

         * 戻り値:   

            * {number}

      * < static > getVersionDOA() → {number}  
         DOA.dmsのバージョンを取得します Dorothy2Rの場合はDorothy.rVersionの値を返します

         * 戻り値:   

            * {number}

      * < static > setDOA_IT()  
         <pre>
         DOAスクリプト用
         DOA.statusをDOA_ITにし、itemのプロパティに適切にDOAの各値を設定します
          DOA.nameが空ではないのなら    item.filename = DOA.name
          DOA.commentが空ではないのなら item.comment += DOA.comment
          DOA.sizeが123.4MB 等の形式の文字列(/^([\d\.]+)([KMG])?(B|Byte)?$/i)ならば
           バイト値に変換して item.filesize に設定します
         </pre>

      * < static > setDOA(itemData)  
         DOAにて不足している各変数やプロパティを設定します DOAスクリプトのmain関数内で毎回呼び出してください

         * パラメータ:

         | 名前     | 型         | 説明                   |
         |----------|------------|------------------------|
         | itemData | IrvineItem | main関数内でのitemData |
         

      * < static > doaItemAdd(url, filename, filesize, comment)  
         DOA画面にアイテムを追加します

         * パラメータ:

         | 名前     | 型            | 引数   | 既定値 | 説明                     |
         |----------|---------------|--------|--------|--------------------------|
         | url      | string        |        |        | アイテムのURL            |
         | filename | string        | 省略可 | ''     | アイテムのファイル名     |
         | filesize | string,number | 省略可 | ''     | アイテムのファイルサイズ |
         | comment  | string        | 省略可 | ''     | アイテムのコメント       |
         

      * < static > doaItemAdd_IT(itemData)  
         DOA画面にアイテムを追加します 追加したアイテムのDOA.statusはDOA_ITになります

         * パラメータ:

         | 名前     | 型                | 説明                                                                     |
         |----------|-------------------|--------------------------------------------------------------------------|
         | itemData | object,IrvineItem | IrvineItemオブジェクトまたはそれと同じ名前のプロパティをもつオブジェクト |
         

      * < static > getCommentOption(key, def) → {string|number|boolean|null|undefined|T}  
         folderdata.Postとitem.commentに設定されたオプションから指定された名前のオプションを取得します  
         オプションの各値は適切なプリミティブ値に変換されます

         * パラメータ:

         | 名前 | 型     | 引数   | 説明                                             |
         |------|--------|--------|--------------------------------------------------|
         | key  | string |        | オプションの名前                                 |
         | def  | T      | 省略可 | 指定されたオプションが存在しなかった場合に返す値 |
         

         * 戻り値:   

            * {string|number|boolean|null|undefined|T}

      * < static > getCommentOptions(def) → {Object}  
         folderdata.Postとitem.commentに設定された全てのオプションを取得します  
         オプションの各値は適切なプリミティブ値に変換されます  
         defを指定した場合は取得したオプションとdefをマージした新しいオブジェクトを返します

         * パラメータ:

         | 名前 | 型     | 引数   | 説明         |
         |------|--------|--------|--------------|
         | def  | Object | 省略可 | デフォルト値 |
         

         * 戻り値:   

            * {Object}

      * < static > setCommentOption(key, value)  
         item.commentにkey=value;形式のオプションを設定します  
         同名のオプションが既に設定されている場合は指定された値で上書きします

         * パラメータ:

         | 名前  | 型     | 説明             |
         |-------|--------|------------------|
         | key   | string | オプションの名前 |
         | value | *      | オプションの値   |
         

      * < static > redefineDorothy()  
         環境別の差異がなるべく少なくなる様にDorothyの関数等を再定義します  
         DOAやDorothy2AやDorothy2set等の環境別に存在したりしなかったりするプロパティや関数等を  
         なるべく全ての環境で使用できるようにします

      * < static > checkVersion()  
         Dorothyの各実行環境で古いバージョンが使用されていないかチェックします  
         古いバージョンが使用されていた場合はエラーメッセージを表示してスクリプトを終了します

変更履歴:
=========

* 2016/02/14  version 1.5
   .objectKeys(), .setCommentOption() を追加

* 2016/02/04  version 1.4
   .setDOA(), .doaItemAdd(), .doaItemAdd_IT() を追加
   .redefineDorothy()にてDOAの場合に.setDOA()を実行するようにした

* 2016/01/26  version 1.3
   .extractPath(), .has(), .saveOption() を追加

* 2016/01/18  version 1.2  
   isDorothy2setListをisDorothy2ListMenuに変更。
   .getVersionDorothy2ListMenu()を追加。
   .redefineDorothyを更新 urlinfo headers folderdataの定義も追加。
   .checkVersion()を追加 バージョンチェックを行う様にした。

* 2015/12/12  version 1.1  
   loadIni(), saveIni(), loadOption() exxpandPath() メソッドを新規追加。  
   call(), apply()にてエラー処理を追加。 

* 2015/12/03  version 1.0  
   新規作成  
   DorothyEx.dmsのほぼ全ての機能もこちらに統合した  

