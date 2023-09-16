# works
### add index
```
$ docker exec -it webapp-mysql-1 /bin/bash
$ mysql -u root -p
$ use isuconp;
$ alter table comments add index post_id_idx (post_id, created_at desc);
```

### config worker processes

### analyze with alp
```
$ alp json \
    --sort sum -r \
    -m "/posts/[0-9]+,/@\w+,/image/\d+" \
    -o count,method,uri,min,avg,max,sum \
    < logs/nginx/access.log
```

### publish static files by nginx
add below under server directive
```
location ~ ^/(favicon\.ico|css/|js/|img/) {
    root /public/;
    expires 1d;
}
```