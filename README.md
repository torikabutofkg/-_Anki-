MM出版のクエバンのpdfからAnkiに取り込むコードについて作成

#ライブラリのインストール　及び　#グーグルドライブと連携は各自のGoogle Colabの環境で行ってください。（多分貼ってあるコード通りで行けるはず９


![image](https://github.com/user-attachments/assets/547db840-942f-4ea1-bace-d119287aa91e)



pdfの読み込み→csvファイルの出力は、左上のファイルのアップロードから、Anki化したいクエバンのpdfファイルをアップロードした後に、右クリックでpassをコピーした後

上部の　
pdf_path = "/content/1A.pdf"と、
下部の
# CSVファイルに保存
output_file = os.path.join(folder_path, "1A.csv")

に貼り付け及び書き出したい名前で書き直す。（1A.pdf,1A.csv　は例）

このコードを行うと、指定したディレクトリにpdfから抽出されたcsvファイル[問題、問題ID、解答、画像]と、問題に画像が存在する場合、その画像ファイルが同時に入っているはず。（画像はzipファイル）
それぞれダウンロードして、画像ファイルはAnki→ファイル→プロファイル→バックアップを開くで出てくるディレクトリの一つ上位のユーザー１の直下のcollection.mediaに貼り付ける。（アクセスが面倒なのでショートカットを作っておくと良い）
ダウンロードしたcsvファイルは、Anki→ファイル→インポートでファイル選択。その後、”フィールド内でHTMLを使う”にチェックをいれるのを忘れずに！（画像表示の都合上）
また同時にフィールドの割り当てに関しても確認しておく。
インポートボタンを押すとインポート完了。
