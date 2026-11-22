# Estoque (app Android)

App offline para controle de estoque: produtos, entradas (com preço de compra e fornecedor),
saídas, perdas, ajuste de contagem, alerta de estoque mínimo e lista de reposição.
Os dados ficam salvos no próprio celular.

## Gerar o APK (sem instalar nada)

1. Crie um repositório no GitHub e envie esta pasta inteira (incluindo `.github`).
2. Abra a aba **Actions** > **Gerar APK** > **Run workflow** (ou faça um push na branch `main`).
3. Quando terminar (uns 3 a 5 minutos), baixe o arquivo **estoque-apk** em *Artifacts*.
4. Descompacte, copie o `.apk` para o celular e instale (permita "fontes desconhecidas" se pedir).

## Gerar o APK no Android Studio

Abra esta pasta no Android Studio, aguarde a sincronização e use
**Build > Build APK(s)**.

## Onde mexer

- Telas e regras do app: `app/src/main/assets/index.html`
- Casca Android (WebView): `app/src/main/java/com/estoque/app/MainActivity.java`

## Observações

- O APK sai assinado com a chave de debug: serve para instalar direto, mas não para publicar na Play Store.
- Os dados ficam no armazenamento do app. Se desinstalar, perde tudo: use **Relatórios > Fazer backup** de vez em quando.
