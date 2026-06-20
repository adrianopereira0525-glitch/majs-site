# Como publicar o site da MAJS — guia para Adriano

Esse guia assume que você nunca publicou um site. Sem pressa, é só seguir a ordem.

---

## Resumo do caminho

1. Criar conta no GitHub (guarda o código)
2. Subir os arquivos do site lá
3. Conectar o GitHub com a Vercel (publica o site)
4. Pegar o link pronto (ex: `majs.vercel.app`)
5. Sempre que quiser mudar algo, volta no chat com a Claude, pega o arquivo novo, sobe no GitHub de novo — o site atualiza sozinho

---

## Passo 1 — Criar conta no GitHub

1. Acesse **github.com**
2. Clique em **Sign up**
3. Use seu e-mail, crie uma senha, escolha um nome de usuário
4. Confirme o e-mail que ele manda

GitHub é só um "armário" gratuito que guarda o código do site.

---

## Passo 2 — Criar o repositório (a pasta do site no GitHub)

1. Depois de logado, clique no **+** no canto superior direito → **New repository**
2. Nome sugerido: `majs-site`
3. Deixe como **Public**
4. Clique em **Create repository**

---

## Passo 3 — Subir os arquivos

Na tela que abrir, vai ter um link **"uploading an existing file"**.

1. Clique nele
2. Arraste **todos os arquivos e pastas** que vieram dentro do pacote que a Claude te entregou (incluindo as pastas `src` e `public`, e os arquivos `package.json`, `vite.config.js`, `index.html`)
3. Escreva qualquer mensagem tipo "primeira versão do site"
4. Clique em **Commit changes**

---

## Passo 4 — Criar conta na Vercel e publicar

1. Acesse **vercel.com**
2. Clique em **Sign Up** → escolha **Continue with GitHub** (assim ele já conecta os dois)
3. Autorize o acesso
4. Clique em **Add New... → Project**
5. Selecione o repositório `majs-site` que você acabou de criar
6. Ele já reconhece automaticamente que é um projeto Vite/React — não precisa mudar nada
7. Clique em **Deploy**

Em menos de um minuto, ele te dá um link tipo:

```
https://majs-site.vercel.app
```

Esse link já é público — qualquer pessoa pode acessar, de qualquer lugar.

---

## Passo 5 — Colocar um domínio próprio (opcional, depois)

Se no futuro você registrar o `majs.com.br` no Registro.br, dentro do projeto na Vercel
tem uma aba **Domains** onde você cola esse domínio e segue as instruções — a Claude
pode te ajudar nessa hora também.

---

## Como editar o site depois de publicado

Sempre que quiser mudar:

1. Volte aqui no chat com a Claude e peça a alteração (cor, texto, foto, nova seção...)
2. Quando terminar, baixe o arquivo `MAJSSite.jsx` atualizado
3. No GitHub, abra o repositório → vá até `src/MAJSSite.jsx` → clique no ícone de lápis (editar)
4. Apague tudo e cole o conteúdo novo
5. Clique em **Commit changes**

A Vercel detecta a mudança automaticamente e publica a nova versão sozinha, em
1-2 minutos. Você não precisa repetir os passos 4 e 5.

---

## Importante sobre o Calendário, Escala e Louvores

Hoje, os dados que vocês editam direto no site (calendário de eventos, escala da
semana, louvores) ficam salvos **no navegador de cada pessoa**, não em um lugar
compartilhado entre todos. Ou seja: se você editar no seu celular, só você vê a
atualização — quem acessar pelo computador da igreja não vê automaticamente.

Para resolver isso direito (todo mundo vendo a mesma informação ao mesmo tempo),
o próximo passo seria conectar o site a um banco de dados simples. É um passo a
mais, mas dá pra fazer — é só pedir pra Claude quando quiser evoluir isso.

---

## Dúvidas comuns

**"Errei alguma coisa no GitHub, e agora?"**
Sem problema, pode apagar o repositório e criar de novo, ou só corrigir o arquivo
com problema clicando no lápis de edição.

**"Posso usar isso no celular?"**
Sim, dá pra fazer todo o processo de criar conta e subir arquivos pelo celular,
mas é mais confortável no computador.

**"Preciso pagar alguma coisa?"**
Não. GitHub e Vercel são gratuitos para esse uso.
