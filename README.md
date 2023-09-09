# rust-rest-api

## データベース

### データベース接続
```
docker compose up -d
docker compose exec postgres bash

psql -U postgres
```

### 初期データ挿入
```bash
CREATE DATABASE rust_rest_api;
\c rust_rest_api
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR NOT NULL,
    email VARCHAR NOT NULL
);
INSERT INTO users (name, email) VALUES ('John', 'sampleuser@email.com');
```

## web apiサーバ立ち上げ
```bash
cargo run
```

http://localhost:8080/

