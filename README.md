# Jogo da memória tech

Jogo da memória com 12 cartas e 6 pares de emojis de tecnologia. O projeto
funciona diretamente no navegador, sem bibliotecas, fontes externas ou servidor.

## Estrutura

- `index.html` — estrutura, estilos e lógica do jogo em um único arquivo.

## Como jogar

Abra `index.html` diretamente no navegador. Use **Tab** para percorrer as cartas
e **Enter** ou **Espaço** para virá-las. Encontre os seis pares; o jogo mostra
as jogadas e o tempo e permite iniciar uma nova partida.

## Publicação no GitHub Pages

O workflow [`Publicar jogo no GitHub Pages`](.github/workflows/pages.yml)
publica somente `index.html`. Ele é executado quando há um push para `main` ou
quando iniciado manualmente em **Actions → Publicar jogo no GitHub Pages → Run
workflow**. O arquivo é copiado para um diretório temporário e enviado como
artefato do Pages; o `README.md` e os demais arquivos do repositório não são
publicados.

O GitHub Pages está configurado para usar **GitHub Actions** como origem do
build. O workflow usa permissões restritas ao job de publicação (`pages: write`
e `id-token: write`); não requer dependências ou servidor para o jogo.

Após uma execução concluída, o jogo ficará em
<https://andradezzzz.github.io/memoria-tech/>. Para verificar, confira a
execução em **Actions**, o deployment `github-pages` no ambiente do repositório
e abra a URL. O repositório e o site são públicos; não publique dados sensíveis
neste projeto.
