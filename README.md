  <p align="center">
  <img src="https://s3.us-west-2.amazonaws.com/gh-assets.chatwoot.com/brand.svg](https://app.dispzap.com/brand-assets/logo.svg" alt="DispZap Whats Marketing" width="240" />
  <p align="center">Seja bem-vindo, aqui você vai encontrar materiais extras criados para dar um up na API Codechat</p>
  </p>

  <details>
<summary>Workflow que habila CSAT</summary>

Para habiliatar o CSAT (pesquisa de satisfação ao cliente) em seu Chatwoot, basta ir até o diretório workflow-n8n

# Baixe e importe o worflow

# PASSO 01: No node `ConsultaIDBanco` adicione suas credenciais do banco de dados postgres

```bash
#host
localhost

#Database
chatwoot_production

#user
User

#Password
Adicone a senha do postgres. Você encontra no arquivo .env do chatwoot em /home/chatwoot/chatwoot

```

# PASSO 02: Vá até o NODE `SetMensagem`

```bash
#Vá até o cmapo value e procure pela variavél `#suaurlchatwoot` e adicione o endereço de instalação do seu chatwoot

https://app.chatwoot.com/survey/responses/{{ $node["ConsultaIDBanco"].json["uuid"] }}

```

# PASSO 03: Ajuste envio no NODE `SendMSGCodechat`

```bash
#Na URL onde ta escrito `#urlcodechat` adicione o endereço da api codechat. Em `#suainstancia` é o nome de sua caixa de entrada

```

# Hora de testar se tudo está correto! Vai até o chatwoot, cloque em `Configurações`, clique em `Caixa de Entrada` abra as configrações, encontre a opção `Habilitar CSAT` e deixe como ativado. Pronto!
Agora quando uma conversa for fechada será enviado para o cliente um link com a pesquisa de satisfação.

### Instalação Finalizada ✅

Caso tenha alguma dúvida [Chama no WhatsApp](https://wa.me/557998178275?text=Gost%C3%A1ria%20de%20contratar%20o%20servi%C3%A7o%20de%20consultoria%20sobre%20com%20o%20Chatwoot!) tenho alguns planos para consultoria individual.

  </details>
