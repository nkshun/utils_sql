出力結果を、jsonファイルに保存する
```
mysql -h <host name> -u <user name> -p <database name> --execute="sql" >test.json
```
[参考](https://qiita.com/ecoyamas/items/dc7089b50f792a18e95a)

select結果を、json形式で出力する
```
select JSON_ARRAYAGG(JSON_OBJECT('data01', data01, 'data02', data02, 'data03', data03, 'data04', data04, 'data05', data05, 'data06', data06, 'data07', data07, 'data08', data08, 'data09', data09, 'data10', data10, 'created_at', created_at, 'updated_at', updated_at)) from data_pool where created_at > '2021-08-18 23:00:00'
```

[参考](https://www.it-mure.jp.net/ja/mysql/mysql%E3%81%A7%E7%B5%90%E6%9E%9C%E3%83%86%E3%83%BC%E3%83%96%E3%83%AB%E3%82%92json%E9%85%8D%E5%88%97%E3%81%AB%E5%A4%89%E6%8F%9B%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95/830599574/)