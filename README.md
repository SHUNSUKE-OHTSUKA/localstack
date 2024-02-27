# localstack

## 概要

AWSリソースをlocalstack環境で開発するためのリポジトリ

## localstack起動コマンド

```
docker compose up -d
```

## localstack操作コマンド

### ホストOSで実行

* localstackに対してterraformを実行する

    ```
    cd ./terraform
    terraform init
    terraform plan
    terraform apply
    ```

    ※ ` Warning: AWS account ID not found for provider`というメッセージが表示されるが問題ない。

* localstackコンテナに入る

    ```
    docker-compose exec localstack /bin/bash
    ```

### localstackコンテナ内で実行

* aws cliを実行する(awslocal)

    ```
    # s3バケットのリストを出力
    awslocal s3 ls
    ```


