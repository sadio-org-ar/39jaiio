# 39jaiio
Version estatica de 39jaiio.sadio.org.ar

Obtenida con: 
```
wget -N --mirror --adjust-extension --page-requisites --no-parent --convert-links --wait=2 -e robots=off --no-host-directories --timeout=10 --tries=3 --output-file=wget_log.txt https://39jaiio.sadio.org.ar
```

Fue necesario cambiar las extensions .js?z por js con:

```
find . -type f -name "*.js?z" -exec bash -c 'mv "$1" "${1%.js?z}.js"' _ {} \;
find . -type f -exec sed -i 's/\.js?z/\.js/g' {} +
```

