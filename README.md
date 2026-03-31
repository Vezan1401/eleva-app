# Eleva PWA — Guia de Publicação

## O que está nesta pasta

| Arquivo | O que faz |
|---------|-----------|
| `index.html` | O app completo (telas, produtos, carrinho) |
| `manifest.json` | Configura o app para instalar no celular |
| `sw.js` | Permite o app funcionar sem internet |

---

## Como publicar de graça na Vercel (passo a passo)

### Passo 1 — Crie uma conta gratuita no GitHub
1. Acesse https://github.com
2. Clique em **Sign up** e crie sua conta

### Passo 2 — Crie um repositório com os arquivos
1. Após entrar no GitHub, clique no **+** no canto superior direito
2. Clique em **New repository**
3. Nome: `eleva-app`
4. Marque **Public**
5. Clique em **Create repository**
6. Clique em **uploading an existing file**
7. Arraste os 3 arquivos desta pasta (`index.html`, `manifest.json`, `sw.js`)
8. Clique em **Commit changes**

### Passo 3 — Conecte ao Vercel (hospedagem gratuita)
1. Acesse https://vercel.com
2. Clique em **Sign up** → entre com sua conta do GitHub
3. Clique em **Add New Project**
4. Escolha o repositório `eleva-app`
5. Clique em **Deploy**

### Passo 4 — Seu app está no ar!
A Vercel vai gerar um link como:
**https://eleva-app.vercel.app**

Você pode compartilhar esse link com os clientes. No celular, o Chrome vai perguntar se quer "Adicionar à tela inicial" — ao clicar, o app aparece como um aplicativo normal!

---

## Como adicionar seus ícones

Na pasta `icons/`, coloque duas imagens com o logo da Eleva:
- `icon-192.png` (192×192 pixels)
- `icon-512.png` (512×512 pixels)

Você pode criar gratuitamente em: https://www.canva.com

---

## Como atualizar os produtos

Abra o arquivo `index.html` em qualquer editor de texto (ex: Bloco de Notas ou VS Code).

Procure pela linha:
```
const PRODUCTS = [
```

Cada produto tem este formato:
```js
{ id:1, name:'Top Aura', cat:'Top', price:90, emoji:'👕', tag:'Novo', sizes:['PP','P','M','G','GG'] },
```

Você pode:
- Mudar o `name` (nome do produto)
- Mudar o `price` (preço)
- Mudar o `tag` para `'SALE'`, `'Novo'` ou `''` (sem tag)
- Mudar os `sizes` disponíveis

Após editar, faça upload do arquivo novamente no GitHub e a Vercel vai atualizar automaticamente.

---

## Domínio personalizado (opcional, gratuito)

Na Vercel, você pode conectar um domínio próprio como `app.byeleva.com.br`.
Se precisar de ajuda com isso, consulte: https://vercel.com/docs/projects/domains
