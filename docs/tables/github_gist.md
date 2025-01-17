# Table: github_gist

GitHub Gist is a simple way to share snippets and pastes with others. You can query **ANY** gist that you have access to by specifying its `id` explicitly in the where clause with `where id =`. You must specify the `id` in a where clause or join key to use this table.

To list the gists that **you own**, use the `github_my_gist` table.

## Examples

### Get details about ANY public gist (by id)

```sql
select
  *
from
  github_gist
where
  id='633175';
```

### Get file details about ANY public gist (by id)

```sql
select
  id,
  jsonb_pretty(files)
from
  github_gist
where
  id = 'e85a3d8e7a23c247f672aaf95b6c3da9';
```
