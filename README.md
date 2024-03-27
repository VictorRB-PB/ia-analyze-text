
# Análise de Sentimentos com Language Studio no Azure AI 

Será realizado um passo a passo de como foi utilizado o Language Studio. Todas as informações foram retiradas de documentações da Microsoft Learn.




## Estudio de Fala

    O serviço Azure AI Speech transcreve a fala em texto e o texto em fala audível. Você pode usar o AI Speech   
    para criar um aplicativo que possa transcrever notas de reuniões ou gerar texto a partir da gravação de entrevistas.

Neste exercício, você experimentará os recursos do Azure AI Speech usando o Azure AI Speech Studio.

1. ```Criar um recurso de fala do Azure AI```
      
      Você pode usar o serviço de Fala criando um recurso de Fala ou um recurso de serviços de IA do Azure.  
      Neste exercício, você criará um recurso AI Speech, a menos que já tenha um recurso que possa usar.

      `` 1.1 Em outra guia do navegador, abra o Azure AI Speech Studio(https://speech.microsoft.com/portal), entrando com sua conta da Microsoft.``
       
     `` 1.2 Selecione Configurações e depois Crie um recurso. Configure-o com as seguintes configurações:``
    ![Criar recurso](https://r2.easyimg.io/bdhbgrmqk/criarrecursodefala.png)
    ![Criar serviço cognitivo](https://r2.easyimg.io/lsqh2bnjb/criandorecursodefala.png)

         Nome do novo recurso: insira um nome exclusivo.
         Assinatura: sua assinatura do Azure.
         Região: selecione uma região suportada.
         Nível de preços: FO gratuito (se disponível, caso contrário, selecione Padrão S0).
         Grupo de recursos: selecione ou crie um grupo de recursos com um nome exclusivo.
      
     `` 1.3   Selecione Criar recurso. Aguarde até que o recurso seja criado e selecione Usar recurso. A página Introdução à Fala é exibida.``

## Explore a fala em texto no Speech Studio

    1. Selecione https://aka.ms/mslearn-speech-files para baixar o Speech.zip. Abra a pasta.
    2. Na página Introdução de fala em texto,localize Conversão de fala em texto em tempo real. Clique em Experimente o Conversão de fala em texto em tempo real.
![conversao](https://r2.easyimg.io/u6o0hlerp/conversaodefalaemtextoemtemporeal.png)
    
    3. Em Escolher arquivos de áudio, selecione Procurar arquivos e navegue até a pasta onde você salvou o arquivo. Selecione WhatAICanDo.m4a e depois Abrir.
![arquivo de fala](https://r2.easyimg.io/01mz6dvxa/procurararquivodefala.png)
   
    4. O serviço de fala transcreve e exibe o texto em tempo real. Se você tiver áudio em seu computador, poderá ouvir a gravação enquanto o texto é transcrito.
    5. Revise a saída, que deve ter reconhecido e transcrito com êxito o áudio em texto.

Neste exercício você criou um recurso AI Speech no Speech Studio. Em seguida, você usou o serviço de fala em texto em tempo real para transcrever uma gravação de áudio. Você pôde ver a transcrição do texto sendo gerada à medida que o arquivo de áudio era reproduzido.

## Analise de texto com Language Studio
Neste exercício, você explorará os recursos da linguagem Azure AI analisando alguns exemplos de avaliações de hotéis. Você usará o Language Studio para entender se as avaliações são em sua maioria positivas ou negativas.  
    
O Processamento de Linguagem Natural (PNL) é um ramo da IA que lida com a linguagem escrita e falada. Você pode usar a PNL para construir soluções que extraiam significado semântico de texto ou fala, ou que formulem respostas significativas em linguagem natural.  
    
Por exemplo, suponha que a agência de viagens fictícia Margie’s Travel incentive os clientes a enviar avaliações sobre estadias em hotéis. Você pode usar o serviço de idiomas para identificar frases-chave, determinar quais avaliações são positivas e quais são negativas ou analisar o texto da avaliação em busca de menções a entidades conhecidas, como locais ou pessoas.  

O Azure AI Language Service inclui análise de texto e recursos de PNL. Isso inclui a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

Crie um novo recurso de fala ou utilize algum caso ja tenha criado.(Demonstrado a cima no apendice 1)

## Configure seu recurso no Azure AI Language Studio

    1. Em outra guia do navegador, abra o Language Studio em https://language.cognitive.azure.com e entre.
    2. Quando solicitado com Selecione um recurso do Azure, faça as seguintes configurações:

         Diretório Azure: Diretório Padrão, o diretório que você está usando
         Assinatura do Azure: selecione a assinatura que você está usando
         Tipo de recurso: Idioma
         Nome do recurso: selecione o recurso de serviço de idioma que você acabou de criar  

    3. Em seguida, selecione Concluído.
![Selecionando recurso](https://r2.easyimg.io/vhrarju6f/selecionandorecursoazure.png)

## Analise avaliações no Language Studio

    1. Em uma nova guia do navegador web, navegue até Language Studio em https://language.cognitive.azure.com.
    2. Na página inicial Bem-vindo ao Language Studio, selecione a guia Classificar texto e, em seguida, selecione o bloco Analisar sentimento e extrair opiniões.
![analisar sentimento](https://r2.easyimg.io/e0iyt52az/analisedesentimentos.png)

    3. Em Selecionar idioma do texto, selecione Inglês.
    4. Em Selecione o seu recurso Azure, selecione o seu recurso.
    5. Em Digite seu próprio texto, carregue um arquivo ou use um de nossos textos de exemplo, copie e cole a seguinte revisão:
```
 Tired hotel with poor service
 The Royal Hotel, London, United Kingdom
 5/6/2018
 This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.

```
    6. Marque a caixa para confirmar que a demonstração incorrerá em uso e poderá incorrer em custos e selecione Executar.
![texto analise sentimentos](https://r2.easyimg.io/fjunagnvo/textoanalisedesentimentos.png)
![run](https://r2.easyimg.io/v4jzla6d3/runetextosentimentos.png)

    7. Revise a saída. Observe que o documento é analisado quanto ao sentimento, assim como cada frase. Selecione Frase 1 para mostrar a análise de sentimento dessa frase.
![sentença 1](https://r2.easyimg.io/hkpxlw39y/sentenca1.png)

Observe que há um sentimento geral seguido por pontuações próximas a três categorias: pontuação positiva, pontuação neutra, pontuação negativa. Em cada uma das categorias é atribuída uma pontuação entre 0 e 1. Essas pontuações de confiança indicam a probabilidade do texto fornecido ser um sentimento específico.

![resultado sentença 1](https://r2.easyimg.io/df2gzedy0/resultadosentenca1.png)

Selecione a sentença 1 novamente para fechar.

    1. Role para cima limpe a caixa de texto, copie e cole a seguinte revisão:

``` 
 Good Hotel and staff
 The Royal Hotel, London, UK
 3/2/2018
 Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.

```

    2. Selecione Executar. Revise o resultado e o sentimento e o nível de confiança.
![resultado frase 2](https://r2.easyimg.io/6zq1tsfjt/resultadofrase2.png)

    3. Limpe a caixa de texto novamente, copie e cole a seguinte revisão:

```Very noisy and rooms are tiny The Lombard Hotel, San Francisco, USA 9/5/2018 Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep–was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds–but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they’ve made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget```

    4. Selecione Executar e analise o sentimento juntamente com o nível de confiança. Dê uma olhada no texto e compare-o com a análise de sentimento que o serviço retornou.

Neste exercício você usou o Language Studio para criar um novo recurso de idioma ou usar um recurso de idioma existente. Você habilitou o recurso em Configurações antes de experimentar o serviço de mineração de sentimento e opinião. Em seguida, você testou o serviço com três trechos de texto.

## Importante: Limpar o workspace

1. No [Azure Machine Learning Studio](https://ml.azure.com/?azure-portal=true), na página Grupos de recursos, abra o grupo de recursos especificado ao criar o seu espaço de trabalho Azure Machine Learning.

![Grupo de Recursos](https://r2.easyimg.io/2o5s4m34r/gruporecursos.png)
![Lista de grupos](https://r2.easyimg.io/ln4zmp7ai/listadegrupos.png)  

2. Clique em Excluir grupo de recursos, digite o nome do grupo de recursos para confirmar que deseja excluí-lo e selecione Excluir, a exclusão pode demorar alguns minutos.
![Excluir grupo](https://r2.easyimg.io/0emlhhnaw/excluirgrupo.png)
![Confirma exclusão](https://r2.easyimg.io/7a9u590oj/confirmaexcluir.png)



## Referências
 - [Explore Speech Studio](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/09-speech.html)
 - [Analise texto com Language Studio](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html)


