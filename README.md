# eita e agora, é Wordpress?

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

- [`the_post_thumbnail();`](https://developer.wordpress.org/reference/functions/the_post_thumbnail/) Serve para chamar o thumbnail na página, mas não tenho certeza se na versão 5 precisamos disso. 

- [`the_permalink();`](https://developer.wordpress.org/reference/functions/the_permalink/) Chamando esse método dentro de um link, faz o post criar um link para ser redirecionado. `<a href="<?php the_permalink(); ?>">`


#### Alguns métodos sobre customização do painel ADMIN
- [Os ícones para customização do painel ADMIN](https://developer.wordpress.org/resource/dashicons/#calendar-alt)

- O método [`register_post_type()`](https://developer.wordpress.org/reference/functions/register_post_type/) permite você criar tipos posts para o tipo que você precisa, exemplo: adiconar CDs, ao invés de posts. Tem dois args: o 1º é um apelido e o 2º é um array de configurações.

- o método [`add_action('init', 'metodo_para_chamar_quando_chegar_no_init')`](https://developer.wordpress.org/reference/functions/add_action/) Quando você cria funções para organizar e isolar o código, para chamar essas novas funções, usamos esse método. O primeiro arg é o quando executar sua função e o segundo arg é chamada da função. 

- [`loop = $new WP_Query( $args );`](https://developer.wordpress.org/reference/classes/wp_query/) Usando esse método, conseguimos dizer de onde (tabela do banco de dados) devemos buscar os dados para aquele loop.


#### Entender o que são Templates

| Template | O que ler? |
| --- | --- |
| `primeiro, o que são templates` | [leitura 1](https://wpapprentice.com/blog/wordpress-theme-vs-template/)|
| `theme X templates`| são duas coisas diferentes |
| `theme`| theme é o design: fonts, colors... |
| `template` | template é mais a estrutura de uma página |
|`existe uma hirarquia de templates`| [Leitura 1](https://developer.wordpress.org/themes/basics/template-hierarchy/) |

|E os templates| links|
| --- | --- | 
| `single.php` | ... |


