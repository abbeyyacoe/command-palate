# Removing .DS_Store

```
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
```

# .htaccess starter pack

```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)\.html$ /$1 [L,R=301] 
```