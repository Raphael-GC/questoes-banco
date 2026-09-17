# Imagens das questões

Cada questão pode ter 0 ou mais imagens — a lista `imagens_desc` no JSON (uma descrição por imagem, na ordem de exibição) substitui o antigo par `possui_imagem`/`imagem_desc` (que só suportava uma imagem por questão).

Nome de arquivo: `<id-da-questao>-<n>.png`, `n` de 1 até a quantidade de imagens daquela questão (mesma ordem de `imagens_desc`) — sempre numerado, mesmo quando a questão só tem uma imagem (`-1.png`), sem caso especial pra "a primeira".

Lista completa das questões que precisam de imagem, com a descrição do que cada uma deve mostrar: `questoes_precisam_imagem.md` na raiz do projeto.

Servidas pro app via GitHub raw (ver "Arquitetura do Questões", §04b — Imagens):

```
https://raw.githubusercontent.com/<usuario>/<repositorio>/main/files/images/<id-da-questao>-<n>.png
```

Não precisa listar as imagens em nenhum manifesto — o app monta essa URL sozinho a partir do id da questão e do índice da imagem.
