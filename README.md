# Desenvolvimento de Chat em Tempo Real — Laravel + WebSocket

## 📌 Sobre o projeto

Este projeto foi desenvolvido para a atividade **Desenvolvimento de Chat – WebSocket**.

O objetivo é desenvolver um sistema de comunicação em tempo real utilizando **Laravel**, **Chatify** e **Pusher**, permitindo que dois usuários autenticados realizem uma conversa e recebam mensagens sem precisar atualizar a página.

A comunicação em tempo real é realizada por meio da integração do Chatify com o Pusher.

---

## 🎯 Objetivo da atividade

Desenvolver um chat web em Laravel utilizando comunicação em tempo real, permitindo:

* Cadastro de usuários;
* Login e autenticação;
* Comunicação entre usuários;
* Envio de mensagens;
* Recebimento de mensagens em tempo real;
* Integração com Pusher;
* Utilização de WebSocket para comunicação em tempo real;
* Persistência das mensagens no banco de dados.

---

## 🛠️ Tecnologias utilizadas

* **PHP**
* **Laravel**
* **Laravel Breeze**
* **Chatify**
* **Pusher**
* **WebSocket**
* **MySQL/MariaDB**
* **XAMPP**
* **Node.js**
* **NPM**
* **Vite**
* **HTML**
* **CSS**
* **JavaScript**

---

# 🚀 Desenvolvimento do projeto

## 1. Criação do projeto Laravel

O projeto foi criado dentro da pasta `C:\xampp\htdocs`.

Comando utilizado:

```bash
composer create-project laravel/laravel chatLaravelPusher
```

Após a criação, o projeto foi acessado pelo terminal:

```bash
cd C:\xampp\htdocs\chatLaravelPusher
```

---

## 2. Configuração do banco de dados

Foi criado o banco de dados:

```text
chatweb3ams
```

A conexão com o banco foi configurada no arquivo `.env`.

As principais informações utilizadas foram:

```env
DB_CONNECTION=mysql
DB_DATABASE=chatweb3ams
```

As credenciais do banco e as chaves privadas utilizadas no projeto não são disponibilizadas neste repositório.

---

## 3. Instalação do Laravel Breeze

O Laravel Breeze foi utilizado para fornecer o sistema de autenticação dos usuários.

Instalação:

```bash
composer require laravel/breeze --dev
```

Depois:

```bash
php artisan breeze:install
```

E as tabelas foram criadas com:

```bash
php artisan migrate
```

Com isso, o projeto passou a possuir cadastro e autenticação de usuários.

---

## 4. Instalação e configuração do Chatify

O Chatify foi utilizado para implementar a interface e a estrutura principal do sistema de mensagens.

Instalação:

```bash
composer require munafio/chatify
```

Depois:

```bash
php artisan chatify:install
```

E novamente foram executadas as migrações:

```bash
php artisan migrate
```

O Chatify criou as estruturas necessárias para o funcionamento das mensagens e conversas.

---

## 5. Configuração do Pusher

Para realizar a comunicação em tempo real, foi utilizada a plataforma **Pusher**.

Foi criada uma aplicação no Pusher com as configurações utilizadas no projeto.

O cluster utilizado foi:

```text
us2
```

As informações de autenticação do Pusher foram configuradas no arquivo `.env`.

Exemplo das variáveis utilizadas:

```env
BROADCAST_CONNECTION=pusher

PUSHER_APP_ID="SUA_APP_ID"
PUSHER_APP_KEY="SUA_APP_KEY"
PUSHER_APP_SECRET="SUA_APP_SECRET"
PUSHER_APP_CLUSTER="us2"
```

> ⚠️ As chaves reais do Pusher não são disponibilizadas neste repositório por questão de segurança.

---

## 6. Configuração dos arquivos JavaScript e CSS

O projeto utiliza **Vite** para carregar os arquivos de frontend.

A integração do Chatify foi ajustada para utilizar:

```php
@vite(['resources/css/app.css', 'resources/js/app.js'])
```

Essa configuração permite que os arquivos de CSS e JavaScript sejam carregados corretamente pelo Vite.

---

## 7. Instalação das dependências do Node.js

As dependências do frontend foram instaladas utilizando:

```bash
npm.cmd install
```

Para gerar os arquivos de produção:

```bash
npm.cmd run build
```

O processo foi concluído com sucesso e os arquivos foram gerados na pasta:

```text
public/build
```

---

## 8. Execução do projeto

Para iniciar o servidor Laravel:

```bash
php artisan serve
```

O sistema pode ser acessado pelo endereço:

```text
http://127.0.0.1:8000
```

---

# 💬 Teste do Chat

Para testar o funcionamento do sistema, foram utilizados dois usuários autenticados.

### Usuário 1

Realiza login no sistema e inicia uma conversa com outro usuário.

### Usuário 2

Também realiza login no sistema e recebe a mensagem enviada pelo primeiro usuário.

A comunicação foi testada nos dois sentidos:

```text
Usuário 1 → Usuário 2
Usuário 2 → Usuário 1
```

As mensagens são recebidas em tempo real, demonstrando o funcionamento da comunicação integrada ao Pusher.

---

# 🔄 Funcionamento da comunicação

O fluxo principal do sistema ocorre da seguinte forma:

```text
Usuário
   ↓
Laravel / Chatify
   ↓
Pusher
   ↓
Comunicação em tempo real
   ↓
Outro usuário
```

O Laravel e o Chatify gerenciam a aplicação e as mensagens, enquanto o Pusher realiza a comunicação em tempo real entre os usuários.

---

# 📂 Principais componentes do projeto

Entre os principais componentes utilizados estão:

```text
app/
config/
database/
resources/
routes/
public/
vendor/
.env
composer.json
package.json
vite.config.js
```

O projeto também possui os arquivos necessários para autenticação, mensagens e integração com o Pusher.

---

# 🎥 Vídeo da atividade

O vídeo deverá apresentar o desenvolvimento e o funcionamento do projeto, incluindo:

* Configuração do projeto Laravel;
* Configuração do banco de dados;
* Instalação do Laravel Breeze;
* Instalação do Chatify;
* Configuração do Pusher;
* Código-fonte do projeto;
* Execução do sistema;
* Login dos usuários;
* Interação entre dois usuários;
* Envio e recebimento de mensagens em tempo real.

**Link do vídeo:**

> LINK DO VÍDEO SERÁ INSERIDO AQUI

---

# 🔗 Repositório

Projeto disponível no GitHub:

```text
https://github.com/Herley777/chatLaravelPusher
```

---

# ✅ Resultado

O projeto apresenta um sistema de chat desenvolvido em Laravel com autenticação de usuários e comunicação em tempo real utilizando **Chatify + Pusher**, permitindo a troca de mensagens entre usuários sem a necessidade de atualizar manualmente a página.

---

## 👨‍💻 Projeto acadêmico

Projeto desenvolvido para fins acadêmicos na disciplina de desenvolvimento de aplicações web.
