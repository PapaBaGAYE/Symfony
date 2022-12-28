# Symfony

**Creer un projet symfony**
```
composer create-project symfony/skeleton:"6.2.*" projet_1
```

**Installation de toutes les dépendances**
```
composer require webapp
```

**creer notre excetuble pour le server**
```
#!/usr/bin/env php
<?php

$port = isset($argv[1]) ? $argv[1] : 80;

exec("php -S localhost:$port -t public");
```

**Lancer l'application**
```
php .\bin\server 8000
```

**Creer un projet symfony autrement**
```
symfony new projet_2 --version="6.1.*"
```
