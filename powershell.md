### tail -f

Get-Content -Path hogehoge.log -Tail 10 -Wait

### ファイルの中身の検索
Select-String -path "検索対象" -pattern "検索したい単語"
Select-String -path *.txt -pattern "the"
