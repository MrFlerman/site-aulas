# Site com Netlify CMS - Instruções Simples

## 🎯 O que você vai ter

- Interface visual para adicionar aulas (como WordPress)
- Design bonito e profissional
- Acesso em: `seusite.com/admin`
- Zero código para adicionar novas aulas

## 📦 Passo 1: Subir para o GitHub

1. Vá em https://github.com/new
2. Crie um repositório novo (ex: "site-aulas")
3. Faça upload desta pasta

**Ou pelo terminal:**
```bash
cd netlify-site
git init
git add .
git commit -m "Site inicial"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

## 🚀 Passo 2: Conectar no Netlify

1. Acesse https://app.netlify.com
2. Clique em "Add new site" → "Import an existing project"
3. Escolha "GitHub" e autorize
4. Selecione seu repositório
5. Configure:
   - **Build command:** `hugo`
   - **Publish directory:** `public`
6. Clique em "Deploy site"

## 🔐 Passo 3: Ativar Identity & Git Gateway

1. No painel do Netlify, vá em "Site configuration" → "Identity"
2. Clique em "Enable Identity"
3. Em "Registration preferences", escolha "Invite only"
4. Vá em "Services" → "Git Gateway" → "Enable Git Gateway"
5. Em "Identity", clique em "Invite users" e adicione seu email
6. Você receberá um email → clique no link para criar senha

## ✏️ Passo 4: Usar a Interface

1. Acesse `seusite.netlify.app/admin`
2. Faça login com seu email
3. Clique em "Aulas" → "New Aulas"
4. Preencha o formulário:
   - Título da aula
   - Data
   - Número
   - Período histórico
   - Categoria
   - Duração
   - Descrição curta
   - **Conteúdo da aula** (editor rico de markdown)

5. Clique em "Publish" → "Publish now"
6. Aguarde 1-2 minutos
7. Seu site está atualizado!

## 📝 Editando Conteúdo

O editor de markdown tem botões para:
- **Negrito** e *itálico*
- Títulos (##, ###)
- Listas
- Links
- Imagens (faça upload direto)
- Citações
- Tabelas

É visual, tipo Google Docs!

## 📸 Adicionando Imagens

No editor de conteúdo:
1. Clique no ícone de imagem
2. Faça upload da sua imagem
3. A imagem é inserida automaticamente

## 🎨 Mudando Informações do Professor

No Netlify CMS você NÃO vai conseguir editar isso pela interface (limitação).

Para mudar, edite o arquivo `config.toml` direto no GitHub:
```toml
[params]
  professor = "Seu Nome Aqui"
  universidade = "Sua Universidade"
  email = "seu@email.com"
```

## 🔄 Fluxo de Trabalho Diário

1. Acesse `seusite.com/admin`
2. Login
3. Crie/edite aulas
4. Publique
5. Pronto!

Não precisa de terminal, VS Code, nada. Tudo pela web.

## ❓ Problemas Comuns

**"Cannot access admin"**
→ Certifique-se que ativou o Identity no Netlify

**"Mudanças não aparecem"**
→ Aguarde 1-2 minutos para o deploy

**"Esqueci a senha"**
→ Use "Forgot password" no login do /admin

## 📱 Bônus: Editar pelo Celular

Funciona! Acesse `/admin` pelo navegador do celular.

## 🆘 Precisa de Ajuda?

Se algo der errado:
1. Confira se seguiu todos os passos do Identity
2. Veja os logs de deploy no Netlify
3. Confira se o GitHub está conectado

---

**É isso!** Muito mais simples que Google Sites e infinitamente mais bonito.
