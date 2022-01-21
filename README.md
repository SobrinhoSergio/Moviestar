# Moviestar

 Este projeto é uma rede social quase completa. O objeto de estudo aqui é a conexão de PHP + BD, PHP e a WEB, Regras de negócio complexas e múltiplas integrações. Este projeto se trata da seção 19 do curso PHP: Do zero a Maestria

 ## Como está o projeto?

 O projeto está totalmente funcional e responsivo. Caso queira experimentar, basta baixar e executar (Seguindo as instruções da Seção: Rodar o projeto). É possível se cadastrar, adicionar filmes, adicionar reviews entre otras funções. Conta com diversas telas, e muita programação e lógica. Conta também com autenticação de usuário, codificação de senha e etc. Além disso, o projeto está totalmente responsivo

### Imagens Projeto

Home:
![Home](.github/assets/home.png)

Login/Registro:
![Login_Registro](.github/assets/login_registro.png)

Usuário:
![Usuario](.github/assets/tela_usuario.png)

Dashboard:
![Dashboard](.github/assets/dashboard.png)

## Vídeo do projeto 

<video autoplay>
  <source src=".github/assets/video.mp4" type="video/mp4">
</video>

## Banco de dados

```sql	
    - CREATE DATABASE moviestar;
        - CREATE TABLE users(
            id INT(11) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
            name VARCHAR(100),
            lastname VARCHAR(200),
            email VARCHAR(200),
            password VARCHAR(200),
            image VARCHAR(200),
            token VARCHAR(200),
            bio TEXT
        );
        - CREATE TABLE movies(
            id INT(11) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
            title VARCHAR(100),
            description TEXT,
            image VARCHAR(200),
            trailer VARCHAR(150),
            category VARCHAR(50),
            length VARCHAR(50),
            users_id INT(11) UNSIGNED,
            FOREIGN KEY (users_id) REFERENCES users(id)
        );
        - CREATE TABLE reviews(
            id INT(11) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
            rating INT,
            review TEXT,
            users_id INT(11) UNSIGNED,
            movies_id INT(11) UNSIGNED,
            FOREIGN KEY (users_id) REFERENCES users(id),
            FOREIGN KEY (movies_id) REFERENCES movies(id)
        );  
```

## Rodar o projeto

Caso queira rodar o projeto em sua máquina local será necessário o Apache e o Banco de Dados Mysql. Recomendo a instalação do **Laragon**, que é um pacote de instalaçaões que traz esses 2 serviços. Basta jogar o projeto na pasta *www* e colocar o banco de dados base disponível na pasta Database no servidor local (Pode-se fazer isso pelo PHPMyadmin). OBS: Talvez seja necessário mudar o arquivo connect.php deixando a variável password vazia.

```php
   $pass = "";
```

 ## Stack
 As tecnologias usadas nesse projeto são:
 * HTML
 * CSS
 * PHP
 * Bootstrap
 * Bootstrap Icons
 * MySQL
 
 Acesse o repositório do curso citado clicando [Aqui](https://github.com/JoaopedroSassi/PHP_Zero_Maestria-HC)