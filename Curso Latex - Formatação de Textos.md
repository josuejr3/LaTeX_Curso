##### ~={cyan}Formatação de Texto com Negrito, Itálico e Sublinhado.=~

Os três tipos de formatações de texto mais comuns encontradas em documentos são:

- Negrito;
- Sublinhado;
- Itálico

Abaixo podemos ver como é o funcionamento de cada um deles na linguagem de Latex.

-  Negrito

```TEX
meu \textbf{trabalho}
```

-  Sublinhado

```tex
meu \underline{trabalho}
```

-  Itálico

```tex
meu \textit{trabalho}
```

Para fazer a combinação entre eles, basta inserir "um dentro do outro".

##### ~={cyan}Enfâse=~

Para dar enfâse basta usar o comando abaixo

```tex
\emph{esse é o meu texto}
```

---
##### ~={cyan}Alinhamento de Texto usando técnica de Ambientes=~

Vamos alinhar primeiro em relação à um ambiente. O alinhamento pode ser tanto à direito, como à esquerda, centralizado ou justificado. Por padrão, o texto fica justificado. Veja o código abaixo.

```tex
\begin{document}
    \maketitle
    
    \section{Inicio}
    % Alinhamento
    \begin{flushleft}
        \lipsum[1]
    \end{flushleft}
    
    \section{Desenvolvimento}
    \begin{flushright}
    \lipsum[1]
    \end{flushright}

    \section{Desenvolvimento2}
    \begin{center}
        \lipsum[1]
    \end{center}

    % Se nenhum parâmetro for passado
    % ele fica justificado
    \section{Conclusao}
    \lipsum[1]
\end{document}
```

Lembrando que como o alinhamento é por ambiente, então ele é feito após a definição de um begin e antes de fechar o ambiente com o end.

##### ~={cyan}Alinhamento de Texto usando técnica de Comandos=~

```tex
\section{indice de figuras}
\raggedleft
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse vel magna mattis nibh viverra viverra. Sed felis leo, consequat id finibus sed, porta eu nulla. Morbi non purus in tellus placerat mattis in non neque. Nulla aliquet, felis dapibus pharetra pulvinar, eros turpis mattis odio, ac aliquet nisi lectus in diam. Nulla eget augue sit amet nunc sagittis cursus in ac nunc. 
```

Esse tipo de comando faz com que até o "tópico" ou seção seja alinhado à esquerda. No meio do texto eu posso utilizar o oposto, "raggedright".

-  raggedright
-  centering

Por padrão, o latex utiliza o alinhamento justificado.

##### ~={cyan}Colorindo Textos=~

Para colorir textos no Latex devemos utilizar o pacote específico para isso, chamado de *"xcolor"*.

```tex
\section{Inicio}
    \begin{flushleft}
        \textcolor{red}{Josue}
    \end{flushleft}
```

Usamos o comando "\\textcolor{cor}{texto}" que recebe no primeiro parâmetro a cor do texto  no segundo o texto que será colorido.

Entretanto, essa não é a forma mais eficiente de colorir um texto. O melhor jeito é "criarmos" uma cor e darmos um nome a ela.

1.  No preâmbulo nós devemos definir a nova cor

```tex
\definecolor{nova_cor}{HTML}{codigo_em_hexadecimal}
\definecolor{cor_laranja}{HTML}{FF4500}
```

---
##### ~={cyan}Listas=~

> Exemplos fazendo listas

```latex
\begin{itemize}
	\item Azul
	\item Verde
	\item Amarelo
	\item Laranja
	\item Vermelho
\end{itemize}
```

Outra alternativa ao itemize é usar o enumerate, com a diferença de que o segundo ao invés de pontuar, vai enumerar cada elemento.

Além disso, posso subdividir a lista faendo um outro ambiente de itemize ou enumerate dentro da própria lista.

```tex
\begin{enumerate}
\item Azul
\item Verde
\begin{enumerate}
	\item Verde1
	\begin{enumerate}
		\item V11
	\end{enumerate}
	\item Verde2
	\item Verde3
\end{enumerate}
\item Amarelo
\item Laranja
\item Vermelho
\end{enumerate}
```

##### ~={cyan}Sobrescrito e Subscrito=~

-  Em textos, o subescrito será indicado por um underline *\_*
-  O sobrescrito será indicado por um acento circunflexo ^

```tex
$H_2O$
```

Tanto o sobreescrito como o subescrito devem estar na forma de escrita matemática que é definida pelo uso de dois cifrões ($).


