# Visão Robótica - ECT/UFRN

Slides da disciplina de Visão Robótica, escritos em Quarto Markdown e publicados como apresentações RevealJS no GitHub Pages.

## Estrutura

- `docs/_quarto.yml`: configuração compartilhada das apresentações.
- `docs/slides/aula_template/aula_template.qmd`: modelo de aula com os elementos mais usados.
- `docs/README.md`: índice do site publicado.
- `docs/assets/`: identidade visual institucional.

## Pré-visualização e publicação

Execute os comandos a partir da pasta `docs`:

```sh
quarto preview slides/aula_template/aula_template.qmd
quarto render
```

Na instalação atual desta máquina, o Quarto 1.2 inclui um Pandoc para Intel que não executa neste Mac. Até atualizar o Quarto, use os executáveis ARM disponíveis:

```sh
QUARTO_DENO=/Applications/quarto/bin/tools/deno-aarch64-apple-darwin/deno QUARTO_PANDOC=/usr/local/bin/pandoc quarto render
```

O HTML das aulas e as dependências geradas em `docs/site_libs/` devem ser versionados junto com os arquivos `.qmd`. O Quarto também cria um `docs/index.html` de redirecionamento; ele é ignorado para que o GitHub Pages publique `docs/README.md` como página inicial com o tema Jekyll. No GitHub, configure Pages para publicar a pasta `/docs` da branch principal. O repositório previsto é `ect-comp/visao_robotica`.

Para criar uma aula, copie a pasta `aula_template`, renomeie o arquivo `.qmd`, substitua os exemplos e inclua o link em `docs/README.md`.
