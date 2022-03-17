## Ferramenta Anais Anped

[![DOI](https://zenodo.org/badge/467663926.svg)](https://zenodo.org/badge/latestdoi/467663926)
 [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) [![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

Projeto de script para web scraping da página de [Anais da Associação Nacional de Pós-Graduação e Pesquisa em Educação - Anped](http://anais.anped.org.br/).

Seu objetivo é compor a base de dados do [Repositório Digital das Humanidades (pt-BR)](https://labhdufba.github.io/redhbr/) e foi desenvolvida por [Eric Brasil](https://ericbrasiln.github.io/) (IHLM/UNILAB) em parceria com o [Laboratório de Humanidades Digitais da Ufba](http://labhd.ufba.br/).

*O script Anais-Anped realiza a raspagem dos papers em pdf dos encontros nacionais 38, 39 e 40, dos anos 2017, 2019 e 2021, respectivamente, (disponíveis atualmente na site).*
___

**A ferramenta foi desenvolvida apenas para pesquisas acadêmicas, sem fins lucrativos.**

### Instalação

Para executar a ferramenta é preciso clonar ou fazer download do repositório para sua máquina. Antes de executar os scripts, é preciso preparar seu computador, como mostramos abaixo.

A ferramentas desse projeto foram escritas em [Python 3.9.7](https://www.python.org/). Portanto, para executar o arquivo .py é preciso instalar o Python3 em seu computador.

[Clique aqui](https://python.org.br/instalacao-windows/) para acessar um tutorial de instalação do Python no Windows, [clique aqui](https://python.org.br/instalacao-linux/) para Linux e [clique aqui](https://python.org.br/instalacao-mac/)
para Mac.

Após a instalação do Python é preciso instalar as bibliotecas necessárias para a ferramenta ser executada. Para isso, basta executar o comando `pip install -r requirements.txt` no terminal, a partir da pasta onde está o arquivo.  Para saber mais sobre instalação de bibliotecas com pip, veja essa lição do [Programming Historian](https://programminghistorian.org/pt/licoes/instalacao-modulos-python-pip).

1. Acesse o diretório em que o arquivo `requirements.txt` está salvo:
   ```{.sh .bash}
   $ cd <caminho para a pasta>
   ```
2. Instale as bibliotecas requeridas com o seguinte comando:
   ```{.python}
   pip install -r requirements.txt
   ```

Agora é possível executar a ferramenta direto do prompt de comando do Windows ou pelo terminal do Linux, ou utilizar as diversas [IDE](https://pt.wikipedia.org/wiki/Ambiente_de_desenvolvimento_integrado) disponíveis.

### Utilização

Na pasta da ferramenta o arquivo `scrape_anped.py`.

Esse script permite ao usuário selecionar qual evento pretende raspar (ou se pretende raspar todos de uma vez).

Para isso é preciso executar o seguinte comando, do interior da pasta onde o arquivo está localizado:

```{.sh}
python scrape_anped.py
```

A seguinte mensagem será exibida:

```{.python}
-=-Definição do evento-=-

- Opções:
38 - 2017
39 - 2019
40 - 2021
Todos
Digite o número correspondente ao evento que deseja raspar: 
```

### Resultados

O script retorna para o usuário **todos os pdfs disponíveis em todas as páginas dos eventos selecionados**. São criadas pastas com o número de cada evento para o armazenamento dos arquivos em PDF.

O script também gera um arquivo **CSV** (*comma-separated values*) contendo os seguintes valores para cada paper: Autores, Título, GT, Evento, Ano, Link.

O script está funcionando perfeitamente. Qualquer alteração no site percebida pelos usuários ou sugestões de aprimoramento são bem vindas.

### Download dos dados

[Se preferir baixar a planilha sem usar o código clique aqui](https://od.lk/d/ODRfNjA1NDgxNDZf/anais-anped-38-39-40_2022-03-09_12-57-55.csv).

### Citação

Como citar essa ferramenta?

É possível clicar em `Cite this repository` na aba à direita da página inicial do repositório no GitHub para acessar a citação nos formatos APA e BibTex, ou ainda acessar o [arquivo da citação](https://github.com/ericbrasiln/anais_anped/blob/main/CITATION.cff) em formato .cff.

Abaixo a citação no formato BibTex:

```
@software{Brasil_Ferramenta_Anais_Anped_2022,
author = {Brasil, Eric},
month = {3},
title = {{Ferramenta Anais Anped}},
url = {https://github.com/ericbrasiln/anais_anped},
version = {1.0},
year = {2022}
}
```

### Licença

MIT licensed

Copyright (C) 2022 [Eric Brasil](https://github.com/ericbrasiln)
