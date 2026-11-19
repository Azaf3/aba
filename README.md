# ABA Alimentos e Distribuição: site de pedidos

Site de pedidos online da ABA Alimentos e Distribuição (Brasília/DF). O cliente escolhe uma cesta básica pronta ou monta uma compra sob demanda, o frete é calculado pelo CEP e o pedido chega pronto no WhatsApp da empresa.

🔗 **No ar:** https://azaf3.github.io/aba/

![Tela inicial do site de pedidos](docs/screenshot.jpg)

## Por que existe

Fechar um pedido só pelo WhatsApp pede muita troca de mensagem: endereço, itens, frete. O site junta tudo num fluxo só e entrega o pedido já organizado pra confirmar.

## Funcionalidades

- **Dois tipos de pedido:** cestas básicas com tamanho e preço fechados, ou compra sob demanda
- **Frete automático:** busca o endereço pelo CEP (BrasilAPI / ViaCEP), geolocaliza (Nominatim) e calcula a distância até o depósito
- **Orçamento em PDF:** gerado no navegador com jsPDF
- **Pedido no WhatsApp:** monta a mensagem formatada e abre o WhatsApp pronta pra enviar
- **Cadastro lembrado:** os dados do cliente ficam salvos no navegador dele, sem precisar preencher de novo
- **Limpeza automática:** depois do envio, se ninguém confirmar em 10 minutos, a ficha é limpa sozinha (útil em aparelho compartilhado)

## Stack

HTML, CSS e JavaScript puro num arquivo só (`index.html`), sem framework e sem build. Dados do cliente em `localStorage`, PDF com jsPDF e APIs públicas de CEP e geocodificação. Publicado no GitHub Pages.

## Rodando localmente

Abra o `index.html` no navegador. Não precisa instalar nada.
