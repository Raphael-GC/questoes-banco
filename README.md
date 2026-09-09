# Imagens das questões

Uma imagem por questão com `possui_imagem: true` no JSON, nomeada exatamente `<id-da-questao>.png` — o mesmo valor do campo `id` daquela questão.

Lista completa das 68 pendentes, com a descrição do que cada imagem deve mostrar: `questoes_precisam_imagem.md` na raiz do projeto.

Servidas pro app via GitHub raw (ver "Arquitetura do Questões", §04b — Imagens):

```
https://raw.githubusercontent.com/<usuario>/<repositorio>/main/files/images/<id-da-questao>.png
```

Não precisa listar as imagens em nenhum manifesto — o app monta essa URL sozinho a partir do id da questão.
