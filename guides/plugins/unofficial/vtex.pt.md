# VTEX

## O que é VTEX?

VTEX é uma **plataforma e-commerce para sua loja virtual** para sua loja virtual, que permite processar pagamentos através do Mercado Pago.

Você poderá oferecer aos seus clientes a possibilidade de pagar com [cartão de crédito](#bookmark_condição_de_pagamento_cartão_de_crédito) e [boleto bancário](#bookmark_condição_de_pagamento_boleto_bancário) no próprio [checkout da sua loja ou redirecionado para o site do Mercado Pago](#bookmark_condição_de_pagamento_checkout_mercado_pago).


## Etapas para configurar

Os **passos para começar a operar com Mercado Pago**, são os seguintes:

1. Crie uma [conta de vendedor](https://www.mercadopago.com.br/activities) no Mercado Pago caso ainda não tenha uma.
2. Cadastre uma afiliação de gateway de pagamento com o "Mercado Pago".
3. Configure as condições de pagamento Mercado Pago.
4. Configure device fingerprint.

## Criando afiliação de gateway Mercado Pago

Para criar uma **afiliação de gateway de pagamento com o Mercado Pago**, siga os passos abaixo:

1. No painel de administração de sua loja, acesse Configurações do módulo de pagamentos.
2. Na aba Afiliações de Gateways, clique no botão "+".
3. Clique no conector MercadoPagoV1.
4. Preencha os campos correspondentes e clique em "Salvar".

| Campos | Dados necessários |
|-------------------------------------------|---------------------------------------------------------------------------------------|
| Nome da afiliação | Defina o nome que identificará a sua Afiliação. |
| OAuth login | Não é utilizado. Deixe-o como está. |
| PublicKey | Refere-se às [credenciais da sua conta](#bookmark_credenciais_de_sua_conta_mercado_pago) do Mercado Pago. Complete com sua chave pública. |
| AccessToken | Refere-se às [credenciais da sua conta](#bookmark_credenciais_de_sua_conta_mercado_pago) do Mercado Pago. Complete com sua chave privada. |
| RefreshToken | Deixar em branco. |
| ExpiredTokenIn | Deixar em branco. |
| Merchant Account Id | Deixar em branco. |
| Processing Mode | Escolha aggregator, modo de processamento a partir de MercadoPagoV1. |
| CountryName | Selecione o país da sua loja. |
| SoftDescriptor | Indique o nome que vai aparecer para identificar a transação realizada na sua loja. |
| Description | Escreva uma breve descrição do seu negócio (o preenchimento é opcional). |
| CategoryId | Escolha a categoria dos produtos que você vende na sua loja. |
| Financial Institution | Deixar em branco. Preenchimento apenas se sua loja operar do "Chile". |
| External Installments | Sim. Utilização das condições de parcelamento diretamente de sua conta Mercado Pago. |
| Antifraud | Informe se deseja usar um antifraude. |
| Time Zone | Indique a região que define seu horário local. |
| OrderExpirationHours | Defina por quantas horas o sistema deve checar o status do pedido antes de sua expiração. Quando essa opção não é preenchida, é adotado o padrão de 192 horas. |
| MaxInstallments | Escolha a quantidade máxima de parcelas enviadas ao Mercado Pago. |
| Categoria Principal | Escolha a categoria que mais se encaixa com sua loja. |
| Captura de segurança antecipada | Você pode desativar a função ou escolher em quanto tempo quer realizar a captura (depois da aprovação da transação e da análise do antifraude). |
<br>
    ![Setting affiliation in VTEX](/images/vtex/vtex_afiliacao_gateway_1.gif)

E pronto! Sua afiliação com o Mercado Pago já está ativa!

## Configurar condições de pagamento

Após ter criado sua afiliação com o Mercado Pago, você tem a opção de oferecer em sua loja pagamentos com [cartão de crédito](#bookmark_condição_de_pagamento_cartão_de_crédito), [boleto bancário](#bookmark_condição_de_pagamento_boleto_bancário) e também pagamentos via [Checkout Mercado Pago](#bookmark_condição_de_pagamento_checkout_mercado_pago).

### Condição de pagamento cartão de crédito

Para criar uma **condição de pagamento cartão de crédito** utilizando sua afiliação com o Mercado Pago, siga os passos abaixo:

1. No painel de administração de sua loja, acesse "Configurações" do módulo de pagamentos.
2. Na aba "Condições de pagamento", clique no botão "+".
3. Na seção "Cartão de Crédito", escolha qual bandeira irá adicionar ao meio de pagamento.
4. Informe o "Nome da regra" para facilitar a identificação e ative a condição de pagamento no campo "Status".
5. Informe sua afiliação com o Mercado Pago, no campo "Processar com a afiliação".
6. Em opções de parcelamento, escolha parcelamento "Automático", onde utiliza as condições de **parcelamento diretamente de sua conta Mercado Pago**.
7. Clique em "Salvar".
<p>&nbsp;</p>
    ![Setting payments in VTEX](/images/vtex/vtex_condicao_pagamento_cartao_2.gif)
<p>&nbsp;</p>

### Condição de pagamento boleto bancário

Para criar uma **condição de pagamento [boleto bancário](#bookmark_condições_de_pagamentos_offline) utilizando sua afiliação com o Mercado Pago**, siga os passos abaixo:

1. No painel de administração de sua loja, acesse "Configurações" do módulo de pagamentos.
2. Na aba "Condições de pagamento", clique no botão "+".
3. Na seção "Boleto", escolha "Boleto Bancário" para adicionar ao meio de pagamento.
4. Informe o "nome da regra" para facilitar a identificação e ative a condição de pagamento no campo "Status".
5. Informe sua afiliação com o Mercado Pago, no campo "Processar com a afiliação".
6. Clique em "Salvar".
<p>&nbsp;</p>
    ![Setting payments in VTEX](/images/vtex/vtex_condicao_pagamento_boleto_3.gif)
<p>&nbsp;</p>

### Condição de pagamento Checkout Mercado Pago

**O comprador será redirecionado ao site do Mercado Pago** e uma vez finalizado o processo, voltará para sua loja.

Para criar essa condição de pagamento, siga os passos abaixo:

1. No painel de administração de sua loja, acesse "Configurações" do módulo de pagamentos.
2. Na aba "Condições de pagamento", clique no botão "+".
3. Na seção "Outro", selecione a condição de pagamento "Mercado Pago".
4. Informe o "Nome da regra" para facilitar a identificação e ative a condição de pagamento no campo "Status".
5. Informe sua afiliação com o Mercado Pago, no campo "Processar com a afiliação".
6. Clique em "Salvar".
<p>&nbsp;</p>
    ![Setting payments in VTEX](/images/vtex/vtex_condicao_redirect_4.gif)
<p>&nbsp;</p>

> As mudanças nas Condições de pagamento podem levar até 10 minutos para serem aplicadas.

## Configurando o parcelamento em sua conta Mercado Pago

1. Acesse sua [conta Mercado Pago](https://www.mercadopago.com.br/business/) e clique em "Seu negócio"
2. Clique na opção "Configurações", navegue até o campo "Oferecer parcelas sem acréscimo" e clique em "Ativar".
3. Escolha "Quantas parcelas você quer oferecer?" e clique em "Ativar" para confirmar as alterações.
<p>&nbsp;</p>
    ![Setting affiliation in VTEX](/images/vtex/vtex-account-installment-7.gif)
<p>&nbsp;</p>
E pronto! Você está oferecendo parcelamento sem acréscimo, assumindo as tarifas de parcelamento que você configurou.

## Obtenha aprovação mais rápida enviando o device fingerprint

O Mercado Pago possui suas próprias ferramentas de prevenção de fraudes. Sempre que possível, **recomendamos que envie informações sobre o comportamento do cliente para detectar movimentos incomuns e evitar transações fraudulentas**. Não se preocupe, cuidamos dos dados de seus clientes e não os compartilhamos com ninguém.

Para configurar o device fingerprint, siga os passos abaixo:

1. No painel de administração de sua loja, acesse Checkout do módulo "Configurações da Loja".
2. Clique no ícone "editar", referente a configuração de seu site.
3. Acessar a aba "Código" e clique em "checkout5-custom.js" no módulo arquivos.
4. Copiar e colar o seguinte código e clique em "Salvar".
<p>&nbsp;</p>

```javascript
var script = document.createElement("script");
script.src = "https://www.mercadopago.com/v2/security.js";
script.setAttribute("output","vtex.deviceFingerprint");
script.setAttribute("view","checkout");
document.body.appendChild(script);
```
<br>
    ![Setting deviceid in VTEX](/images/vtex/vtex_deviceid_6.gif)

## Credenciais de sua conta Mercado Pago

Você conta com dois pares de chaves para conectar-se com a VTEX, um para ambiente de testes e outro para ambiente de produção. Estas chaves podem ser encontradas na seção [credenciais da sua conta](https://www.mercadolibre.com/jms/mlb/lgz/login?platform_id=mp&go=https://www.mercadopago.com/mlb/account/credentials).

> Antes de iniciar sua operação em produção, assegure se de preencher o formulário 'Ir para produção'. Caso já tenha realizado este passo o link não será apresentado.

## Entendendo sobre os principais logs da VTEX

**Os logs permitem revisar a informação que retorna Mercado Pago** e VTEX expõe para poder ter um maior entendimento de o que ocorreu com uma transação. Também em caso de modificação ou ativação de novos meios de pagamento, nos dão a possibilidade de poder validar se tudo está funcionando segundo o previsto. Por último, provém um maior entendimento às equipes comerciais para que possam dar um melhor suporte aos vendedores e converter se em uma primeira instância de suporte.

Acesse a transação da VTEX, então busque pelo LOG que contenha o status response e clique em _ver mais_.

Os dados mais significativos são os seguintes:

| Campo | Dado | Descrição |
|-------------------|-------------------------------------|--------------------------------------------|
| ID | 10302316 | Número da transação de Mercado Pago. |
| Payment_method_id | visa | Meio de pagamento. |
| Payment_type_id | credit_card | Meio de pagamento. |
| Status | authorized | Estado do pagamento. |
| Status_detail | pending_capture | Detalhe do estado do pagamento. |
| External_reference | 503451 | Identificador da VTEX enviado a Mercado Pago. |
| First_six_digits | 450995 | Bin do cartão de crédito. |
| Processing_mode | agregador | Modo de processamento do pagamento. |

Quando confrontado com uma rejeição, é muito importante rever o `status_detail` que especifica o motivo do mesmo.

| Campo | Dado | Descrição |
|-------------------|-------------------------------------|--------------------------------------------|
| Status | rejected | Pagamento rejeitado. |
| Status_detail | cc_rejected_other_reason | Rejeição do cartão de crédito, sem informação do motivo. |
| Status_detail | cc_rejected_call_for_authorize | Rejeição do cartão de crédito, o cliente deve ligar para autorizar o pagamento. |
| Status_detail | cc_rejected_insufficient_amount | Rejeição do cartão de crédito, o cliente não tem saldo suficiente disponível. |
| Status_detail | cc_rejected_high_risk | Rejeição de Mercado Pago, risco de fraude. |

> Para mais informação, visite o site [oficial da VTEX](https://help.vtex.com/).
