# devTricks

**Angular Deployement**

1 - Apache

**Rehefa manao déployement angular amin'ny apache ianao dia asio an'ity .htaccess ity ao amin'ny racine mba tsy ho lasa 404**

```
<IfModule mod_rewrite.c>
    RewriteEngine on

    # Don't rewrite files or directories
    RewriteCond %{REQUEST_FILENAME} -f [OR]
    RewriteCond %{REQUEST_FILENAME} -d
    RewriteRule ^ - [L]

    # Rewrite everything else to index.html
    # to allow html5 state links
    RewriteRule ^ index.html [L]
</IfModule>

```

2 - Nginx

