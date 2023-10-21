# 39jaiio
Version estatica de 39jaiio.sadio.org.ar

Obtenida con: 
```
wget -N --mirror --adjust-extension --page-requisites --no-parent --convert-links --wait=2 -e robots=off --no-host-directories --timeout=10 --tries=3 --output-file=wget_log.txt https://39jaiio.sadio.org.ar
```

Fue necesario cambiar las extensions .js?z por js, y .css?z por css con algo como:

```
find . -type f -name "*.js?z" -exec bash -c 'mv "$1" "${1%.js?z}.js"' _ {} \;
```

Y luego reemplazar en todos los archivos .js?z, por .js, .css?z por .css, .js%3Fz por .js, y http:// por https://
