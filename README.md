# Wordpress?

#### Começando com wordpress
- [Como instalar o wordpress localmente](https://www.themeum.com/install-wordpress-localhost/)

#### Desbravando o wordpress
- [Criar um tema só seu dentro do diretório](https://codex.wordpress.org/Theme_Development) 
`wp-content/themes`
- [Basic templates - wordpress tem métodos pré definidos, exemplo:](https://codex.wordpress.org/Theme_Development#Basic_Templates)
`get_header()`
- [Após criar alguns posts dentro do painel admin do wordpress, precisamos mostrar os post no site. Então usamos o The Loop como:](https://codex.wordpress.org/The_Loop)
`while(have_posts())`

#### Alguns métodos que vão ser encontrados e usados
- [`get_template_directory_uri()`](https://developer.wordpress.org/reference/functions/get_template_directory_uri/). Ao invés de você usar `wordpress/wp-content/themes/malura/style.css`, você chama esse método e consegue acessar apenas com: `href="<?= get_template_directory_uri(); ?>/style.css"`

