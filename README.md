# Banco de questões — Questões (app)

Fonte remota consumida pelo app Android [Questões](https://github.com/Raphael-GC/questoes-app): os `.json` por disciplina em `files/` e o `manifest.json` (contagens + versão) são a cópia pública de `app/src/main/assets/questoes/` daquele repositório — **a cada mudança no banco do app, sincronize os arquivos aqui e suba `manifest.json.versao`**, senão a tela "Atualizar banco" do app não vê a mudança.

## `manifest.json`

- `versao` — inteiro, incrementado a cada atualização de conteúdo. O app guarda a última versão aplicada e só baixa/reimporta quando a remota é maior.
- `total_questoes` / `disciplinas[].total_questoes` — só informativo (conferência rápida, não usado pelo app pra decidir nada).
- `concursos` — proveniência de cada prefixo de id (prova de origem, edital/portaria, observações) — histórico, não consumido pelo app.
- `simulados_ref` — os simulados por cargo são definidos no código do app (`SelecaoSimuladoScreen.kt`), não aqui.

## Imagens das questões

Cada questão pode ter 0 ou mais imagens — a lista `imagens_desc` no JSON (uma descrição por imagem, na ordem de exibição) substitui o antigo par `possui_imagem`/`imagem_desc` (que só suportava uma imagem por questão).

Nome de arquivo: `<id-da-questao>-<n>.png`, `n` de 1 até a quantidade de imagens daquela questão (mesma ordem de `imagens_desc`) — sempre numerado, mesmo quando a questão só tem uma imagem (`-1.png`), sem caso especial pra "a primeira".

Lista completa das questões que precisam de imagem, com a descrição do que cada uma deve mostrar: `questoes_precisam_imagem.md` na raiz do projeto.

Servidas pro app via GitHub raw (ver "Arquitetura do Questões", §04b — Imagens):

```
https://raw.githubusercontent.com/<usuario>/<repositorio>/main/files/images/<id-da-questao>-<n>.png
```

Não precisa listar as imagens em nenhum manifesto — o app monta essa URL sozinho a partir do id da questão e do índice da imagem.
