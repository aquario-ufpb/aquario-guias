# Guias do Aquário

Esse repositório contém o conteúdo dos guias do Aquário UFPB, organizados por centro e categorias temáticas.

## 📁 Estrutura de Pastas

A estrutura de pastas determina como os guias serão organizados no site. Você pode usar **nomes elegantes e legíveis** para seus arquivos!

```
aquario-guias/
└── centro-de-informatica/
    ├── 0 - Bem Vindo/
    │   ├── 1 - Introdução.md
    │   └── 2 - Dicas.md
    ├── 1 - Grupos/
    │   ├── Atética.md
    │   ├── Grupos e Ligas.md
    │   ├── Laboratórios.md
    │   └── PET.md
    ├── 2 - Informações/
    │   ├── Bolsas.md
    │   ├── Salas.md
    │   └── Transporte.md
    ├── Ciencia da Computação/
    │   ├── 0 - Sobre o Curso.md
    │   ├── Coordenação.md
    │   ├── Estrutura CC.md
    │   └── Grade.md
    ├── Ciencia de Dados e Inteligencia Artificial/
    │   └── ...
    └── Engenharia da Computação/
        └── ...
```

## 🗂️ Hierarquia no Site

A estrutura de pastas é mapeada para URLs da seguinte forma:

```
/guias/{guia}/{secao}/{subsecao}
```

### Níveis:

1. **Centro** (nível 1): Nome do centro (pasta raiz - **usa kebab-case**)
   - Exemplo: `centro-de-informatica`
   - URL: `/guias`

2. **Guia** (nível 2): Categoria principal do guia (pasta)
   - Exemplo: `0 - Bem Vindo`, `1 - Grupos`, `Ciencia da Computação`
   - URL: `/guias/0-bem-vindo`, `/guias/1-grupos`, `/guias/ciencia-da-computacao`

3. **Seção** (nível 3): Arquivo `.md` com nome amigável
   - Exemplo: `1 - Introdução.md`, `Atética.md`, `Sobre o Curso.md`
   - URL: `/guias/0-bem-vindo/1-introducao` (slug gerado automaticamente!)

4. **Subseção** (nível 4): Arquivo `.md` dentro de uma pasta de seção
   - Exemplo: Arquivos dentro de pastas como `Estrutura CC/`
   - URL: `/guias/ciencia-da-computacao/estrutura-cc/[subsecao]`

## ✨ Características da Estrutura

A estrutura permite:

- ✅ **Nomes legíveis**: Use espaços, acentos e maiúsculas
- ✅ **Mais intuitivo**: O nome do arquivo é exatamente o que você quer mostrar
- ✅ **Slugs automáticos**: O sistema converte "Cálculo I.md" → URL `calculo-i`
- ✅ **Estrutura simplificada**: Use `Nome do Arquivo.md` diretamente, sem necessidade de `pasta/content.md`

## ✍️ Como Adicionar Novo Conteúdo

### 1. Escolha o Centro e Categoria

Navegue até a pasta do centro (`centro-de-informatica/`) e escolha ou crie a categoria apropriada:

- Para conteúdo geral do CI: `0 - Bem Vindo`, `1 - Grupos`, `2 - Informações`, etc.
- Para conteúdo específico de curso: `Ciencia da Computação`, `Ciencia de Dados e Inteligencia Artificial`, `Engenharia da Computação`

⚠️ **Atenção**: Apenas a pasta do **centro** deve usar kebab-case (ex: `centro-de-informatica`). As pastas de categorias podem usar nomes descritivos com espaços e maiúsculas.

### 2. Crie a Estrutura de Pastas (se necessário)

Crie as pastas necessárias seguindo a hierarquia:

```bash
# Exemplo: Adicionar conteúdo sobre ferramentas no CI
mkdir -p centro-de-informatica/3 - Ferramentas
```

### 3. Crie o Arquivo Markdown com Nome Elegante

Crie um arquivo `.md` com um **nome descritivo e amigável**:

```bash
# Use espaços, acentos e maiúsculas normalmente!
touch "centro-de-informatica/3 - Ferramentas/Controle de Versão com Git.md"
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

### Fazer Commit

```bash
git add .
git commit -m "Mensagem do commit"
```

## Recursos Adicionais

- [Documentação Oficial](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
````

## 📝 Convenções de Nomenclatura

### Nomes de Pastas

**Para pasta do CENTRO (nível raiz):**

- Use **kebab-case** (palavras separadas por hífen)
- Use apenas letras minúsculas
- Evite caracteres especiais e acentos

✅ **Correto para centros:**

- `centro-de-informatica`

**Para outras pastas (categorias/guias):**

- Use nomes descritivos com espaços e maiúsculas quando apropriado
- Pode usar números para ordenação (ex: `0 - Bem Vindo`, `1 - Grupos`)
- Exemplos: `0 - Bem Vindo`, `1 - Grupos`, `Ciencia da Computação`, `Ferramentas`

### Nomes de Arquivos Markdown

🎉 **Use nomes amigáveis e legíveis!**

✅ **Excelente:**

- `Sobre o Curso.md`
- `Principais Cadeiras.md`
- `Cálculo I.md`
- `Programação Orientada a Objetos.md`
- `Introdução à Inteligência Artificial.md`

✅ **Também funciona:**

- `LAICO.md`
- `Git.md`
- `Docker.md`

### Como os Slugs são Gerados

O sistema converte automaticamente os nomes dos arquivos em URLs amigáveis:

| Nome do Arquivo              | Slug (URL)                |
| ---------------------------- | ------------------------- |
| `Sobre o Curso.md`           | `sobre-o-curso`           |
| `Cálculo I.md`               | `calculo-i`               |
| `Programação I.md`           | `programacao-i`           |
| `Inteligência Artificial.md` | `inteligencia-artificial` |

**Regras de conversão:**

- Remove acentos: á → a, ç → c
- Remove espaços: substitui por hífen
- Converte para minúsculas
- Remove caracteres especiais

## 🎯 Exemplos Práticos

### Exemplo 1: Conteúdo Simples (Sem Sub-conteúdo)

**Objetivo:** Criar guia sobre Laboratórios

**Estrutura:**

```
centro-de-informatica/
└── 1 - Grupos/
    └── Laboratórios.md
```

**URL resultante:** `/guias/1-grupos/laboratorios`

**Laboratórios.md:**

```markdown
# Laboratórios - O que são?

Você ouvirá bastante sobre os laboratórios do CI. Eles são basicamente mini instituições dentro da UFPB lideradas cada uma por seus professores e que tem como objetivo a realização de projetos dentro da área determinada pelo laboratório.

## Como entrar em um?

Vai depender muito de cada laboratório. O recomendado é perguntar a pessoas mais a frente do curso sobre cada um...
```

### Exemplo 2: Conteúdo com Sub-conteúdo

**Objetivo:** Criar seção sobre estrutura do curso com detalhes de cada componente

**Estrutura:**

```
centro-de-informatica/
└── Ciencia da Computação/
    ├── Estrutura CC.md                 ← Conteúdo principal
    └── Estrutura CC/                    ← Pasta com mesmo nome
        ├── Atividades Extracurriculares.md
        ├── Complementares Flexíveis.md
        └── assets/
            └── grade.png
```

**O que acontece:**

1. Ao acessar `/guias/ciencia-da-computacao/estrutura-cc`:
   - Mostra o conteúdo de `Estrutura CC.md`
   - **Adiciona automaticamente** uma seção "Conteúdo relacionado" com links para as sub-páginas

**Estrutura CC.md:**

```markdown
# Estrutura do Curso de Ciência da Computação

Este guia apresenta a estrutura curricular do curso.

## Sobre a Estrutura

A estrutura do curso é composta por...
```

**Resultado na página:**

```markdown
# Estrutura do Curso de Ciência da Computação

Este guia apresenta a estrutura curricular do curso.

## Sobre a Estrutura

A estrutura do curso é composta por...

## Conteúdo relacionado

- [Atividades Extracurriculares](/guias/ciencia-da-computacao/estrutura-cc/atividades-extracurriculares)
- [Complementares Flexíveis](/guias/ciencia-da-computacao/estrutura-cc/complementares-flexiveis)
```

### Exemplo 3: Apenas Sub-conteúdo (Sem Arquivo Principal)

**Objetivo:** Criar categoria de ferramentas sem descrição própria

**Estrutura:**

```
centro-de-informatica/
└── 3 - Ferramentas/
    └── Desenvolvimento/                ← Pasta SEM .md principal
        ├── Git.md
        ├── Docker.md
        └── VS Code.md
```

**O que acontece:**
Ao acessar `/guias/3-ferramentas/desenvolvimento`, o sistema **gera automaticamente**:

```markdown
# Desenvolvimento

## Conteúdo relacionado

- [Git](/guias/3-ferramentas/desenvolvimento/git)
- [Docker](/guias/3-ferramentas/desenvolvimento/docker)
- [VS Code](/guias/3-ferramentas/desenvolvimento/vs-code)
```

### Exemplo 4: Estrutura com Ordenação Numérica

**Estrutura:**

```
centro-de-informatica/
└── 1 - Grupos/
    ├── 0 - Introdução.md
    ├── 1 - Laboratórios.md
    ├── 2 - Ligas Acadêmicas.md
    └── 3 - Grupos de Estudo.md
```

**Benefício:** Os números no início garantem a ordem desejada na navegação.

### Exemplo 5: Guia com Imagens

**Estrutura:**

```
centro-de-informatica/
└── 2 - Informações/
    ├── Transporte.md
    └── Transporte/
        └── assets/
            ├── mapa-rotas.png
            └── horarios.png
```

**Transporte.md:**

```markdown
# Transporte

![Mapa de Rotas](./Transporte/assets/mapa-rotas.png)

## Horários

![Horários](./Transporte/assets/horarios.png)

Informações sobre transporte público...
```

## 🔗 Links Internos

Ao criar links para outras páginas do guia, use **caminhos absolutos** começando com `/guias/`:

```markdown
Veja mais sobre [Laboratórios](/guias/1-grupos/laboratorios)

Para saber sobre o PET, acesse [este link](/guias/1-grupos/pet)

Confira informações sobre [Sobre o Curso](/guias/ciencia-da-computacao/0-sobre-o-curso)
```

## 🖼️ Imagens e Recursos

### Opção 1: Pasta de Imagens ao Lado do .md

```
cadeiras/
├── Cálculo I.md
└── Cálculo I/
    └── imagens/
        └── grafico.png
```

```markdown
![Gráfico](./Cálculo I/imagens/grafico.png)
```

### Opção 2: Pasta Compartilhada

```
centro-de-informatica/
├── assets/
│   └── imagens/
│       └── logo-ci.png
└── 0 - Bem Vindo/
    └── 1 - Introdução.md
```

```markdown
![Logo CI](../assets/imagens/logo-ci.png)
```

## ✅ Checklist para Novo Conteúdo

Antes de fazer commit, verifique:

- [ ] A pasta do centro usa kebab-case (ex: `centro-de-informatica`)
- [ ] Os arquivos `.md` têm nomes descritivos e amigáveis
- [ ] O conteúdo está em Markdown válido
- [ ] Links internos usam caminhos absolutos começando com `/guias/`
- [ ] Imagens (se houver) estão com caminhos relativos corretos
- [ ] O conteúdo está revisado e sem erros ortográficos
- [ ] Se tem sub-conteúdo, a pasta tem o mesmo nome que o arquivo principal
- [ ] Se usar numeração para ordenação, use o formato `N - Nome` (ex: `0 - Bem Vindo`)

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

## 💡 Dicas e Boas Práticas

### 1. Nomes Descritivos

Use nomes que deixem claro o conteúdo:

- ✅ `Introdução ao Curso.md`
- ✅ `Como Escolher Cadeiras Optativas.md`
- ❌ `Intro.md`
- ❌ `Info.md`

### 2. Organize por Tópico

Agrupe conteúdos relacionados em pastas:

```
ferramentas/
├── Editores de Código/
│   ├── VS Code.md
│   ├── IntelliJ.md
│   └── Vim.md
└── Controle de Versão/
    ├── Git.md
    └── GitHub.md
```

### 3. Use Hierarquia com Moderação

Não crie hierarquias muito profundas. Idealmente, limite-se a 3-4 níveis.

### 4. Conteúdo Principal + Sub-conteúdo

Use a combinação de arquivo principal + pasta para criar índices ricos:

- O arquivo `.md` principal tem visão geral
- Os sub-conteúdos têm detalhes específicos

## 📞 Dúvidas?

Se tiver dúvidas sobre como organizar o conteúdo ou onde adicionar um guia específico, abra uma issue nesse repositório ou entre em contato com a equipe do Aquário.

---

**Mantido pela comunidade Aquário UFPB** 🐟
