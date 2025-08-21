##### ~={cyan}Trabalhando com Imagens=~

Por padrão, quando criamos um documento em branco no Latex ele já insere uma biblioteca específica para manipulação de imagens, que é a graphicx. 

Além de usar o módulo, eu preciso importar o arquivo de imagem na minha "área de trabalho". Após isso, basta usar o comando de begin com end e passar o parâmetro de figure. Automaticamente o Latex preenche o bloco.

```tex
\begin{figure}
	\centering
	\includegraphics{andromeda.jpeg}
	\caption{Caption}
	\label{fig:my_label}
\end{figure}
```

Como vimos antes, o primeiro e o último comando são responsáveis por iniciar e terminar o ambiente figura.
Em seguida, temos o comando de centralizar a figura no meio da página. O *includegraphics* será o arquivo da figura, o *caption* é a legenda e por fim o *label* que é o nome da figura dentro do documento.
##### ~={cyan}Redimensionamento da Figura=~

Muitas vezes a imagem não vem do tamanho adequado, dessa maneira é importante sabermos redimensionar ela passando os parâmetros corretos.

Os parâmetros de dimensões da imagem são enviados através de \[ ] 

> Exemplo

```tex
\begin{figure}
    \centering
    \includegraphics[width=12cm, height=12cm]{blackagar.jpg}
    \caption{Caption}
    \label{fig:my_label}
\end{figure}
```

Outra forma de definir o tamanho é pela porcentagem da escala, dessa maneira, ao invés de usarmos parâmetros de width e height, usariamos o scale.

Por fim, podemos deixar a imagem do tamanho do texto e respeitando as margens, ele ficará "alinhado", com o texto nas duas extremidades.

<div align="center"><img src="texto alinhado.png"></div>

> Exemplo

```tex
\lipsum[2]
\begin{figure}
    \centering
    \includegraphics[width=\textwidth]{blackagar.jpg}
    \caption{Caption}
    \label{fig:my_label}
\end{figure}
```

Por fim, podemos ainda modificar a angulação da imagem usando o parâmetro "angle".
##### ~={cyan}Reposicionamento de Imagens=~

As vezes a imagem não fica posicionada no local desejado, com isso podemos passar um parâmetro opcional ao usar o comando de ambiente. 

O parâmetro informa a posição da imagem em relação ao texto. Os parâmetros são:

-  h - aproxima do texto original ou do texto anterior;
-  t  - ficará mais ao topo da página;
-  b - a imagem ficará na parte inferior da página;
-  p - uma página será dedicada apenas para a imagem.

```tex
\lipsum[2]
\begin{figure}[h]
    \centering
    \includegraphics[width=\textwidth]{blackagar.jpg}
    \caption{\textit{Black Bolt - "I Win"}}
    \label{fig:my_label}
\end{figure}
```

A diferença quando trabalhamos com muitas imagens é que devemos colocar todas em uma única pasta para facilitar o manuseamento. Os parâmetros vão ter de ser alterados para *"nome_pasta/arquivo"*. Porém, podemos melhorar isso criando uma variável de imagens.

```tex
% Nome da pasta no argumento do comando
\grapicspath{{./imagens/}}
```

##### ~={cyan}Colocando Imagens lado à lado
=~
Antes de passarmos para o procedimento de imagens lado à lado precisamos entender o conceito de minipage. A minipage é um ambiente que pode receber alguns parâmetros, como por exemplo a posição, que foi o que vimos antes, p, b, t, porém aqui também teremos o c de centro.

Como parâmetros, tem-se o opcional de posicionamento e obrigatório de largura.

```tex
\subsection{MiniPage}
\begin{minipage}[c]{0.4=\textwidth}    % 0.4 da largura do texto
% Dessa forma o texto vai ocupar apenas 0.4 da largura do texto
\lipsum[1]
\end{minipage}
```

Para colocar duas imagens lado a lado, será necessário que dentro do ambiente da figura eu crie um ambiente de minipage. Para colocar elas na "mesma linha", usa-se o comando "\hfill".

```tex
\begin{figure} % inicio da figura

	\centering % centraliza a figura
	
		\begin{minipage}[b]{0.4\textwidth}
			\includegraphics[width=\textwidth]{imagens/andromeda.jpeg}
			\caption{Andrômeda pequena}
			\label{fig:my_label}
		\end{minipage}
		\hfill
		\begin{minipage}[b]{0.4\textwidth}
			\includegraphics[width=\textwidth]{imagens/andromeda.jpeg}
			\caption{Andrômeda pequena}
			\label{fig:my_label}
		\end{minipage}
		
\end{figure} % fim da figura
```









