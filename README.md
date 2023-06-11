# Sefaz Availability Application

O intuito deste programa é alertar usuários em um espaço customizado no Google Chat sobre os eventos de disponibilidade de NFe e NFCe na SEFAZ.

![logo](https://github.com/daviddev16/sefaz-availability-core/blob/master/assets/logo.png)

# Como funciona ?

O sistema espera o período de tempo configurado no campo ``global.fetch.time`` no arquivo ``services.json``, em seguida, faz a busca na API de monitoramento da [tecnospeed](monitor.tecnospeed.com.br) que retorna os status de cada estaddo e depois envia a mensagem para o espaço do Google Chat configurado no arquivo ``services.json``. Importante lembrar que esse programa não faz uso de credenciais de acesso do Google Cloud. É utilizado Webbooks para o envio de mensagem, certifique-se de ter um webhook configurado no espaço desejado.

# Utilização

A informação da key do webhook e o id do espaço do Google Chat pode ser informado de 2 jeitos:
- Através do arquvido ``services.json`` nos campos ``googlechat.space.id`` e ``googlechat.space.webhook.key``.
- Através dos parametros ``space-id=<space_id>`` e ``webhook-key=<webhook_key>`` na linha de comando quando for feita a execução do programa.

# Ambiente

Esse projeto foi desenvolvido no ``Eclipse`` e ``Temurin JDK-11.0.18.10`` com as seguintes dependências:
- ``com.google.code.gson:2.9.1``
- ``org.slf4j-api:1.7.6``
- ``org.slf4j-log4j12:1.7.5``
- ``commons-cli:1.5.0``
