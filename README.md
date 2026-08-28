 # Bot de Autenticação para Discord (OAuth2)

[![Licença](https://shields.io)](LICENSE)
[![Discord](https://shields.io)](https://discord.gg)

Um bot do Discord avançado focado em segurança, verificação e proteção da sua comunidade. Desenvolvido em JavaScript, ele utiliza o sistema OAuth2 do Discord para autenticar usuários, oferecendo um sistema de gerenciamento e configuração 100% integrado dentro do próprio Discord, além de um sistema de Handler automatizado para comandos.

##  Funcionalidades

*   **Configuração In-Discord:** Gerencie tudo (cargos, canais e logs) diretamente por comandos no Discord, sem complicação.
*   **Sistema de Handler:** Estrutura moderna e organizada para carregamento automático de eventos e comandos Slash (/).
*   **Verificação OAuth2:** Autenticação externa segura para validar que o usuário é real.
*   **Backup e Restauração (Puxar):** Salva o acesso dos membros no banco de dados, permitindo restaurá-los se o servidor sofrer algum problema.
*   **Painel de Verificação:** Envio automatizado de botões e links de autenticação nos canais selecionados.

## 🛠️ Tecnologias Utilizadas

*   [Node.js](https://nodejs.org) (Ambiente de execução)
*   [Discord.js](https://js.org) (Biblioteca do bot)
*   [JavaScript](https://mozilla.org) (Linguagem de programação)
*   [Express](https://expressjs.com) (Para gerenciar a rota de callback do OAuth2)

## 📦 Instalação e Configuração

### Pré-requisitos
*   [Node.js](https://nodejs.org) v18.x ou superior instalado.
*   URL de redirecionamento configurada no [Discord Developer Portal](https://discord.com) (OAuth2 -> Redirects).

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com
   cd seu-repositorio
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Configure as variáveis de ambiente:**
   Crie um arquivo `.env` na raiz do projeto e preencha com seus dados:
   ```env
   TOKEN=SEU_TOKEN_DO_BOT
   CLIENT_ID=ID_DO_BOT
   CLIENT_SECRET=SECRET_DO_OAUTH2_DO_BOT
   REDIRECT_URI=https://sua-url.com
   PORT=3000
   DATABASE_URL=SUA_CONEXAO_COM_BANCO_DE_DADOS
   ```

4. **Inicie o bot:**
   ```bash
   node index.js
   ```

## ⚙️ Comandos Principais (/)

*   `/configurar` - Painel completo dentro do Discord para definir cargos, logs e canais.
*   `/enviar` - Envia o painel/mensagem com o botão de autenticação OAuth2 no canal.
*   `/puxar` - Comando restrito para restaurar/trazer os membros autenticados de volta para o servidor.
*   `/status` - Mostra a quantidade de usuários salvos na sua lista de autenticação.

## 📄 Licença

Este projeto está sob a licença [MIT](LICENSE). Veja o arquivo para mais detalhes.
