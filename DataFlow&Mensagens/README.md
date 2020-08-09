## Modelo para Apresentação do Lab02 - Data Flow & Mensagens

### Tarefa sobre catálogo de componentes
* [arquivo do notebook com a resolução das seis tarefas](https://github.com/Rebecamorais2/INF331/blob/master/DataFlow%26Mensagens/notebook/lab2_part1.ipynb)

### Tarefa Web Components 1

```HTML

<dcc-trigger label="Mundo"
             action="noticia/mundo/politica"
             value="Vacina para COVID19 é aprovada em testes e começará ser produzida no começo de dezembro">
</dcc-trigger>
<dcc-trigger label="Brasil P"
             action="noticia/brasil/politica"
             value="Paulo Guedes desentende com Bolsonaro e pede demissão">
</dcc-trigger>
<dcc-trigger label="Brasil E"
             action="noticia/brasil/esporte"
             value="Corinthians vence Palmeiras na final do campeonado Paulista">
</dcc-trigger>

<dcc-trigger label="Bahia"
             action="noticia/bahia/esporte"
             value="Moradores da Bahia criam esportes para jogares com a familia em tempos de pandemia">
</dcc-trigger>

<dcc-lively-talk duration="0s"
                 character="doctor">
    <subscribe-dcc topic = "noticia/mundo/politica"/>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="nurse">
    <subscribe-dcc topic = "noticia/b#"/>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="patient">
    <subscribe-dcc topic = "noticia/#"/>
</dcc-lively-talk>

<dcc-trigger label="News" action="start/rss">
</dcc-trigger>
```
### Tarefa Web Components 2

```HTML
<dcc-trigger label="Ciência" action="next/rss">
</dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-trigger label="Design" action="next/rss">
</dcc-trigger>

<dcc-rss source="https://www.wired.com/category/design/feed" publish="rss/design">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>


<dcc-lively-talk duration="0s"
                 character="doctor">
    <subscribe-dcc topic = "aggregate/science"/>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="nurse">
    <subscribe-dcc topic = "rss/science"/>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="patient">
    <subscribe-dcc topic = "rss/design"/>
</dcc-lively-talk>
```
