# Site de Pedidos — Aba Cestas Básicas

Site para pedido online das cestas básicas da **Aba Cestas Básicas** (Brasília/DF), com cadastro de cliente, seleção de cestas por tamanho e envio do pedido formatado direto pro WhatsApp.

🔗 **Site no ar:** https://azaf3.github.io/aba/

---

## Funcionalidades

- **Cadastro do cliente** — nome, telefone, endereço, bairro, referência e forma de pagamento, salvo no navegador do próprio cliente (não precisa preencher de novo na próxima compra)
- **Validação de telefone** — formata automaticamente enquanto digita e avisa se faltar algum dígito
- **Catálogo de cestas** (P, M e G) — com foto, preço, peso, quantidade de itens e lista completa do que vem em cada uma
- **Seleção por quantidade** — contador (+/-) para cada tamanho de cesta, com resumo fixo mostrando total de itens e valor
- **Revisão do pedido** — antes de enviar, mostra um resumo com os dados do cliente e os itens escolhidos pra conferência
- **Envio direto pro WhatsApp** — monta a mensagem formatada e abre o WhatsApp já pronta pra enviar
- **Finalização automática** — depois do envio, pergunta se o pedido foi encaminhado; se ninguém responder em 10 minutos, limpa a ficha sozinho (evita ficar com dados do cliente anterior)
- **Botão "limpar ficha"** — disponível a qualquer momento, com confirmação, para apagar o cadastro salvo naquele aparelho

## Tecnologia

Arquivo único (`index.html`) — HTML, CSS e JavaScript puro, sem frameworks, sem build, sem backend. As imagens (fotos das cestas, logo, ícone) ficam embutidas em base64 dentro do próprio arquivo.

- **Poppins** / **DM Sans** / **JetBrains Mono** — tipografia (Google Fonts)
- **`localStorage`** — armazena o cadastro do cliente no navegador (por aparelho, não em nuvem)
- **wa.me** — link de envio direto pro WhatsApp com a mensagem pré-preenchida

## Estrutura

```
site-aba/
├── index.html   ← o site inteiro (única página)
└── README.md
```

```

| O que mudar | Onde |
|---|---|
| Preço de cada cesta | Campo `preco` de cada item em `CESTAS` |
| Itens de cada cesta | Array `itens` de cada item em `CESTAS` |
| Número de WhatsApp que recebe os pedidos | Constante `WHATSAPP_NUMERO` |
| Fotos das cestas / logo / ícone | Embutidas em base64 no campo `img` de cada cesta e nas tags `<img>` do cabeçalho — para trocar, gere uma nova imagem em base64 e substitua o valor |

## 🔒 Privacidade

Não existe banco de dados nem servidor: os dados do cliente ficam apenas no `localStorage` do navegador em que ele fez o pedido, isolados por aparelho — um cliente nunca tem acesso aos dados de outro. Em caso de uso em aparelho compartilhado (ex: tablet da loja), use o botão **"limpar ficha"** entre um atendimento e outro.

---

AZZZZ

