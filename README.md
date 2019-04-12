# universal-copy-tool

Like `cp` but for anything

## Copy files to and from anywhere

### Locally

```shell
ucpt /some/file/here  /copy/it/over/here/instead
```

### Locally to some machine

```shell
ucpt /some/file/here  ssh://user@machine:/home/user/file/here
```

### Remotely

```shell
ucpt scp://user@machine:/home/user/file  ssh://another_user@another_machine:/home/user/file/here
```

### You can also copy files to and from Object Store Services

```shell
ucpt ssh://user@machine:/home/user/file/here s3://bucket/name/of/object
```

### Or from service to service

```shell
ucpt  s3://bucket/name/of/object gs://bucket/name/of/object
```

### Even databases

```shell
ucpt  postgresql://user@127.0.0.1:db.schema.table mongodb://user@host.com:27017/database/collection/
ucpt  redis://127.0.0.1 mssql://user@host.com:1433.database.table
ucpt  /home/user/* bigtable://google-project-id/column-family/
```

## Mix and match

```shell
ucpt https://wesite.com/somepage.html bigquery://google-project-id.dataset.table
ucpt cosmos://user@password:acct.documents.azure.com:1025/database https-post://user@password:/some/rest/service?q=v
```

## How it works
