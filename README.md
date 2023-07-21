# Setup_KIOSK
Windows PC をKIOSK 端末としてセットアップする方法のメモ。  
  
お品書き  
## ローカルアカウントでセットアップ
## OS起動時は自動ログイン
## OS起動時にChromeを最大化（または全画面表示）で表示
## Chrome を一定間隔で自動リロード
## Chromeリモートデスクトップで遠隔操作
## タイマーでPCを自動電源ON
## タスクスケジューラで自動シャットダウン

## ローカルアカウントでセットアップ
1. 「個人」「会社や学校」の「学校」
2. Microsoft アカウントでは「dummy@example.com」などパスワードもデタラメで進める
3. エラーになり、ローカルアカウントの設定になる。
4. （前段で「BypassNRO.cmd」を実行？）
## OS起動時は自動ログイン
1. 「regedit」で「HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon」を開く
2. [AutoAdminLogon]が[0]であれば、[1]にする。
3. [DefaultUserName]を確認。
4. [DefaultPassword]がなければ[文字列値] で作成。
## OS起動時にChromeを最大化（または全画面表示）で表示
1. 「Winキー」+「R」で「ファイル名を指定して実行」を開き、「shell:startup」を実行。
2. 「スタートアップ」フォルダにChrome のショートカットをコピーして置く。
3. 「設定->アプリ->スタートアップ」の設定も確認。
## Chrome を一定間隔で自動リロード
1. 機能拡張をインストールする。（例）：「Auto Refresh Plus」
## Chromeリモートデスクトップで遠隔操作
1. 機能拡張をインストールする。（例）：「Chrome Remote Desktop」
## タイマーでPCを自動電源ON
1. BIOS(UEFI) のRTC で自動起動を設定
## タスクスケジューラで自動シャットダウン
1. 「タスクスケジューラ」で