# 🚀 Guia de Deploy: GitHub + Netlify

## Pré-requisitos
- Conta no GitHub (github.com)
- Conta na Netlify (netlify.com)
- Git instalado no computador

---

## Parte 1: Push para GitHub

### 1️⃣ Criar Repositório no GitHub

1. Acesse https://github.com/new
2. Preencha os dados:
   - **Repository name**: `sereno-loja`
   - **Description**: `Site de e-commerce de roupas de linho - SERENO`
   - **Visibility**: Public ✅
3. Clique em **"Create repository"**
4. Copie a URL que aparece (algo como `https://github.com/seu-usuario/sereno-loja.git`)

### 2️⃣ Fazer Push do Repositório Local

Abra PowerShell/CMD na pasta do projeto e execute:

```bash
# Renomear branch para main
git branch -M main

# Adicionar remote (substitua a URL pela sua)
git remote add origin https://github.com/seu-usuario/sereno-loja.git

# Fazer push
git push -u origin main
```

**Será pedido seu usuário/senha do GitHub:**
- Usuário: seu email GitHub
- Senha: seu Personal Access Token (veja instruções abaixo)

### 📝 Como gerar Personal Access Token

Se o Git pedir senha:
1. Vá para https://github.com/settings/tokens/new
2. Dê um nome: `sereno-deploy`
3. Marque: `repo` (acesso completo ao repositório)
4. Clique em **"Generate token"**
5. Copie o token (aparece uma única vez)
6. Use este token como senha no git push

---

## Parte 2: Deploy na Netlify

### 1️⃣ Conectar Netlify ao GitHub

1. Acesse https://netlify.com
2. Faça login com GitHub (botão azul)
3. Autorize o Netlify a acessar seus repositórios
4. Clique em **"New site from Git"**

### 2️⃣ Selecionar Repositório

1. Escolha **GitHub** como provider
2. Busque por `sereno-loja`
3. Selecione o repositório

### 3️⃣ Configurações de Build

Deixe as configurações padrão:
- **Branch**: main
- **Build command**: (deixe vazio - não precisa)
- **Publish directory**: . (ponto, significa a raiz)

Clique em **"Deploy site"**

### ⏳ Aguarde o Deploy

Netlify vai:
1. Clonar o repositório
2. Fazer build (rápido, já que é só HTML)
3. Colocar online

Quando terminar, você receberá um URL como:
```
https://seu-site-aleatorio.netlify.app
```

### 🔧 Renomear o Site (Opcional)

1. Em **Site settings** → **General**
2. Clique em **"Change site name"**
3. Digite um nome melhor (ex: `sereno-loja`)
4. Novo URL: `https://sereno-loja.netlify.app`

---

## Parte 3: Atualizações Futuras

Toda vez que você fizer mudanças:

```bash
# 1. Fazer as alterações nos arquivos

# 2. Stage e commit
git add .
git commit -m "Descrição das mudanças"

# 3. Push para GitHub
git push

# 4. Netlify detecta automaticamente e faz deploy!
```

---

## ✅ Checklist Final

- [ ] Repositório criado no GitHub
- [ ] Arquivos fizeram push
- [ ] Site conectado na Netlify
- [ ] Deploy completado com sucesso
- [ ] Site acessível em netlify.app

---

## 🆘 Troubleshooting

### Git push falha com "authentication failed"
- Use Personal Access Token, não senha

### Netlify mostra erro 404
- Verifique se o `netlify.toml` existe
- Verifique se todos os arquivos estão no repositório

### Imagens não aparecem
- Verifique se a pasta `imagens/` foi commitada
- Use caminhos relativos (ex: `imagens/photo.jpg`)

### Site não atualiza após push
- Espere alguns minutos (Netlify está fazendo deploy)
- Limpe o cache do navegador (Ctrl+F5)
- Verifique o status em https://app.netlify.com

---

Pronto! Seu site está online! 🎉
