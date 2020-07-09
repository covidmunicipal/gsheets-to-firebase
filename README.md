# Exportação do Google Sheets para Firebase

Contém o modelo para uma planilha de acompanhamento dos dados, além de um script para o [Google Apps Script](http://script.google.com/) que exporta os dados de uma planilha do Google Sheets para uma Realtime Database do Firebase. Utilizamos para publicar e disponibilizar para o aplicativo os dados coletados.

## Configurando

Primeiro, importe a [planilha modelo](spreadsheet_model.ods) (`spreadsheet_model.ods`) para o Google Sheets.

No [arquivo de script](code.gs) (`code.gs`), altere o `<SPREADSHEET-ID>` e o `<FIREBASE-URL>` do objeto `environment` pela ID da planilha do Google Sheets e a URL do Firebase Realtime Database, respectivamente. A URL precisa estar no formato `https://<ID-DO-PROJETO-DO-FIREBASE>.firebaseio.com/`.

Depois, na planilha, acesse a opção _Ferramentas_ -> _Editor de script_ e cole ambos os arquivos.

Ainda no editor de script, selecione a opção _Executar_ -> _Executar função_ -> _initialize_. Serão solicitadas as permissões para executar o script.

O script será executado automaticamente toda vez que houver uma alteração na planilha.

Se deseja ver um modelo de como a planilha é preenchida, veja a [planilha usada no painel de acompanhamento de Irará](https://docs.google.com/spreadsheets/d/1-a543uhVSRItc7P4tZPiHBvz5bwUH0zQLn5b8hNbehg).

## Sobre

O código fornecido é baseado no snippet de [Edwin Lee](https://gist.github.com/edwinlee) disponível [neste artigo do Medium](https://medium.com/firebase-developers/sheets-to-firebase-33132e31935b).
