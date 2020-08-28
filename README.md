# Curriculum Vitae en Tex

Auteur original : Adrien Friggeri

Intrigué par le TeX , j'avais décidé de me pencher un peu dessus.

Il y a quelques temps je cherchais un model de CV assez *sexy* pour me démarquer
et j'avais trouvé celui-ci.

Ce model n'est plus disponible, car il a été amélioré par l'auteur original, je
continue à l'utiliser car il me convient .

Comme d'habitude je déborde sur la deuxième page et je souhaitais que mon nom apparaisse
à nouveau ainsi mes coordonnées sur la seconde page.

L'astuce consiste à indiquer *newpage* pour pouvoir ré inserer l'en-tête et le *aside*.

## Configuration

```
% -- Encoding UTF-8 without BOM
% -- XeLaTeX => PDF (BIBER)

\documentclass[]{cv-style}          % Add 'print' as an option into the square bracket to remove colours from this template for printing.
                                    % Add 'espanol' as an option into the square bracket to change the date format of the Last Updated Text

\sethyphenation[variant=british]{english}{french} % Add words between the {} to avoid them to be cut

```
## En-tête

On débute le document , et on défini le *header*

```
\begin{document}

\header{George}{Abitbol}           % Indiquez votre nom pour l'en-tête
% \lastupdated                     % On peut indiquer la dernière mise à jour du document


```

## Aside

C'est la colonne à gauche dans laquelle on définit les sections: *Contact*, *Langues*, *Mobilité* , à vous de définir ce que vous souhaité faire apparaitre.

```
\begin{aside}
  \section{bla}
  \section{ble}
  \section{bli}
\end{aside}

```

Il est possible d'intégrer un lien comme ceci:

` \href{mailto:george.abitbol@gmail.com}{george.abotbol@gmail.com}`

```
%----------------------------------------------------------------------------------------
%	SIDEBAR SECTION  -- aside est la colonne à gauche pour les informations
%----------------------------------------------------------------------------------------

\begin{aside}
% -- Nous définissons ici les sections
\section{Contact}
255 Route de Pétaouchnock
Pétaouchnock
~
France
~
01.02.03.04.05
~
% -- href permet d'intégrer un lien , ici le mailto permet au recruteur
% -- d'envoyer un courriel directement
 \href{mailto:george.abitbol@gmail.com}{george.abotbol@gmail.com}
~
~
\section{Langues}
% la commande suivante permet d'ajouter des petits dessin , ici un coeur bleu .
{\color{blue} $\varheartsuit$}
Francais
English-Espagnol
~
```
## Aptitudes

C'est ici que l'on va définir les aptitudes , je conseille de copier et de ré arranger ce que le recruteur recherche, c'est beaucoup plus simple.

```
%----------------------------------------------------------------------------------------
%	LES APTITUDES
%----------------------------------------------------------------------------------------

\section{La  Classe Américaine}

%----------------------------------------------
	{Recueillir les informations, s’informer sur les éléments du contexte}\\
	{Mettre en œuvre les conditions favorables à l’activité}\\
	{Mettre en œuvre des activités d’éveil }\\
    {Réaliser des soins du quotidien-accompagner l’enfant dans ses apprentissages}\\
	{Appliquer des protocoles liés à la santé de l’enfant }\\
	{Coopérer avec l’ensemble des acteurs-- Rendre compte (oral/écrit) d’une activité}

```
## Expériences et formations

J'ai préféré lier les périodes de formations et les expériences entre elles afin d'avoir une chronologie.

On débute la `\section{Formations et experiences}`,
puis on renseigne chaque entrée de la liste:

```
\begin{entrylist}
\entry
{DATE}
{QUOI OU}
{Etablissement VILLE}
{\jobtitle{QUOI plus précisément}\\
	\begin{itemize}
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
\end{itemize}}\\
\end{entrylist}
```

Il suffit de copier-coller les blocs les uns à la suite des autres et de modifier les entrées.

```
%----------------------------------------------------------------------------------------
%	Formations et Expériences
%----------------------------------------------------------------------------------------

\section{Formation et expériences}
\begin{entrylist}
\entry
{2014-2017}
{Bac Pro Cosmonaute Toulouse}
{Lycée de l'Espace Toulouse}
{\jobtitle{Formation en alternance de 3 ans}\\
	\begin{itemize}
		\item accompagner des publics non autonomes et \\développer une communication adaptée
		\item techniques de soins de confort
		\item règles d'hygiène et de sécurité
		\item intégrer les enjeux de nos territoires montagnards, \\péri-urbains et touristiques
		\item analyser des pratiques professionnelles françaises et étrangères
\end{itemize}}\\
```
## Nouvelle pages

Lorsque que l'on a beaucoup d'expériences ou un long parcours , il peut arriver que cela ne tienne pas sur une seule page, dans ce cas je préfère faire un rappel du nom du candidat en rajoutant un *header*, ainsi que les coordonnées avec un *aside*.

Cependant attention, il faut fermer le *entrylist*, puis d'indiquer `\newpage`.

```
\end{entrylist}
%-----------------------------------------------
\newpage
\header{George Abitbol}
%------------------------------------------------

%-----------------------------------------------
\begin{aside}
\section{Contact}
255 Route de Pétaouchnock
France
~
01.02.03.04.05
~
george.abitbol
@gmail.com
\end{aside}

```
## Suite des expériences et formations

Puis on replace des blocs suivant ce modèle .

```
\begin{entrylist}
\entry
{DATE}
{QUOI OU}
{Etablissement VILLE}
{\jobtitle{QUOI plus précisément}\\
	\begin{itemize}
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
		\item Ce que vous avez fait
\end{itemize}}\\
\end{entrylist}

```

## Centres d'Interets

J'indique ici les centres d'intérêts *Professionel* et *Personnel* en gras avec cette balise `\textbf{Professionel:}`


```
%----------------------------------------------------------------------------------------
%	CENTRES D'INTERETS
%----------------------------------------------------------------------------------------

\section{Intérêts}
  \vspace{-0.1cm}

\textbf{Professionel:} Réaliser des soins du quotidien-accompagner l’enfant dans ses apprentissages.Mettre en œuvre les conditions favorables à l’activité;
Mettre en œuvre des activités d’éveil;
Mettre en œuvre les conditions favorables à l’activité\\
\textbf{Personnel:} Randonnée, balade, lecture
%----------------------------------------------------------------------------------------

\end{document}
```

### Licence

Copyright (C) 2012, Adrien Friggeri

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
