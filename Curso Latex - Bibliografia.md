##### ~={cyan}Como criar uma bibliografia?=~

-  Criar arquivo de bibliografia, ele deve ter uma extensão (.bib);
-  Selecionar de algum site, com a opção "*citar*" o código da bibliografia;
-  Colar no arquivo .bib;
-  No arquivo principal, adicionar o pacote *"biblatex"*;
-  No arquivo principal, adicionar o arquivo.

```tex
\addbibresource{biblio.bib}
```

-  Para citar, basta escolher o local no texto e executar o seguinte comando.

```tex
\cite{nome_da_referencia_no_arquivo_bib}
```

-  No final do arquivo, antes do documento executar o comando abaixo para ele printar a bibliografia.

```tex
\printbibliography[title={Referencias}]
```

-  Citando agora dois autores ou duas fontes (para isso basta separar os dois por vírgulas).

```tex
\cite{nome_da_referencia_no_arquivo_bib}
```

##### ~={cyan}Estilos distintos de Referências=~

No importe do pacote eu posso passar um parâmetro opicional que é o "*style*", com isso eu posso mudar o estilo da referência.

```tex
\usepackage[style=alphabetic]{biblatex}
```

##### ~={cyan}Referências de Livros=~

As referências de livros devem seguir o formato abaixo (no arquivo de bibliografia).

```bib
@book{suassuna2018iniciaccao,
	title={Inicia{\c{c}}{\~a}o {\`a} est{\´e}tica},
	author={Suassuna, Ariano},
	year={2018},
	publisher={Nova Fronteira}
}

% sobrenomeANOprimeironome
@book{einstein2017vejo,
	title={Como eu vejo o mundo},
	author={Einstein, Albert},
	year={2017},
	publisher={Nova Fronteira}
```

##### Referências Bibliográficas na ABNT

> Passos

1. Definir o tipo do documento como article e abntex2
2. Usar o pacote abntex2cite
3. Passar como parâmetro no abntex2cite o tipo de apresentação (alf)
4. Usar o pacote babel com idioma brasileiro

```tex
\documentclass[article]{abntex2}
\usepackage[alf]{abntex2cite}
\usepackage[brazil]{babel}
\usepackage{graphicx}
```

No final do documento, vamos usar o comando de bibliografia e passar o arquivo de bibliografia como parâmetro.

```tex
\bibliography{biblio.bib}
```

