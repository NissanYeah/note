## 如何處理MySQL無法正常匯入CSV檔案的問題

1. 如果匯入csv時出現 `can't analyze file,please try to change encoding type.if that doesn't help,maybe this file is not:csv,or the file is empty.`，可能是因為資料不是標準的utf-8。如果資料是來自於excel，因為它匯出的資料不是標準的utf-8，所以可以先用`number`打開csv檔案再另存成utf-8

2. 如果匯入csv時出現，無法直接使用existing table，就可以先匯到新的table，然後再用以下語法合併表格

```sql
INSERT IGNORE INTO myschema.myTable    -- ignore表示不跑出錯誤，即使有重複

SELECT * FROM myschema.newTable
```