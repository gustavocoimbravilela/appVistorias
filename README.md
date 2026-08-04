# App de Vistorias — pacote instalável (PWA)

Arquivos:
- index.html ......... o app
- manifest.json ...... identidade do app (nome, ícone, cor) para instalar
- service-worker.js .. faz o app abrir offline
- icon-192.png / icon-512.png ... ícones

## Testar no computador (rápido)
1. Abra o terminal nesta pasta.
2. Rode:  python -m http.server
3. Abra:  http://localhost:8000
   (o IndexedDB e o service worker só funcionam por um endereço, não em file://)

## Publicar no Firebase Hosting (endereço próprio + instalável no celular)
Use uma conta Google PESSOAL (fora da organização).

1. Instale o Node.js (uma vez).
2. No terminal:  npm install -g firebase-tools
3. Faça login:   firebase login
4. Nesta pasta:  firebase init hosting
   - "Use an existing project" ou crie um novo no console do Firebase.
   - Public directory:  .   (ponto — a pasta atual)
   - Single-page app:   No
   - Não sobrescreva o index.html se ele perguntar.
5. Publique:     firebase deploy
6. O terminal mostra a URL (https://SEU-PROJETO.web.app). Abra no celular.

## Instalar no celular
- Android (Chrome): abra a URL e toque em "Instalar app" (ou menu > Adicionar à tela inicial).
- iPhone (Safari): abra a URL, toque em Compartilhar > "Adicionar à Tela de Início".
