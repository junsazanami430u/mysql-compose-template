# このリポジトリについて
- mysqlコンテナを立ち上げるのに使えるテンプレート

以下の形式で`.envrc`ファイルを作成して、  
`direnv allow`をしてからdocker composeの操作で立ち上げてください
```.env:.envrc
export MYSQL_DATABASE=""
export MYSQL_PASSWORD=""
export MYSQL_ROOT_PASSWORD=""
export MYSQL_USER=""
export PMA_HOSTS=""
export MYSQL_URL="mysql://root:${MYSQL_ROOT_PASSWORD}@localhost:3306/${MYSQL_DATABASE}"
export MYSQL_DSN="root:${MYSQL_ROOT_PASSWORD}@tcp(localhost:3306)/${MYSQL_DATABASE}?parseTime=true"
export MYSQL_TEST_DSN="root:${MYSQL_ROOT_PASSWORD}@tcp(localhost:3306)/${MYSQL_DATABASE}?parseTime=true"
```