
Um dos pacotes mais utilizados em Latex é o *"geometry".* Ele é responsável por controlar as margens do documento e o tamanho da página.

> Exemplo de uso

```tex
\usepackage[letterpaper,top=2cm,bottom=2cm,left=3cm,right=3cm,marginparwidth=1.75cm]{geometry}
```

Define o tipo de papel, o tamanho das margens superior, inferior, esquerda e direita, além da margem interna.

> Exemplo usando textos gerados

```tex
\usepackage{lipsum}
```

```tex
\begin{document}
\section{Introdução}
% cria de 1 a 8 paragrafos
\lipsum[1-8]
% cria 2 paragrafos
\lipsum[2]
\end{document}
```

O section que é visto no código pode ser por exemplo um tópico de introdução, desenvolvimento ou qualquer outro.

