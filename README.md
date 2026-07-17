# Base de Dados do Projeto EcoMuseu do Boné

Este repositório armazena e organiza o acervo digital do EcoMuseu do Boné, projeto de extensão da Universidade Tecnológica Federal do Paraná (UTFPR), campus Apucarana-PR.

A base de dados foi estruturada para disponibilizar conteúdos históricos e culturais relacionados ao universo do boné, permitindo sua utilização em aplicações digitais voltadas à consulta e à acessibilidade do acervo.

---

## Objetivo

O objetivo deste repositório é centralizar os dados e arquivos digitais do EcoMuseu do Boné, mantendo uma estrutura organizada e padronizada para o armazenamento de conteúdos e seus respectivos metadados.

---

## Ferramentas e Tecnologias

- [Sveltia CMS](https://github.com/sveltia/sveltia-cms)
- JSON
- Arquivos digitais

---

## Estrutura da Base de Dados

A base de dados está organizada em duas categorias principais:

- **Dados:** arquivos digitais que compõem o acervo;
- **Metadados:** informações descritivas e estruturais relacionadas aos conteúdos.

### Representação da estrutura hierárquica

```text
Base de dados EcoMuseu/
├── Dados/
│   ├── Artigos/
│   │   ├── artigo_2.pdf
│   │   └── ...
│   └── Audios/
│       ├── audio_2.wav
│       └── ...
└── Metadados/
    ├── metadados_principal.json
    ├── metadados_conteudos/
    │   ├── metadados_conteudo_2.json
    │   └── ...
    └── metadados_WCAG.json
```

Na Figura acima, o “metadados_principal.json” contém a chave-primária que identifica unicamente 
cada arquivo selecionado do acervo. O “artigo_2.pdf” é um arquivo do acervo. Para a sua inserção no site, 
o índice “2” desse arquivo é inserido como chave-estrangeira no arquivo “metadados_principal.json”. A seguir o índice “2” é inserido como chave-primária no arquivo
“metadados_conteudo_2.json”. Todo conteúdo textual possui um correspondente em áudio. O
conteúdo em áudio também está inserido no “metadados_principal.json”. Ambos os arquivos
utilizam o mesmo identificador de chave estrangeira para referenciar o conteúdo.

---

#### Dados 
Os dados são os arquivos puros vindos do Ecomuseu do Boné, são distribuidos conforme as seguintes categorias:
- Artigo;
- Carta;
- Depoimento;
- Entrevista;
- Fotografia;
- Legenda;
- Logotipo;
- Notícia;
- Ofício;
- Outros Conteúdos;
- Publicidade;
- Selo.

---
  
#### Metadados

Os metadados são armazenados em arquivos JSON e têm como objetivo descrever e organizar os conteúdos presentes no acervo.

A estrutura de metadados contempla informações como:

- Identificação dos conteúdos;
- Descrição dos arquivos (autor, ano, conteúdo...) ;
- Informações relacionadas à acessibilidade;
  - Critérios e requisitos baseados nas diretrizes WCAG.

#### Acessibilidade

A organização dos dados considera aspectos relacionados à acessibilidade digital, especialmente os critérios estabelecidos pelas diretrizes Web Content Accessibility Guidelines (WCAG).

O arquivo metadados_WCAG.json é utilizado para armazenar informações relacionadas aos critérios de acessibilidade aplicáveis aos conteúdos.

---

## Gerenciamento do Conteúdo

A manutenção e a edição dos metadados podem ser realizadas por meio do Sveltia CMS, permitindo a organização dos conteúdos sem a necessidade de editar diretamente os arquivos JSON.

---

## Licença

Este repositório foi desenvolvido como parte do meu TCC. O conteúdo do EcoMuseu do Boné pertence aos seus respectivos mantenedores.

---
