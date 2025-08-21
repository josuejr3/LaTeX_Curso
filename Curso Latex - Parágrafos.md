#### ~={cyan}Espaçamento entre Parágrafos=~

Inicialmente para fazer o espaçamento entre parágrafos usamos o código abaixo. Devemos importar o pacote parskip e passar como argumento para o comando setlength., o segundo parâmetro é a quantidade de pontos de espaçamento.

Lembrando que como esse tipo de configuração é feita no preâmbulo, então todo o documento terá essa configuração.

> Exemplo

```tex
\usepackage{parskip}
\setlength{\parskip}{12pt}
```

No exemplo acima, acima os parágrafos estão separados por 12 pontos.

O parâmetro de tamanho pode ser inserido como:

-  Pontos
-  Pixels
-  Centímetros

Assim como outras configurações que podemos fazer específicas para páginas e regiões, também podemos fazer com parágrafos. Basta definirmos onde irá começar.

```tex
\setlength{\parskip}{12pt}
% Daqui pra frente a separação de parágrafo é de 12 pt
...
\setlength{\parskip}{48pt}
% Daqui pra frente a separação de parágrafo é de 48 pt
```

##### ~={cyan}Identação de Parágrafos, Alinhamento de Parágrafos e Espaçamento entre Linhas=~

A identação de parágrafos é basicamente um pequeno recuo que o parágrafo tem assim que ele começa. Normalmente eles são definidos também no preâmbulo do documento.

```tex
\setlength{\parindent}{48px}
```

```tex
\setlength{\parindent}{1.25cm}
```

O mesmo pode ser feito ao longo do documento.

Semelhante ao que vimos anteriormente, podemos alinhar um parágrafo abrindo um ambiente (bloco) de begin e end e após isso passar como parâmetro se é center, flushright e flushleft.

```tex
\begin{center, flushleft, flushright}
...
\end{center, flushleft, flushright}
```

Assim como as configurações anteriores o espaçamento entre linhas é feito no preâmbulo do documento.

Lembrando que nesse caso, é necessário usar o pacote setspace

```tex
\usepackage{setspace}
\setstretch{1.5}
```

##### ~={cyan}Colocando Identação no Primeiro Parágrafo
=~
Por padrão, o latex não identa o primeiro parágrafo de uma seção. O primeiro nunca é identado, porém podemos alterar. Para isso, usaremos o pacote abaixo.

```tex
\usepackage{indentfirst}
```

Não precisa executar nenhum comando, só o fato de colocar o pacote no projeto ele já indenta automaticamente.

##### ~={cyan}Quebrando linha sem quebrar o parágrafo=~

Para quebrar uma linha, não adianta somente dar um espaçamento, um espaçamento único uma linha, se for dois ele já considera um outro parágrafo. O comando para quebrar a linha sem quebrar o parágrafo é o que vimos antes, o *\newline*. Alternativamente, podemos usar o comando "\\\\".

```tex
....\\...
```