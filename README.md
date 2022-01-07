# Comandos utilizados

Terminal:
1 - mkdir filmesImdb
2 - cd filmesImdb/
3 - python -m venv filmesImdb
4 - source filmesImdb/bin/activate
5 - pip install scrapy
6 - code .

VsCode
7 - source filmesImdb/bin/activate
8 - scrapy startproject imdb250
9 - cd imdb250/
10 - scrapy genspider imdb https://www.imdb.com/chart/top/?ref_=nv_mv_250/
11 - scrapy shell // Ambiente de testes
12 - response.css('.titleColumn').get()
13 - filmes = response.css('.titleColumn').get()
14 - len(filmes)
15 - response.css('.titleColumn a::text').get()
16 - titulos = response.css('.titleColumn a::text').get()
17 - response.css('.secondaryInfo::text').get()
18 - anos = response.css('.secondaryInfo::text').get()
19 - response.css('strong::text').get()
20 - avaliacoes = response.css('strong::text').get()
21 - scrapy crawl imdb // Verificando a saída no console
22 - scrapy crawl imdb -O imdb.json // Armazenando os dados em um arquivo JSON
23 - scrapy crawl imdb -O imdb.csv // Armazenando os dados em um arquivo CSV
