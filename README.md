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

**Creer une application web tranditionnelle symfony**
```
symfony new projet_2 --version="6.1.*" --webapp
```

```
symfony new projet_2 --version="6.1.*" --full
```

**Lancer l'application**
```
symfony serve
```

```
symfony server:start
```

<hr>

```
composer init
```

## TWIG

**Ajouter twig au projet**
```
composer require twig/twig
```

```
<?php

use App\Kernel;
use Twig\Loader\FileSystemLoader;

// require_once dirname(__DIR__).'/vendor/autoload_runtime.php';
require_once dirname(__DIR__).'/vendor/autoload.php';

$loader = new FileSystemLoader(dirname(__DIR__).'/templates');
$twig = new \Twig\Environment($loader, [
            // "cache" => dirname(__DIR__)."/var/cache",
        ]);

$users = ['Pape Aly', "Mai", "Astou", "Messi", "Neymar"];

echo $twig->render(
    'index.html.twig',
    ['titre' => 'Twig', "users" => $users]
    );
```

## DOCTRINE ORM

**Installation de doctrine**

```
composer require symfony/orm-pack
```

```
composer require --dev symfony/maker-bundle
```

**Creer une base de données**

```
php bin/console doctrine:database:create
```

**Creer une entité ( table )**

```
 php bin/console make:entity
 ```
