# Guias do Aquário

Esse repositório contém o conteúdo dos guias do Aquário UFPB, organizados por curso.

## 📁 Estrutura de Pastas

A estrutura de pastas determina como os guias serão organizados no site. Com a nova estrutura, você pode usar **nomes elegantes e legíveis** para seus arquivos!

```
aquario-guias/
├── ciencia-da-computacao/
│   ├── bem-vindo/
│   │   ├── Sobre o Curso.md
│   │   └── Grade Curricular.md
│   ├── cadeiras/
│   │   ├── Principais Cadeiras.md
│   │   └── Principais Cadeiras/
│   │       ├── Cálculo I.md
│   │       ├── Programação I.md
│   │       └── Estrutura de Dados.md
│   └── laboratorios/
│       └── LAICO.md
├── ciencias-de-dados-e-inteligencia-artificial/
│   └── ...
└── engenharia-da-computacao/
    └── ...
```

## 🗂️ Hierarquia no Site

A estrutura de pastas é mapeada para URLs da seguinte forma:

```
/guias/{curso}/{guia}/{secao}/{subsecao}
```

### Níveis:

1. **Curso** (nível 1): Nome do curso (pasta raiz - **apenas essa usa kebab-case**)
   - Exemplo: `ciencia-da-computacao`
   - URL: `/guias/ciencia-da-computacao`

2. **Guia** (nível 2): Categoria principal do guia (pasta)
   - Exemplo: `bem-vindo`, `cadeiras`, `laboratorios`
   - URL: `/guias/ciencia-da-computacao/bem-vindo`

3. **Seção** (nível 3): Arquivo `.md` com nome amigável
   - Exemplo: `Sobre o Curso.md`, `Principais Cadeiras.md`
   - URL: `/guias/ciencia-da-computacao/bem-vindo/sobre-o-curso` (slug gerado automaticamente!)

4. **Subseção** (nível 4): Arquivo `.md` dentro de uma pasta de seção
   - Exemplo: `Cálculo I.md`, `Programação I.md`
   - URL: `/guias/ciencia-da-computacao/cadeiras/principais-cadeiras/calculo-i`

## ✨ Nova Estrutura - O que mudou?

### Antes (estrutura antiga ❌):

```
cadeiras/
└── principais-cadeiras/
    └── content.md              # Nome genérico
```

### Agora (estrutura nova ✅):

```
cadeiras/
└── Principais Cadeiras.md      # Nome elegante e legível!
```

### Benefícios:

- ✅ **Nomes legíveis**: Use espaços, acentos e maiúsculas
- ✅ **Mais intuitivo**: O nome do arquivo é exatamente o que você quer mostrar
- ✅ **Slugs automáticos**: O sistema converte "Cálculo I.md" → URL `calculo-i`
- ✅ **Menos aninhamento**: Não precisa de `pasta/content.md`, só `Nome do Arquivo.md`

## ✍️ Como Adicionar Novo Conteúdo

### 1. Escolha o Curso

Navegue até a pasta do curso onde deseja adicionar conteúdo:

- `ciencia-da-computacao/`
- `ciencias-de-dados-e-inteligencia-artificial/`
- `engenharia-da-computacao/`

⚠️ **Atenção**: Apenas os **nomes de curso** devem usar kebab-case (tudo minúsculo com hífens).

### 2. Crie a Estrutura de Pastas (se necessário)

Crie as pastas necessárias seguindo a hierarquia:

```bash
# Exemplo: Adicionar conteúdo sobre Git no curso de Ciência da Computação
mkdir -p ciencia-da-computacao/ferramentas
```

### 3. Crie o Arquivo Markdown com Nome Elegante

Crie um arquivo `.md` com um **nome descritivo e amigável**:

```bash
# Use espaços, acentos e maiúsculas normalmente!
touch "ciencia-da-computacao/ferramentas/Controle de Versão com Git.md"
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

**Apenas para pastas de CURSO (nível raiz):**

- Use **kebab-case** (palavras separadas por hífen)
- Use apenas letras minúsculas
- Evite caracteres especiais e acentos

✅ **Correto para cursos:**

- `ciencia-da-computacao`
- `ciencias-de-dados-e-inteligencia-artificial`
- `engenharia-da-computacao`

**Para outras pastas (guias):**

- Use nomes descritivos simples
- Pode ser kebab-case ou palavras simples
- Exemplos: `bem-vindo`, `cadeiras`, `laboratorios`, `ferramentas`

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

**Objetivo:** Criar guia sobre o LAICO

**Estrutura:**

```
ciencia-da-computacao/
└── laboratorios/
    └── LAICO.md
```

**URL resultante:** `/guias/ciencia-da-computacao/laboratorios/laico`

**LAICO.md:**

```markdown
# LAICO - Laboratório de Aplicações de Informática Avançada

## Sobre o LAICO

O LAICO é um laboratório...

## Horários de Funcionamento

- Segunda a Sexta: 8h às 18h
- Sábado: 8h às 12h
```

### Exemplo 2: Conteúdo com Sub-conteúdo

**Objetivo:** Criar seção sobre cadeiras principais com detalhes de cada uma

**Estrutura:**

```
ciencia-da-computacao/
└── cadeiras/
    ├── Principais Cadeiras.md          ← Conteúdo principal
    └── Principais Cadeiras/            ← Pasta com mesmo nome
        ├── Cálculo I.md
        ├── Programação I.md
        └── Estrutura de Dados.md
```

**O que acontece:**

1. Ao acessar `/guias/ciencia-da-computacao/cadeiras/principais-cadeiras`:
   - Mostra o conteúdo de `Principais Cadeiras.md`
   - **Adiciona automaticamente** uma seção "Conteúdo relacionado" com links para as sub-páginas

**Principais Cadeiras.md:**

```markdown
# Principais Cadeiras do Curso

Este guia apresenta as disciplinas fundamentais do curso de Ciência da Computação.

## Sobre as Disciplinas

As cadeiras principais formam a base do conhecimento necessário...
```

**Resultado na página:**

```markdown
# Principais Cadeiras do Curso

Este guia apresenta as disciplinas fundamentais do curso de Ciência da Computação.

## Sobre as Disciplinas

As cadeiras principais formam a base do conhecimento necessário...

## Conteúdo relacionado

- [Cálculo I](/guias/ciencia-da-computacao/cadeiras/principais-cadeiras/calculo-i)
- [Programação I](/guias/ciencia-da-computacao/cadeiras/principais-cadeiras/programacao-i)
- [Estrutura de Dados](/guias/ciencia-da-computacao/cadeiras/principais-cadeiras/estrutura-de-dados)
```

### Exemplo 3: Apenas Sub-conteúdo (Sem Arquivo Principal)

**Objetivo:** Criar categoria de ferramentas sem descrição própria

**Estrutura:**

```
ciencia-da-computacao/
└── ferramentas/
    └── Desenvolvimento/                ← Pasta SEM .md principal
        ├── Git.md
        ├── Docker.md
        └── VS Code.md
```

**O que acontece:**
Ao acessar `/guias/ciencia-da-computacao/ferramentas/desenvolvimento`, o sistema **gera automaticamente**:

```markdown
# Desenvolvimento

## Conteúdo relacionado

- [Git](/guias/ciencia-da-computacao/ferramentas/desenvolvimento/git)
- [Docker](/guias/ciencia-da-computacao/ferramentas/desenvolvimento/docker)
- [VS Code](/guias/ciencia-da-computacao/ferramentas/desenvolvimento/vs-code)
```

### Exemplo 4: Estrutura Completa de Cadeiras por Período

**Estrutura:**

```
ciencia-da-computacao/
└── cadeiras/
    ├── Primeiro Período.md
    ├── Primeiro Período/
    │   ├── Cálculo I.md
    │   ├── Programação I.md
    │   └── Introdução à Computação.md
    ├── Segundo Período.md
    └── Segundo Período/
        ├── Cálculo II.md
        ├── Programação II.md
        └── Estrutura de Dados.md
```

**Cálculo I.md (exemplo de sub-conteúdo):**

```markdown
# Cálculo I

## Sobre a Disciplina

Disciplina de cálculo diferencial e integral, fundamental para a formação...

## Ementa

- Limites
- Derivadas
- Integrais
- Aplicações

## Dicas de Estudo

1. Pratique bastante exercícios
2. Assista às video-aulas complementares
3. Participe das monitorias

## Professores

- Prof. João Silva
- Prof. Maria Santos

## Recursos Úteis

- [Khan Academy - Cálculo](https://www.khanacademy.org/math/calculus-1)
- [MIT OpenCourseWare](https://ocw.mit.edu/)
```

### Exemplo 5: Guia com Imagens

**Estrutura:**

```
ciencia-da-computacao/
└── laboratorios/
    ├── LAICO.md
    └── LAICO/
        └── imagens/
            ├── foto-lab.jpg
            └── mapa-localizacao.png
```

**LAICO.md:**

```markdown
# LAICO

![Foto do Laboratório](./LAICO/imagens/foto-lab.jpg)

## Localização

![Mapa](./LAICO/imagens/mapa-localizacao.png)

O laboratório fica no prédio...
```

## 🔗 Links Internos

Ao criar links para outras páginas do guia, use **caminhos absolutos** começando com `/guias/`:

```markdown
Veja mais sobre [Programação I](/guias/ciencia-da-computacao/cadeiras/primeiro-periodo/programacao-i)

Para saber sobre o LAICO, acesse [este link](/guias/ciencia-da-computacao/laboratorios/laico)
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
ciencia-da-computacao/
├── assets/
│   └── imagens/
│       └── logo-cin.png
└── bem-vindo/
    └── Sobre o Curso.md
```

```markdown
![Logo CIn](../assets/imagens/logo-cin.png)
```

## 📋 Comparação Rápida: Antes vs Agora

| Aspecto             | Estrutura Antiga ❌         | Estrutura Nova ✅                 |
| ------------------- | --------------------------- | --------------------------------- |
| **Nome do arquivo** | `content.md` (sempre igual) | `Nome Descritivo.md` (legível)    |
| **Espaços**         | Não permitido               | ✅ Permitido                      |
| **Acentos**         | Não permitido               | ✅ Permitido                      |
| **Maiúsculas**      | Não permitido               | ✅ Permitido                      |
| **Aninhamento**     | `pasta/subpasta/content.md` | `pasta/Título Bonito.md`          |
| **Slugs**           | Nome da pasta               | Gerado automaticamente do arquivo |

### Migração de Conteúdo Antigo

Se você tem conteúdo na estrutura antiga, pode migrar assim:

**Antes:**

```
cadeiras/
└── calculo-i/
    └── content.md
```

**Depois:**

```
cadeiras/
└── Cálculo I.md
```

Basta **renomear e mover** o `content.md` para o nível acima com um nome descritivo!

## ✅ Checklist para Novo Conteúdo

Antes de fazer commit, verifique:

- [ ] A pasta do curso usa kebab-case (ex: `ciencia-da-computacao`)
- [ ] Os arquivos `.md` têm nomes descritivos e amigáveis
- [ ] O conteúdo está em Markdown válido
- [ ] Links internos usam caminhos absolutos começando com `/guias/`
- [ ] Imagens (se houver) estão com caminhos relativos corretos
- [ ] O conteúdo está revisado e sem erros ortográficos
- [ ] Se tem sub-conteúdo, a pasta tem o mesmo nome que o arquivo principal

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
