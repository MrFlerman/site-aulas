# Site Hugo - Estado, Política e História do Direito

Site acadêmico para disciplina, gerado com Hugo e preparado para deploy no Netlify.

## 📋 O que você tem aqui

- **Página principal**: Lista todas as aulas automaticamente
- **Páginas individuais**: Cada aula tem sua própria página completa
- **Design sóbrio**: Paleta tradicional (bordeaux, navy, dourado)
- **Responsivo**: Funciona em desktop, tablet e celular

## 🚀 Como usar

### 1. Instalar Hugo (se ainda não tiver)

**macOS:**
```bash
brew install hugo
```

**Linux:**
```bash
sudo apt-get install hugo
```

**Windows:**
Baixe em https://gohugo.io/installation/

### 2. Ver o site localmente

No terminal, dentro da pasta `site-hugo`:

```bash
hugo server -D
```

Abra o navegador em: `http://localhost:1313`

O site atualiza automaticamente quando você edita os arquivos!

### 3. Adicionar uma nova aula

Crie um arquivo novo em `content/aulas/` chamado `aula-04.md`:

```markdown
---
title: "Título da Aula"
date: 2025-03-27
numero: 4
periodo: "Período Histórico"
categoria: "medieval"
duracao: "100 minutos"
descricao: "Breve descrição que aparece no card"
---

## Primeiro Tópico

Seu conteúdo aqui...

### Subtópico

Mais conteúdo...

- Lista item 1
- Lista item 2

> Citação importante

[Link para PDF](/materiais/aula04.pdf)
```

### 4. Formatação do Markdown

**Negrito:** `**texto**`  
**Itálico:** `*texto*`  
**Títulos:** `## Título` (quanto mais #, menor o título)  
**Listas:** Use `-` ou `1.`  
**Links:** `[texto](url)`  
**Citações:** `> texto`  
**Código:** `` `código` ``

**Imagens:**
```markdown
![Descrição da imagem](/images/nome.jpg)
```
(Coloque as imagens em `static/images/`)

**Tabelas:**
```markdown
| Coluna 1 | Coluna 2 |
|----------|----------|
| Dado 1   | Dado 2   |
```

**Vídeo do YouTube:**
```markdown
{{< youtube ID_DO_VIDEO >}}
```

### 5. Estrutura de arquivos

```
site-hugo/
├── config.toml          # Configurações gerais
├── content/
│   └── aulas/          # SUAS AULAS AQUI
│       ├── _index.md
│       ├── aula-01.md
│       ├── aula-02.md
│       └── aula-03.md
├── layouts/            # Templates HTML (não precisa mexer)
│   └── _default/
│       ├── baseof.html
│       ├── list.html   # Página principal
│       └── single.html # Página de cada aula
└── static/
    ├── css/           # Estilos
    └── images/        # Suas imagens aqui
```

## 📤 Publicar no Netlify

### Opção 1: Drag and Drop (mais fácil)

1. Gerar o site:
   ```bash
   hugo
   ```
   Isso cria a pasta `public/`

2. Acesse https://app.netlify.com/drop

3. Arraste a pasta `public/` para o site

4. Pronto! Seu site está no ar.

### Opção 2: GitHub + Netlify (recomendado)

1. **Criar repositório no GitHub:**
   - Vá em github.com
   - Crie um novo repositório
   - Faça upload da pasta `site-hugo`

2. **Conectar ao Netlify:**
   - Acesse https://netlify.com
   - "New site from Git"
   - Conecte seu GitHub
   - Selecione o repositório
   - Build command: `hugo`
   - Publish directory: `public`

3. **Deploy automático:**
   - Sempre que você fizer commit no GitHub
   - O Netlify regenera o site automaticamente
   - Demora ~1 minuto

## 🎨 Personalizar

### Mudar informações do professor

Edite `config.toml`:

```toml
[params]
  professor = "Seu Nome"
  universidade = "Sua Universidade"
  periodo = "2025/1"
  carga_horaria = "80 horas"
  email = "seu@email.com"
```

### Mudar cores

Edite `static/css/style.css`, no início do arquivo:

```css
:root {
    --bordeaux: #6b2737;  /* Cor principal */
    --navy: #1e2a3a;      /* Azul escuro */
    --gold: #b8986b;      /* Dourado */
    /* ... */
}
```

## 💡 Dicas

1. **Escreva no VS Code** ou qualquer editor de texto
2. **Use `hugo server -D`** para ver mudanças em tempo real
3. **Faça backup** antes de mudanças grandes
4. **Organize por módulo** usando a categoria no frontmatter
5. **PDFs e materiais** vão em `static/materiais/`

## 📝 Exemplo de Fluxo de Trabalho

1. Abra o terminal na pasta do site
2. `hugo server -D` (deixe rodando)
3. Abra navegador em localhost:1313
4. Crie/edite arquivo `.md` em `content/aulas/`
5. Veja mudanças automaticamente no navegador
6. Quando terminar: Ctrl+C no terminal
7. `hugo` para gerar versão final
8. Commit no GitHub (se usar) ou upload no Netlify

## 🆘 Problemas Comuns

**"Hugo não encontrado"**
→ Instale o Hugo primeiro

**"Página em branco"**
→ Verifique se tem `_index.md` em `content/aulas/`

**"Imagem não aparece"**
→ Coloque em `static/images/` e use `/images/nome.jpg`

**"CSS não carrega"**
→ Verifique se `static/css/style.css` existe

## 📚 Recursos

- Hugo: https://gohugo.io/documentation/
- Markdown: https://www.markdownguide.org/
- Netlify: https://docs.netlify.com/

---

**Dúvidas?** Consulte a documentação do Hugo ou entre em contato.
