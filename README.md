# Hosting

My server installation recipes.

Inspired from https://github.com/tomMoulard/make-my-server

```bash
docker-compose ()
{
    /usr/local/bin/docker-compose $(find -name 'docker-compose*.yml' -type f -printf '%p\t%d\n'  2>/dev/null | sort -n -k2 | cut -f 1 | awk '{print "-f "$0}') $@
}
```  
