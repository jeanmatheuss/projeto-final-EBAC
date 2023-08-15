# Projeto de Captura e Armazenamento de Mensagens do Telegram

Este projeto tem como objetivo capturar mensagens de um bot do Telegram e armazená-las de forma eficiente utilizando os serviços da Amazon Web Services (AWS). As mensagens, fornecidas no formato JSON através da API web de bots do Telegram, serão ingeridas e redirecionadas para uma API web, possibilitando o armazenamento por meio do AWS Lambda e do AWS S3.

### Fluxo do Projeto

![img](https://github.com/jeanmatheuss/projeto-final-EBAC/blob/main/img/img_arquitetura.png?raw=true)


1. As mensagens capturadas pelo bot do Telegram são ingeridas via streaming, uma vez que o Telegram retém mensagens por apenas 24 horas em seus servidores.
2. Para possibilitar a ingestão em tempo real, será utilizado um webhook para redirecionar automaticamente as mensagens para uma API web.
3. O serviço AWS API Gateway será empregado para receber os dados redirecionados e permitir o encaminhamento para outros serviços AWS.
4. Conectaremos o AWS API Gateway ao AWS Lambda, que armazenará as mensagens no seu formato JSON original em um bucket do AWS S3.


### Considerações Finais
Este projeto demonstra a criação de um sistema eficiente para captura e armazenamento de mensagens do Telegram utilizando serviços da AWS. A combinação do AWS API Gateway, AWS Lambda e AWS S3 proporciona um fluxo de trabalho automatizado e escalável.
