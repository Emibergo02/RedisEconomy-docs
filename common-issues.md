# Common issues

During migration duplicated uuids will result as `<uuid>-Unknown` inside the baltop

If you have hanging uuid-Unknown on Redis, use \
<mark style="color:orange;">`/purge-balance (.{36}-Unknown) onlyNameUUID`</mark>\
to clear the redis data
