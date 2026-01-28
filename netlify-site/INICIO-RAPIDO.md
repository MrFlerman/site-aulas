# ⚡ Guia Rápido - 10 Minutos

## Passo 1: GitHub (2 min)
1. Vai em github.com/new
2. Nome: "site-aulas"
3. Upload do ZIP que baixou

## Passo 2: Netlify (3 min)
1. app.netlify.com
2. "New site" → GitHub
3. Escolhe o repo
4. Build: `hugo`
5. Pasta: `public`
6. Deploy!

## Passo 3: Identity (3 min)
1. Site configuration → Identity
2. Enable Identity
3. Enable Git Gateway
4. Invite users → seu email
5. Abre email, cria senha

## Passo 4: Usar! (2 min)
1. seusite.com/admin
2. Login
3. "New Aulas"
4. Preenche
5. Publish!

---

## Interface do Admin

Quando acessar /admin, você verá:

```
┌─────────────────────────────────┐
│  Netlify CMS                    │
├─────────────────────────────────┤
│  Collections:                   │
│  > Aulas                        │
│                                 │
│  Quick add:                     │
│  [+ New Aulas]                  │
└─────────────────────────────────┘
```

Ao criar aula:

```
┌─────────────────────────────────┐
│  Nova Aula                      │
├─────────────────────────────────┤
│  Título: [____________]         │
│  Data: [06/03/2025]            │
│  Número: [1]                    │
│  Período: [____________]        │
│  Categoria: [▼ antiguidade]     │
│  Duração: [100 minutos]         │
│  Descrição: [____________]      │
│                                 │
│  Conteúdo: (editor rico)        │
│  ┌───────────────────────┐     │
│  │ B I U [H] [•] [1] ["] │     │
│  ├───────────────────────┤     │
│  │                       │     │
│  │ Escreva aqui...       │     │
│  │                       │     │
│  └───────────────────────┘     │
│                                 │
│  [Publish] [Save Draft]         │
└─────────────────────────────────┘
```

## Resultado

Cada vez que você publicar:
- Netlify detecta mudança
- Gera o site (30 seg)
- Publica automaticamente
- Seu site está atualizado!

---

**É ISSO!** Muito mais fácil que editar HTML manualmente.

Qualquer dúvida, leia o COMO-USAR.md completo.
