# OAuth2.0 + OICD OpenId  - Demonstração (API)

Essa uma demonstração do modelo Delegated Authorization Flow onde:
1. Convivem aplicação web (Client) + Servidor de autenticação (auth0) + Servidor de Recursos (API)
2. Aqui estão detalhes da camada API
3. A aplicação WEB ou APP delega a autenticação de seus usuários para um servidor de autenticação (auth0)
4. O servdidor verifica a autenticação e se sucesso retorna para a página logada (/callback)
5. Juntamente com o redirect o servidor retorna um authorization_code que identifica o usuário autenticado
6. Ao receber o authorization_code o cliente (aplicação web) usa o authorization_code para obter um access_token
7. Com esse access_token a aplicação web poderá consumir a os recursos do Servidor de Recursos (API)
8. O servidor de API valida o token, extrai dele a identificação do usuário e entrega o conteúdo de acordo com o usuário que solicitou.

Como testar

1. Faça clone do repositório
2. Execute `npm install`
3. Execute `npm start`
4. Acesse `http://localhost:3001`
5. Vá até o projeto Web APP, inicie a aplicação web
6. Ao chamar `http://localhost:3001` com o devido access_token o servidor deverá responder um conteúdo como resposta.