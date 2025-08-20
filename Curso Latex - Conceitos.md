
#### ~={cyan}Conceitos - LaTeX=~

-  Ambientes

São as áreas delimitadas pelo nosso documento, é onde um conjunto de regras específicas se aplica.

> Exemplo - Ambiente do documento que estamos trabalhando

```tex
\begin{document}

\maketitle

\section{Introdução}

\end{document}
```

O ambiente começa com um *begin* e termina com um *end.*

> Exemplo - Criando um ambiente de uma equação, tabela e figuras.

```Tex
\begin{equation}
\end{equation}

\begin{table}
\end{table}

\begin{figure}
\end{figure}
```

-  Comandos

Comandos em LaTeX são palavras ou símbolos que iniciam uma palavra específica. Sempre começam com uma barra invertida seguidos do nome do comando.

> Exemplo - Comando de titulo e autor

```tex
\author
\date
\title
```

-  Parâmetros

Os parâmetros são as opções que podem ser passadas para um comando ou ambiente. Eles são passadas através de colchetes " { } ", ou de chaves " \[ ] ".

> Exemplo - Incluindo Imagens

```tex
\subsection{How to include Figures}
% Um parâmetro entre colchetes e outro entre chaves
\includegraphics[width=0.3\textwidth]{frog.jpg}
```

<mark style="background: #BBFABBA6;">Obs</mark>

1. Parâmetros entre colchetes são opcionais
2. Parâmetros em chaves são obrigatórios
	Dessa maneira, no segundo include é obrigatório dizer qual é a imagem, porém o tamanho é opcional. No caso de ambientes por exemplo, eu preciso informar qual ambiente está sendo encerrado obrigatoriamente.


-  Classes de Documentos

As classes de documentos, como o próprio nome já diz, define o tipo de documento que estamos criando ou trabalhando. A partir disso, temos as opções de formatação.

> Exemplo - Classes de Documentos

```tex
\documentionclass{article}
\documentionclass{book}
```

Após definir a classe, eu vou pedir usar determinados comandos. A classe do documento deve ser definida no inicio do código.

-  Preâmbulo

O preâmbulo é a parte do documento que vem antes do conteúdo principal. É o local em que são definidas as configurações globais do documento, como classe, pacotes e comandos personalizados.

> Exemplo - Preâmbulo

```tex
% tudo antes disso, é o preâmbulo
\begin{document}
\end{document}
```

-  Pacotes

No LaTeX pacotes são plugins que adicionam funcionalidades extras ao sistema básico. Exemplo são os pacotes de tabelas, referências bibliográficas e imagens. 

> Exemplo - Pacotes

```tex
% Usando o pacote babel
\usepackage[english]{babel}
\usepackage{amsmath}
\usepackage{graphicx}
```


