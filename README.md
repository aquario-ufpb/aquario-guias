# Guias do Aquário

Este repositório contém o conteúdo dos guias do Aquário UFPB, organizados por curso.

## 📁 Estrutura de Pastas

A estrutura de pastas determina como os guias serão organizados no site:

```
aquario-guias/
├── ciencia-da-computacao/
│   ├── bem-vindo/
│   │   └── sobre-o-curso/
│   │       └── content.md
│   ├── cadeiras/
│   │   └── principais-cadeiras/
│   │       ├── calculo-I/
│   │       │   └── content.md
│   │       └── programacao-I/
│   │           └── content.md
│   └── laboratorios/
│       └── laico/
│           └── content.md
├── ciencias-de-dados-e-inteligencia-artificial/
│   └── ...
└── engenharia-da-computacao/
    └── ...
```

## 🗂️ Hierarquia no Site

A estrutura de pastas é mapeada para URLs da seguinte forma:

```
/{curso}/{guia}/{secao}/{subsecao}
```

### Níveis:

1. **Curso** (nível 1): Nome do curso (pasta raiz)
   - Exemplo: `ciencia-da-computacao`
   - URL: `/guias/ciencia-da-computacao`

2. **Guia** (nível 2): Categoria principal do guia
   - Exemplo: `bem-vindo`, `cadeiras`, `laboratorios`
   - URL: `/guias/ciencia-da-computacao/bem-vindo`

3. **Seção** (nível 3): Tópico dentro do guia
   - Exemplo: `sobre-o-curso`, `principais-cadeiras`
   - URL: `/guias/ciencia-da-computacao/bem-vindo/sobre-o-curso`

4. **Subseção** (nível 4): Subtópico específico
   - Exemplo: `calculo-I`, `programacao-I`
   - URL: `/guias/ciencia-da-computacao/cadeiras/principais-cadeiras/calculo-I`

## ✍️ Como Adicionar Novo Conteúdo

### 1. Escolha o Curso

Navegue até a pasta do curso onde deseja adicionar conteúdo:

- `ciencia-da-computacao/`
- `ciencias-de-dados-e-inteligencia-artificial/`
- `engenharia-da-computacao/`

### 2. Crie a Estrutura de Pastas

Crie as pastas necessárias seguindo a hierarquia:

```bash
# Exemplo: Adicionar conteúdo sobre Git no curso de Ciência da Computação
mkdir -p ciencia-da-computacao/ferramentas/controle-versao/git
```

### 3. Crie o Arquivo `content.md`

Cada página de conteúdo **deve** ser chamada `content.md`:

```bash
touch ciencia-da-computacao/ferramentas/controle-versao/git/content.md
```

### 4. Escreva o Conteúdo em Markdown

Adicione o conteúdo usando Markdown padrão:

````markdown
# Git - Controle de Versão

## O que é Git?

Git é um sistema de controle de versão distribuído...

## Comandos Básicos

### Inicializar Repositório

```bash
git init
```
````

### Fazer Commit

```bash
git add .
git commit -m "Mensagem do commit"
```

## Recursos Adicionais

- [Documentação Oficial](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)

```

## 📝 Convenções de Nomenclatura

### Nomes de Pastas

- Use **kebab-case** (palavras separadas por hífen)
- Use apenas letras minúsculas
- Evite caracteres especiais e acentos
- Seja descritivo mas conciso

✅ **Bom:**
- `ciencia-da-computacao`
- `principais-cadeiras`
- `controle-versao`

❌ **Ruim:**
- `Ciência da Computação` (com espaços e acentos)
- `PrincipaisCadeiras` (camelCase)
- `controle_versao` (underscore)

### Títulos no Markdown

- Use títulos descritivos e amigáveis
- Podem conter acentos e caracteres especiais
- O sistema converte automaticamente os nomes das pastas em títulos

## 🎯 Exemplos Práticos

### Exemplo 1: Adicionar Guia sobre Laboratório

**Objetivo:** Criar guia sobre o LAICO

**Estrutura:**
```

ciencia-da-computacao/
└── laboratorios/
└── laico/
└── content.md

````

**URL resultante:** `/guias/ciencia-da-computacao/laboratorios/laico`

**content.md:**
```markdown
# LAICO - Laboratório de Aplicações de Informática Avançada

## Sobre o LAICO

O LAICO é um laboratório...

## Horários de Funcionamento

- Segunda a Sexta: 8h às 18h
- Sábado: 8h às 12h
````

### Exemplo 2: Adicionar Múltiplas Cadeiras

**Objetivo:** Adicionar várias cadeiras do curso

**Estrutura:**

```
ciencia-da-computacao/
└── cadeiras/
    ├── primeiro-periodo/
    │   ├── calculo-I/
    │   │   └── content.md
    │   ├── programacao-I/
    │   │   └── content.md
    │   └── introducao-computacao/
    │       └── content.md
    └── segundo-periodo/
        ├── calculo-II/
        │   └── content.md
        └── estrutura-dados/
            └── content.md
```

### Exemplo 3: Seção com Subseções (Índice Automático)

Se você criar uma seção **sem** `content.md` próprio, mas com subseções, o sistema gera automaticamente um índice:

**Estrutura:**

```
ciencia-da-computacao/
└── ferramentas/
    ├── git/
    │   └── content.md
    ├── docker/
    │   └── content.md
    └── linux/
        └── content.md
```

**Resultado:** Ao acessar `/guias/ciencia-da-computacao/ferramentas`, será exibido:

```markdown
# Ferramentas

## Conteúdo disponível

- [Git](/guias/ciencia-da-computacao/ferramentas/git)
- [Docker](/guias/ciencia-da-computacao/ferramentas/docker)
- [Linux](/guias/ciencia-da-computacao/ferramentas/linux)
```

## 🔗 Links Internos

Ao criar links para outras páginas do guia, use caminhos absolutos:

```markdown
Veja mais em [Programação I](/guias/ciencia-da-computacao/cadeiras/primeiro-periodo/programacao-I)
```

## 🖼️ Imagens e Recursos

Para adicionar imagens:

1. Crie uma pasta `assets` ou `imagens` no mesmo nível do `content.md`
2. Referencie usando caminho relativo:

```markdown
![Descrição da imagem](./imagens/foto.png)
```

## ✅ Checklist para Novo Conteúdo

Antes de fazer commit, verifique:

- [ ] Todas as pastas usam kebab-case
- [ ] O arquivo se chama exatamente `content.md`
- [ ] O conteúdo está em Markdown válido
- [ ] Links internos usam caminhos absolutos
- [ ] Imagens (se houver) estão na estrutura correta
- [ ] O conteúdo está revisado e sem erros ortográficos

## 🚀 Publicação

Após adicionar ou editar conteúdo:

1. Faça commit e push para este repositório:

```bash
git add .
git commit -m "feat: adicionar guia sobre [assunto]"
git push
```

2. O repositório principal do Aquário será atualizado:
   - Automaticamente via GitHub Actions, ou
   - Manualmente pelos mantenedores

3. O conteúdo aparecerá no site após a próxima build!

## 📞 Dúvidas?

Se tiver dúvidas sobre como organizar o conteúdo ou onde adicionar um guia específico, abra uma issue neste repositório ou entre em contato com a equipe do Aquário.

---

**Mantido pela comunidade Aquário UFPB** 🐟
