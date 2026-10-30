# Minha Garagem de Minis

Protótipo de uma loja de miniaturas colecionáveis (escala 1:64) com **pré-venda, reserva com sinal por Pix, acompanhamento de pedido e painel do dono**.

> **A Minha Garagem de Minis é uma empresa fictícia.** Nome, logo, CNPJ, endereço, contatos e clientes são inventados para demonstração. Nenhum pagamento real é gerado.

## O que o protótipo mostra

- **Vitrine por coleção:** data de chegada prevista, preço por peça, percentual de sinal e vagas restantes, com linha do tempo das próximas chegadas.
- **Reserva em 4 etapas:** dados do cliente, resumo do contrato, Pix do sinal e confirmação.
- **Acompanhar pedido:** o cliente consulta com o código do pedido e os 4 últimos dígitos do WhatsApp, vê a linha do tempo, paga o saldo e pode pedir cancelamento (direito de arrependimento).
- **Painel do dono:** valores a receber e recebidos, filtros por situação, cobrança por WhatsApp com mensagem pronta, marcação de lote chegado, controle de estornos e cadastro de coleções.
- **Páginas legais:** privacidade (LGPD), termos da pré-venda e direito de arrependimento (CDC art. 49 e Decreto 7.962/2013).

## Como rodar

É um arquivo único, sem dependências. Abra o `index.html` no navegador. Os dados de exemplo ficam no `localStorage`, e o botão "Restaurar dados de exemplo" no painel limpa tudo.

## O que é demonstração e o que falta para produção

| Tema | Neste protótipo | Em produção |
| --- | --- | --- |
| Pix | QR Code ilustrativo e botão "Simular Pix recebido" | Cobrança Pix por API de um provedor (Mercado Pago, Asaas ou Efí) com webhook de confirmação |
| Pedidos | Salvos só no navegador de quem usa | Banco de dados no servidor |
| Painel | Aberto | Login com senha e verificação em duas etapas |
| Segredos | Nenhum | Chaves de API apenas no servidor, nunca na página |
| Logs | Nenhum | Registros de acesso conforme o Marco Civil da Internet |

## Aviso legal

Os textos de privacidade, termos e arrependimento são um **modelo de partida** e não substituem a revisão de um advogado ou contador. A política de privacidade descreve controles (HTTPS, login com verificação em duas etapas, registros de acesso) que só valem quando a versão de produção os implementar.

## Estrutura

```
index.html   página única: HTML, CSS e JavaScript
README.md    este arquivo
```

## Dados da loja fictícia

Ficam no objeto `STORE`, no começo do `<script>` do `index.html`. Para adaptar a outra loja, troque nome, razão social, CNPJ ou CPF, endereço, e-mail e WhatsApp, e substitua a logo na variável CSS `--logo`.

## Autor

Gylles de Assis Furtado · https://www.linkedin.com/in/gyllesassis/
