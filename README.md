>  # Desenvolvimento de Atividade e Documentação Passo a Passo para Autenticação em Aplicações Laravel e PHP
#
>  ##  Introdução
*  ### Esta atividade visa aprofundar e consolidar o conhecimento adquirido até o momento no domínio do processo de login em aplicações web, especialmente utilizando as tecnologias Laravel e PHP. O objetivo principal é fornecer uma oportunidade prática para os participantes desenvolverem habilidades na criação de guias de usuário detalhados e na elaboração de mapas da aplicação, contribuindo assim para uma compreensão mais holística e efetiva do desenvolvimento de software.
#
> ## Objetivos Específicos:

* #### 1° Consolidação do Conhecimento: Reforçar e aplicar os conceitos aprendidos sobre autenticação em sistemas web, utilizando as melhores práticas recomendadas pela comunidade Laravel e PHP.

* #### 2° Desenvolvimento de Habilidades Práticas: Proporcionar aos participantes a oportunidade de traduzir teoria em prática, fortalecendo suas habilidades na criação de guias de usuário detalhados, essenciais para facilitar a compreensão e utilização da aplicação.

* #### 3° Utilização de Ferramentas Profissionais: Promover o uso eficiente de ferramentas padrão da indústria, como o Microsoft Word, para a elaboração de documentos técnicos. Isso inclui a criação de um guia passo a passo claro e conciso.

* #### 4° Mapeamento da Aplicação: Incentivar a prática na criação de mapas da aplicação, destacando a estrutura e os fluxos de dados relacionados ao processo de autenticação. Esse exercício visa aprimorar a capacidade dos participantes de visualizar e compreender a arquitetura de uma aplicação de maneira abrangente.

---


> ## Download e instalações de ferramentas utilizadas.:

## Composer       <a href="https://getcomposer.org/download/"><img src="assets/composer.svg" width = "20" alt="Link â pagina de download Composer"></a>

* ### Download Composer (versão 2.6.6) para todos os sistemas operacionais e também via código (php).: 
>  <a href="https://getcomposer.org/download/"><img src="assets/pagComposer.png" alt="Pagina de Download Virtual Box"></a>

* ### Link de download direto à pagina.:

   > <a href="https://getcomposer.org/download/"><img src="assets/composer.svg" width = "50" alt="Link â pagina de download Composer"></a>

* ### Instalação do mesmo:

* #### Após a execução do composer setup

 <img src="assets/Composer.png" width = "300" alt="Install Composer">

#### "Install for me only". 
---

 <img src="assets/delComposer.png" width = "300" alt="Install Composer">

#### Aplique a opção de developer mode 

 <img src="assets/delApli.png" width = "400" alt="Install Composer">

#### A partir dai pode continuar aplicando next para as proximas perguntas.

 


---
## Laravel <a href="https://laravel.com/docs/8.x"><img src="assets/laravel.svg" width= "20" alt="Link â pagina de download Ubuntu Server 22.04"></a>
* ### Documentação Laravel para duvidas e obtenção do mesmo. OBS(Versão utilizada: 8.x)
> <a href="https://laravel.com/docs/8.x"><img src="assets/laravelDoc.png" alt="Tutorial install Laravel 8.X"></a>
* ### Link download direto à pagina.:

    > <a href="https://laravel.com/docs/8.x"><img src="assets/laravel.svg" width= "50" alt="Link â pagina de download Ubuntu Server 22.04"></a>


---

## XAMPP (Banco de dados MySQL) 

* ### XAMPP. Utilizamos o XAMPP para o acesso ao banco de dados MySQL de forma mais rapida

> <a href="https://www.apachefriends.org/pt_br/index.html"><img src="assets/pagXamp.png" alt="Tutorial install Laravel 8.X"></a>

* ### Link download direto à pagina.:

    > <a href="https://laravel.com/docs/8.x"><img src="assets/xampp.svg" width= "40" alt="Link â pagina de download Ubuntu Server 22.04"></a>
---

> # Criação Projeto

## Passo a passo e utilização das ferramentas.:

* ### Primeiro iniciamos o projeto com o framework laravel utilizando o composer com a seguinte linha de código:

#### 1° Abra o terminal.

#### 2° Navegue até o diretório onde deseja criar seu novo projeto Laravel.

#### 3° Execute o seguinte comando para criar um novo projeto Laravel:

```
composer create-project --prefer-dist laravel/laravel nome-do-projeto
```

#### Após a criação do projeto laravel via composer, certifique-se que esta dentro da pasta do projeto, caso não saiba digiteo seguinte comando:

```
ls
```

#### Caso não esteja, digite o seguinte:

```
cd (nome do projeto)
```
---

> # Controller

### Após a criação do projeto, vira os passos para criar o sistema de login dentro do projeto. Comece criando o controller.

* #### O que é um controller
#### No Laravel, um controller é uma classe PHP responsável por manipular as requisições HTTP e controlar o fluxo de uma aplicação. Ele age como uma ponte entre as rotas definidas na aplicação e a lógica de negócios, facilitando a organização e a estruturação do código.

* #### Função
#### A principal função de um controller é receber uma requisição HTTP, processá-la e, em seguida, retornar uma resposta. As ações ou métodos dentro de um controller representam diferentes funcionalidades da aplicação.

* #### O que iremos fazer com os controllers
#### Em nosos projeto utilizamos os controllers para diversas funções, utilizamos para setar uma pagina (blade.php), criamos uma function|função com um nome e chamos a mesma nas rotas, após a rota ser chamada, a função possui uma view e esta view se aponta para a pagina (blade.php)

* #### Exemplo:

<img src="assets/Exmplo view.png" width= "300" alt="Link â pagina de download Ubuntu Server 22.04">

#### No exemplo acima, possuo um controller com nome de HomeController, este controller possui uma função e esta função retorna uma view e esta view aponta para um caminho que se encontra esta pagina.

* #### Criação do controller. OBS Sugiro que o nome do controller seja LoginController:

```
php artisan make:controller (Nome do controller).
```

#### Após a criação e a configuração do controller que se encontra dentro da pasta App\Http\Controllers

#### Crie uma view que retorne uma pagina e esta pagina peço que seja construida um formulario. Esta pagina deve ser criada dentro resources/views. Vai do seu interesse de criar uma pasta dentro dela ou somente criar o arquivo a dentro, porém, dentro da function do controller deve apenas apontar o nome do arquivo exemplo.:


<img src="assets/viewLogin.png" width= "400" alt="Link â pagina de download Ubuntu Server 22.04">


---

<img src="assets/route.png" width= "800" alt="Link â pagina de download Ubuntu Server 22.04">

#### Neste exemplo esse é um arquivo de rotas chamado web.php, ele se encontra dentro da pasta "routes". Como dito antes, esta é um rota que retorna uma pagina por conta da função chamada index dentro do HomeController, esta função aponta para uma view e essa view retorna um caminho onde se encontra a pagina

<img src="assets/caminhoRout.png" width= "300" alt="Link â pagina de download Ubuntu Server 22.04">

#### Aqui é para onde a view aponta e aqui também se encontra o arquivo "home".

#### Agora ligando|ativando o servidor do laravel no terminal com o seguinte comando

```
php artisan serve
```

#### O terminal ira retornar um ip de loop com uma porta

<img src="assets/servelaravel.png" width= "700" alt="Link â pagina de download Ubuntu Server 22.04">

#### Seguindo este ip de loop seremos redirecionados a pagina da view
---

> # MySQL

## Passos para realizar o sistema de login

* #### Para construir e usarmos o login, iremos realiza-lo com usuarios dentro do banco de dados, para isso utilizaremos o XAMPP que possui o banco de dados MySQL, após abri-lo e ligar o banco de dados MySQL

* #### Obviamente devemos criar uma tabela para usuarios e preenche-las para o login, caso ocorra alguma duvida de como se deve fazer isso, deixarei uma documentação sobre o MySQL e como acessar o banco de dados local

#### Deixarei uma extensão do Visual Studio Code para realizar a conexão com o banco de dados e criar suas tabelas e diversas outras funções dentro do MySQL.: 
> ### Database Client JDBC

#### Caso não goste, também deixarei a obtenção de um editor de código voltado para o MySQL
> ### MySQL Workbench

* ### Link download direto à pagina.:

    > <a href="https://dev.mysql.com/downloads/workbench/"><img src="assets/mysql-workbench.svg" width= "40" alt="Link à pagina de download WorkBench"></a>

### Documentação para criação do banco, tabelas e tuplas (inserts).:

* ### Link documentação MySQL.:

    > <a href="https://www.w3schools.com/mysql/mysql_create_table.asp"><img src="assets/mysql-workbench.svg" width= "40" alt="Link de documentação e aulas MySQL"></a>
    #### Junto de passo a passo e aulas


#### Após configurar suas tabelas, campos e tuplas, precisaremos de uma pagina (blade.php) que possua um formulario para realizar este login.

> # Formulario

### Para o meu login estarei utilizando este seguinte formulario:

<img src="assets/pagLogin.png" width= "" alt="Link de documentação e aulas MySQL">



#### Após a criação e configuração do formulario. OBS: Preciso que o "name" das inputs sejam setados

<img src="assets/names.png" width= "" alt="Link de documentação e aulas MySQL">

---

>  # Resumo

#### Perceba que o formulario possui uma ação, esta ação sera ativada ao clicar no botão onde há "submit" que aponta para uma rota dentro de web.php, esta rota sera criada dentro do LoginController com uma função|function e dentro da mesma sera criado a autenticação dos valores dentro das inputs e sera comparado com os dados dentro do banco de dados, caso ambas informações sejam iguais, a pessoa realizará o login.

---

> # Criação Model

### Aqui damos inicio aos passos finais. Agora vem a criação dos models para realizar a representação das tabelas dentro do banco de dados.

#### Na aplicação de login apresentada iremos criar um login tanto para os alunos da academia quanto para os funcionarios da mesma, sendo assim devemos possuir 2 tabelas, uma para alunos e outra para funcionario e para realizar o login de ambos, iremos utilizar a tabela de usuarios onde possui as informações para login das mesmas

> # Tabelas

## Tabela Aluno

> <img src="assets/tblAluno.png" width= "" alt="Link de documentação e aulas MySQL">

---

## Tabela Funcionarios

> <img src="assets/tblFuncionario.png" width= "" alt="Link de documentação e aulas MySQL">

## Tabela Usuario

> <img src="assets/tblUsuario.png" width= "" alt="Link de documentação e aulas MySQL">


### Demostrado então as tabelas iremos aos models. Para a criação dos models segue o comando:

```
php artisan make:model (Nome do model)
```

### Crie um para cada tabela (Aluno, Funcionario e Usuario). Os models serão encontrados em App\Models.

> # Configuração de Model



---
## Conclusão