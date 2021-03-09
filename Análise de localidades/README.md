# Análise de localidades dos tweets

Os códigos disponíveis nesta pasta objetivam transformar as informações relativas à localização dos tweets sobre a pandemia de covid 19 no Brasil em análises gráficas que possam ser comparadas com os indicadores epidemiológicos para os mesmos períodos da coleta.

## Preparando o ambiente

Todos os códigos foram feitos usando a linguagem de programação python 3 por meio da interface Jupyter Notebook. Além disso, os códigos foram executados no sistema operacional Windows 10. Logo, caso tente reproduzir os resultados em outro Sistema operacional, talvez seja preciso alterar algumas linhas do código. Nesses casos, basta seguir os comentários presentes no próprio código, que indicam o que fazer.

Algumas bibliotecas de Python precisam ser previamente instaladas, caso ainda não estejam, para que o programa não apresente nenhum tipo de erro. Para instalá-las, basta digitar os seguintes comandos, um por vez, no prompt de comando do seu computador (para Windows) e pressionar "Enter".

```bash
pip install plotly
pip install pysqlite3 
pip install geobr
```

## Correcao_locations.ipynb

Este script é o responsável por transformar os dados brutos das localizações dos tweets coletados anteriormente em uma base de dados que normaliza as localizações que foram possíveis de serem identificadas como válidas.

Observe que não é possível executar esse código sem possuir os arquivos resultantes da coleta de dados do Twitter. Logo, ele está presente no repositório apenas para validar o processo de criação para o arquivo que serviu de base para as análises executadas no outro script. O arquivo resultante desse script já está disponível nesse repositório.

script Correcao_locations.ipynb:

- Entradas: dados coletados com as localizações dos tweets.
- Saída: arquivo "tweets_location_corrigido.csv" com as localizações normalizadas.

## PlotsLocations.ipynb
Esse é o principal script desta análise. Com ele unimos as localizações normalizadas dos tweets coletados anteriormente com as bases de dados relativas aos indicadores epidemiológicos da pandemia. 
Portanto, para que  seja possível executá-lo, é necessário antes possuir os arquivos "tweets_location_corrigido.csv" e "indicadores.db".

PlotsLocations.ipynb: 
- Entradas: arquivos "tweets_location_corrigido.csv" e "indicadores.db"
- Saídas: pastas "resultadosHTML" e "resultadosPNG" contendo as análises e visualizações nos formatos HTML e PNG.

**Atenção**: por conta do seu volume, o arquivo "tweets_location_corrigido.zip" está comprimido e precisa ser descompactado antes de ser utilizado.

