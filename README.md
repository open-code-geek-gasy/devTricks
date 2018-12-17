# devTricks

**Angular Deployement**

1 - Apache

**Rehefa manao déployement angular amin'ny apache ianao dia asio an'ity .htaccess ity ao amin'ny racine mba tsy ho lasa 404 rehefa reloadena ilay page**

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
```
location / {
    try_files $uri $uri/ /index.html?$query_string;
}
```

3 - Server IIS

```
<?xml version="1.0" encoding="UTF-8"?> 
<configuration> 
    <system.webServer> 
        <rewrite> 
            <rules> 
                <rule name="angularjs routes" stopProcessing="true"> 
                    <match url=".*" /> 
                        <conditions logicalGrouping="MatchAll"> 
                            <add input="{REQUEST_FILENAME}" matchType="IsFile" negate="true" /> 
                            <add input="{REQUEST_FILENAME}" matchType="IsDirectory" negate="true" /> 
                        </conditions> 
                    <action type="Rewrite" url="/egs/" /> 
                </rule> 
            </rules> 
        </rewrite> 
    </system.webServer> 
</configuration>
```
