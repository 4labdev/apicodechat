  <p align="center">
  <img src="https://app.dispzap.com/brand-assets/logo.svg" alt="DispZap Whats Marketing" width="240" />
  <p align="center">Seja bem-vindo, aqui você vai encontrar materiais extras criados para dar um up na API Codechat</p>
  </p>

  <details>
<summary>Workflow que Habila CSAT</summary>

Para habilitar CSAT (Pesquisa de Satisfação ao Cliente) em seu Chatwoot, basta ir até o diretório `workflow-n8n` e baixar e importar o Workflow `CsatToChatwootCodechat.json`

PASSO 01: No NODE `ConsultaIDBanco` adicione suas credenciais do banco de dados Postgres

```bash
#host
localhost

#Database
chatwoot_production

#user
chatwoot

#Password
Adicone a senha do Postgres. Você encontra no arquivo
.env do chatwoot em /home/chatwoot/chatwoot/.env

```

PASSO 02: Vá até o NODE `SetMensagem`

```bash
#Vá até o campo value e procure pela variavél `#suaurlchatwoot` e adicione o endereço de instalação do seu chatwoot

https://app.chatwoot.com/survey/responses/{{ $node["ConsultaIDBanco"].json["uuid"] }}

```

# PASSO 03: Ajuste envio no NODE `SendMSGCodechat`

```bash
#Na URL onde ta escrito `#urlcodechat` adicione o endereço da api codechat. Em `#suainstancia` é o nome de sua caixa de entrada

```

### Hora de testar se tudo está correto!
Vai até o chatwoot, clique em `Configurações`, depois em `Caixa de Entrada` abra as configrações, encontre a opção `Habilitar CSAT` e deixe como ativado. Pronto!
Agora quando uma conversa for fechada será enviado para o cliente um link com a pesquisa de satisfação.

### Integração Concluída ✅

Caso tenha alguma dúvida [Chama no WhatsApp](https://wa.me/557998178275?text=Gost%C3%A1ria%20de%20contratar%20o%20servi%C3%A7o%20de%20consultoria%20sobre%20com%20o%20Chatwoot!) tenho alguns planos para consultoria individual.

  </details>
