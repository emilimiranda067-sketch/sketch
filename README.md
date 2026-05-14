Deploy do meu site

on:
push:
 branches: ["main"] # Roda sempre que voce salvar algo na mnain

 permissions:
  contents: read
  pages: write
  id-token: write

jobs:
 build-and-deploy:
 runs-on: ubuntu-latest
 steps:
 - name: Checkout (Baixa seu código)
   uses: actions/checkout@v4

   - name: Setup Pages (Configura o ambiente)
       uses: actions/upload-pages-artifact@v3
      with
     path: '.' # O ponto significa que seu index.html está na raiz

     - name: deployment
     - uses: actions/deploy-pages@v4
