##### ~={cyan}Fontes serifadas e não serifadas=~

-  Com Serifa

```tex
\textrm{Com Serifa}
% ou para deixar mais visivel
{\Large \textrm{Com Serifa}}
```

Eu posso utilizar a combinação de fontes serifadas com itálico ou negrito.

-  Sem Serifa

```tex
\textsf{Sem Serifa}
{\Large \textsf{Sem Serifa}}
```

Do mesmo jeito que usamos o negrito e o itálico na serifada, podemos deixar na não serifada.

##### ~={cyan}Fontes personalizadas=~

Fontes personalizadas podem ser usadas no Overleaf/Latex, entretanto, deve ser feito o upload de cada uma delas no projeto.

-  Alterar o compilador para o XLatex (o compilador com PDF não consegue rodar a nova fonte)
-  Usar o pacote de *"/usepackage{fontspec}"* para definir novas fontes
-  Formatar a fonte no preâmbulo

```tex
\usepackage{fontspec}
\setromanfont{EBGaramond}[
	Path= ./ebgaramond/,
	Extension= .ttf,
	UprightFont=*-Regular,,
	BoldFont=*-Bold,
	ItalicFont=*-Italic
	BoldItalic=*-BoldItalic
]
```