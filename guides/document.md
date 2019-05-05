# Impaginare un documento

## Scegliere il motre corretto

- ❔ [Differences between LuaTeX, ConTeXt and XeTeX](https://tex.stackexchange.com/questions/36/)

### XeTeX

- [`fontspec`](https://ctan.org/pkg/fontspec) — Fontspec is a pack­age for XELATEX and LuaLATEX. It pro­vides an au­to­matic and uni­fied in­ter­face to fea­ture-rich AAT and OpenType fonts
	- 📃 [package documentation](http://ctan.math.illinois.edu/macros/latex/contrib/fontspec/fontspec.pdf)

## Mantenere un changelog

Il versionamento è importante, non sottostimarlo. [Keeping a changelog](https://keepachangelog.com/it-IT/1.0.0/) è un sito dove viene presentata questa pratica.

- [`changelog`](https://ctan.org/pkg/changelog) — pro­vides a `changelog` en­vi­ron­ment (which it­self pro­vides a `ver­sion` en­vi­ron­ment) to rep­re­sent a changelog. The pack­age sup­ports mul­ti­ple au­thors, un­re­leased changes, and yanked (re­voked) re­leases.

## Codice condizionale

### Meccanismo prefefinito

- ❔ [LaTeX conditional expression](https://tex.stackexchange.com/questions/5894)

### Definiti dai pacchetti

- [`ifthen`](https://ctan.org/pkg/ifthen) — the pack­age's ba­sic com­mand is \ifthenelse, which can use a wide ar­ray of tests. Also pro­vided is a sim­ple loop com­mand `whiledo`.
	- 📃 [package documentation](http://mirror.utexas.edu/ctan/macros/latex/base/ifthen.pdf)
	- ❔ [Why is the ifthen package obsolete?](https://tex.stackexchange.com/questions/13866)
- [`etoolbox`](https://ctan.org/pkg/etoolbox) — it provides two interfaces to boolean flags which are completely independent of each other.

## Aggiungere nuovi comandi e ambienti

- ✏️ [From `\newcommand` to `\NewDocumentCommand`](https://www.texdev.net/2010/05/23/from-newcommand-to-newdocumentcommand/)
- ❔ [Special behavior if optional argument is not passed](https://tex.stackexchange.com/questions/217757/)
- ❔ [Space after LaTeX commands](https://tex.stackexchange.com/questions/31091/)
- ❔ [What's the difference between `\newcommand` and `\newcommand*`?](https://tex.stackexchange.com/questions/1050/)
- ❔ [What is the difference between `\def` and `\newcommand`?](https://tex.stackexchange.com/questions/655/)

### Esempi

#### Liste

	Ho preso spunto da "[Good way to make `\textcircled` numbers?](https://tex.stackexchange.com/questions/7032/)"
	```latex
	\documentclass{standalone}

	\usepackage{tikz}
	\DeclareRobustCommand\circled[1]{%
		\tikz[baseline=(char.base)]{%
	            \node[shape=circle,draw,inner sep=2pt] (char) {#1};%
		}%
	}

	\usepackage{enumitem}
	\newlist{circledlist}{enumerate}{10}
	\setlist[circledlist]{label=\circled{\arabic*}}

	\begin{document}
	Numbers aligned with the text:  \circled{1} \circled{2} \circled{3} end.

	\begin{circledlist}
		\item First item
		\item Second item
		\item Third item
		\item Fourth item
	\end{circledlist}
	\end{document}
	```

## Hooks

### hooks predefiniti

- `AtBeginDocument` — it will let you specify a set of commands that will be executed when `\begin{document}` is met.
- `AtEndDocument` — it does the same for `\end{document}`.

### Definiti dai pacchetti

- [`etoolbox`](https://ctan.org/pkg/etoolbox) — is a toolbox of programming tools geared primarily towards LATEX class and package authors. It provides LATEX frontends to some of the new primitives provided by e-TeX as well as some generic tools which are not related to [e-TeX](https://ctan.org/pkg/etex) but match the profile of this package. e-TeX is an ex­tended ver­sion of TeX. LATEX pro­gram­mers may (in all cur­rent TeX dis­tri­bu­tions) as­sume e-TEX func­tion­al­ity.
	- `AtBeginEnvironment`
	- `BeforeBeginEnvironment`
	- `AtEndEnvironment`
	- `AfterEndEnvironment`

## Contatori

- 📖 [Wikibooks](https://en.wikibooks.org/wiki/LATEX/Counters)

## Fonts

- 🍃 [Font sizes, families, and styles](https://it.overleaf.com/learn/latex/Font_sizes,_families,_and_styles)
- ✏️ [Changing the font size in LATEX](https://texblog.org/2012/08/29/changing-the-font-size-in-latex/)

- [`fontspec`](https://ctan.org/pkg/fontspec) — it is a pack­age for XELATEX and LuaLATEX. It pro­vides an au­to­matic and uni­fied in­ter­face to fea­ture-rich AAT and OpenType fonts through the NFSS in LATEX run­ning on XETEX or LuaTEX en­gines.

### Risorse

- [The LaTeX Font Catalogue](http://www.tug.dk/FontCatalogue/)
- [A Survey of Free Math Fonts for TeX and LaTeX](http://mirrors.rit.edu/CTAN/info/Free_Math_Font_Survey/en/survey.html)

#### font monospazione

- [`comfortaa`](https://ctan.org/pkg/comfortaa) — pro­vides sup­port for comfortaa font in LATEX

## Sottotitolo

- ❔ [Add a subtitle](https://tex.stackexchange.com/questions/50182/)

## Note a fine documento

- [`enoez`](https://ctan.org/pkg/enotez) — al­lows nested end­notes, sup­ports hy­per­ref and pro­vides means for easy cus­tomiza­tion of the list of notes
	- 📃 [package documentation](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/enotez/enotez_en.pdf)

## Gestione delle pagine

- [`clrdblpg`](https://ctan.org/pkg/clrdblpg) — allows easy manipulation of the headers and footers on pages left blank by `cleardoublepage`
- [`changepage`](https://ctan.org/pkg/changepage) &longrightarrow; [chngpage](https://ctan.org/pkg/chngpage) — it pro­vides com­mands to change the page lay­out in the mid­dle of a doc­u­ment, and to ro­bustly check for type­set­ting on odd or even page
	- [`changelayout`](https://ctan.org/pkg/changelayout) — extension of [`changepage`](https://ctan.org/pkg/changepage)
- [`emptypage`](https://ctan.org/pkg/emptypage) — it pre­vents page num­bers and head­ings from ap­pear­ing on empty pages.

### Output condizionale

- [`excludeonly`](https://ctan.org/pkg/excludeonly) — The pack­age de­fines an `ex­cludeonly` com­mand, which is (in ef­fect) the op­po­site of `in­cludeonly`. If both `in­cludeonly` and `ex­cludeonly` ex­ist in a doc­u­ment, only files “al­lowed” by both will be in­cluded.
- [`pagesel`] — Selects sin­gle pages, ranges of pages, odd pages or even pages for out­put.
	- 📄 [package documentation](http://ctan.math.utah.edu/ctan/tex-archive/macros/latex/contrib/oberdiek/pagesel.pdf)

### In preparazione alla pubblicazione

- [`thumbs`](https://ctan.org/pkg/thumbs) — it puts run­ning, cus­tomiz­able thumb marks in the outer mar­gin, mov­ing down­ward as the chap­ter num­ber (or what­ever shall be marked by the thumb marks) in­creases

## Documenti a due colonne

- [`multicol`](https://ctan.org/pkg/multicol) — it de­fines a mul­ti­cols en­vi­ron­ment which type­sets text in mul­ti­ple columns (up to a max­i­mum of 10), and (by de­fault) bal­ances the end of each col­umn at the end of the en­vi­ron­ment
	- 📃 [package documentation](http://ctan.math.utah.edu/ctan/tex-archive/macros/latex/required/tools/multicol.pdf)
	- [`multicolrule`](https://ctan.org/pkg/multicolrule) — lets you cus­tomize the ap­pear­ance of the ver­ti­cal rule that ap­pears be­tween columns of mul­ti­col­umn text. It is pri­mar­ily in­tended to work with the mul­ti­col pack­age, hence its name, but also sup­ports the twocol­umn op­tion and `twocol­umn` macro pro­vided by the stan­dard classes.
		- 📃 [package documentation](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/multicolrule/multicolrule.pdf)
- [`ftnright`](https://ctan.org/pkg/ftnright)
	- 📃 [package documentation](http://texdoc.net/texmf-dist/doc/latex/tools/ftnright.pdf) — Assem­bles foot­notes on two-col­umn pages at the bot­tom of the right hand col­umn.

## Margini

- [`geometry`](https://ctan.org/pkg/geometry) — it pro­vides an easy and flex­i­ble user in­ter­face to cus­tomize page lay­out, im­ple­ment­ing auto-cen­ter­ing and auto-bal­anc­ing mech­a­nisms so that the users have only to give the least de­scrip­tion for the page lay­out
	- 📃 [package documentation](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/geometry/geometry.pdf)

## documenti multi-file

- [`docmute`](https://ctan.org/pkg/docmute) — it permits to `in­put` or `in­clude` stand-alone LATEX doc­u­ments, ig­nor­ing ev­ery­thing but the ma­te­rial be­tween `be­gin{doc­u­ment}` and `end{doc­u­ment}`.
	- 📃 [package documentation](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/docmute/docmute.pdf)
- [`combine`](https://ctan.org/pkg/combine) — lets you bun­dle in­di­vid­ual doc­u­ments into a sin­gle doc­u­ment
* [`standalone`](https://ctan.org/pkg/standalone) — a class and pack­age is pro­vided which al­lows TEX pic­tures or other TEX code to be com­piled stan­dalone or as part of a main doc­u­ment. Spe­cial sup­port for pic­tures with beamer over­lays is also pro­vided. The pack­age is used in the main doc­u­ment and skips ex­tra pream­bles in sub-files. The class may be used to sim­plify the pream­ble in sub-files.
	* 📃 [package documentation](http://ctan.mirror.garr.it/mirrors/CTAN/macros/latex/contrib/standalone/standalone.pdf)
* [`import`](https://ctan.org/pkg/import) — it permits to use relative path when inputting a file that is part of a master document using custom commands, i.e. __subimport__
	* 📃 [package documentation](http://ctan.mirror.garr.it/mirrors/CTAN/macros/latex/contrib/import/import.pdf)

## Mi­cro lay­out

This topic con­tains pack­ages with para­graph shapes, mar­gin ad­just­ments, etc.

* 🔗 [paragraph formatting](https://www.overleaf.com/learn/latex/Paragraph_formatting) — The default LATEX formatting is fine and makes documents quite readable, but it can be changed if you need a different looking document. This article explains how to change the paragraph and line spacing.

- [`microtype`](https://ctan.org/pkg/microtype) — The pack­age pro­vides a LATEX in­ter­face to the mi­cro-ty­po­graphic ex­ten­sions that were in­tro­duced by pdfTEX and have since also prop­a­gated to XETEX and LuaTEX: most promi­nently, char­ac­ter pro­tru­sion and font ex­pan­sion, fur­ther­more the ad­just­ment of in­ter­word spac­ing and ad­di­tional kern­ing, as well as hy­phen­at­able let­terspac­ing (track­ing) and the pos­si­bil­ity to dis­able all or se­lected lig­a­tures.
	- 📃 [package documentation](http://ftp.math.purdue.edu/mirrors/ctan.org/macros/latex/contrib/microtype/microtype.pdf)

	```latex
	\usepackage[
	    activate = {true},
	    final,
	    tracking = true,
	    kerning  = true,
	    % spacing  = true,
	    factor   = 1100,
	    stretch  = 10,
	    shrink   = 10
	]{microtype}
	```

	To avoid hyphenation in entire phrases see [this question](https://tex.stackexchange.com/questions/91307/).

### Gestire lo spazio fra i paragrafi

- [`setspace`](https://ctan.org/pkg/setspace) — it pro­vides sup­port for set­ting the spac­ing be­tween lines in a doc­u­ment. Pack­age op­tions in­clude: `sin­glespac­ing`, `one­half­s­pac­ing`, and `dou­blespac­ing` com­mands.

### Impaginazione del paragrafo

- [`shapepar`](https://ctan.org/pkg/shapepar) — it provides a macro to type­set para­graphs in a spe­cific shape. The size is ad­justed au­to­mat­i­cally so that the en­tire shape is filled with text.

### Licenzia il materiale

- [`doclicense`](https://ctan.org/pkg/doclicense) — it al­lows you to put your doc­u­ment un­der a li­cense and in­clude a link to read about the li­cense or in­clude an icon or im­age of the li­cense. Cur­rently, only Creative Com­mons is sup­ported, but this pack­age is de­signed to han­dle all kinds of li­censes
	```latex
	\usepackage[
		type       = CC,
		modifier   = by-nc-sa,
		version    = 4.0,
		imagewidth = 4em,
	]{doclicense}
	```

- [`background`](https://ctan.org/pkg/background) — of­fers the place­ment of back­ground ma­te­rial on the pages of a doc­u­ment. The user can con­trol many as­pects (con­tents, po­si­tion, color, opac­ity) of the back­ground ma­te­rial that will be dis­played; all place­ment and at­tribute set­tings are con­trolled by set­ting key val­ues.

	```latex
	\usepackage{xparse}
	\NewDocumentCommand{\docversion}{}{\texttt{v.1.0.0}}

	\usepackage{xcolor}
	\colorlet{darkblue}{blue!50!black}

	\usepackage{background}
	\backgroundsetup{
		,pages    = all
		,contents = \fbox{\texttt{\small \doclicenseIcon Emanuele Nardi, {\docversion} - {\today}}}
		,color    = darkblue
		,position = current page.south east
		,hshift   = -6cm
		,vshift   = -1cm
		,opacity  = 1
		,angle    = -90
		,scale    = 1
	}
	```

## Citazioni

- [fancychapters](https://ctan.org/pkg/fancychapters) — pro­vides a com­mand `Chap­ter` whose first ar­gu­ment holds a quo­ta­tion to be type­set above the `chap­ter` com­mand, to which the op­tional sec­ond and manda­tory third ar­gu­ments are passed.

## Glossario

- 🔗 [Best solution for acronyms, abbreviations, glossary and index](https://tex.stackexchange.com/questions/287080/)
- 🔗 [How to combine Acronym and Glossary](https://tex.stackexchange.com/questions/8946/how-to-combine-acronym-and-glossary)

- [glossaries](https://ctan.org/pkg/glossaries) — sup­ports acronyms and mul­ti­ple glos­saries, and has pro­vi­sion for op­er­a­tion in sev­eral lan­guages (us­ing the fa­cil­i­ties of ei­ther ba­bel or poly­glos­sia). New en­tries are de­fined to have a name and de­scrip­tion (and op­tion­ally an as­so­ci­ated sym­bol). Sup­port for mul­ti­ple lan­guages is of­fered, and plu­ral forms of terms may be spec­i­fied.
	- 🔗 [Two column glossary](https://tex.stackexchange.com/questions/30812/)
	- 🔗 [Display \acrfull reversed](https://tex.stackexchange.com/questions/317227/)

## Indice

- [makeindex](https://ctan.org/pkg/makeindex) — it is a gen­eral pur­pose hi­er­ar­chi­cal in­dex gen­er­a­tor; it ac­cepts one or more in­put files (of­ten pro­duced by a text for­mat­ter such as TeX or troff), sorts the en­tries, and pro­duces an out­put file which can be for­mat­ted. The for­mats of the in­put and out­put files are spec­i­fied in a style file; by de­fault, in­put is as­sumed to be an .idx file, as gen­er­ated by LATEX.

## Bibliografia

- ❔ [Guidelines for customizing biblatex styles](https://tex.stackexchange.com/questions/12806/)
- ❔ [Add "Retrieved", "Last accessed" or similar information to authoryear in biblatex](https://tex.stackexchange.com/questions/51079/)

## Conta parole

See [➡️ atom plugins]()

- [texcount](https://ctan.org/pkg/texcount) — it is a Perl script that counts words in the text of LATEX files. It has rules for han­dling most of the com­mon macros, and can pro­vide colour-coded out­put show­ing which parts of the text have been counted.

## Utilità

- [clipboard](https://ctan.org/pkg/clipboard) — provides a basic framework for copying and pasting content within a single document or across multiple documents

## Debug

- [showkeys](https://ctan.org/pkg/showkeys) — mod­i­fies the `la­bel`, `ref`, `pageref`, `cite` and `bib­item` com­mands so that the 'in­ter­nal' key is printed, with­out af­fect­ing the ap­pear­ance of the rest of the text, so far as is pos­si­ble (the keys typ­i­cally ap­pear in the mar­gin)
- [refcheck](https://ctan.org/pkg/refcheck) — it checks ref­er­ences in a doc­u­ment, look­ing for num­bered but un­la­belled equa­tions, for la­bels which are not used in the text, for un­used bib­li­og­ra­phy ref­er­ences. It can also dis­play la­bel names in text near cor­re­spond­ing num­bers of equa­tions and/or bib­li­og­ra­phy ref­er­ences
- [latexdemo](https://ctan.org/pkg/latexdemo) — pro­vides con­fig­urable tools to print out LATEX code and the re­sult­ing out­put in the same doc­u­ment. It also sup­ports print­ing the re­sult in­side a con­di­tional se­quence; thus one may sup­press print­ing if the code would not com­pile

## Reimplementazioni di comandi e ambienti

- [xparse](https://ctan.org/pkg/xparse) —  pro­vides a high-level in­ter­face for pro­duc­ing doc­u­ment-level com­mands. In that way, it of­fers a re­place­ment for LATEX2ε’s `new­com­mand` macro, with sig­nif­i­cantly im­proved func­tion­al­ity
- [verbatim](https://ctan.org/pkg/verbatim) — it reim­ple­ments the `ver­ba­tim` and `ver­ba­tim*`` en­vi­ron­ments and a com­mand `ver­ba­tim­in­put` for type­set­ting the con­tents of a file, ver­ba­tim

## Optimization

Shortening the compile time

* `draft` — it is a document option. Setting the draft option will speed up typesetting, because _figures are not loaded_, just indicated by a frame. _LATEX will also display hyphenation_ (Overfull hbox warning) _and justification problems with a small black square_. Delete the `draft` option or replace it with `final` in the final document version.
- [draftfigure](https://ctan.org/pkg/draftfigure) —
- [trace](https://ctan.org/pkg/trace) — it re­de­fines a num­ber of key com­mands to turn off trac­ing while they ex­e­cute (those the au­thor finds most an­noy­ing and noisy). Since it po­ten­tially mod­i­fies the con­tent of other pack­ages, the pack­age __should be loaded last__ in a doc­u­ment's pream­ble.

## Tables

- [tabularx](https://ctan.org/pkg/tabularx) — it de­fines an en­vi­ron­ment tab­u­larx, an ex­ten­sion of tab­u­lar which has an ad­di­tional col­umn des­ig­na­tor, `X`, which cre­ates a para­graph-like col­umn whose width au­to­mat­i­cally ex­pands so that the de­clared width of the en­vi­ron­ment is filled
- [array](https://ctan.org/pkg/array) — an ex­tended im­ple­men­ta­tion of the ar­ray and tab­u­lar en­vi­ron­ments which ex­tends the op­tions for col­umn for­mats, and pro­vides "pro­grammable" for­mat spec­i­fi­ca­tions.
- [multirow](https://ctan.org/pkg/multirow)
	* :link: [Multi column and multi row](https://texblog.org/2012/12/21/multi-column-and-multi-row-cells-in-latex-tables/)
- [cellprops](https://ctan.org/pkg/cellprops) — reworks the internals of `tabular`, `array`, and similar constructs, and adds a `\cellprops` command accepting _CSS-like_ selectors and properties
- [makecell](https://ctan.org/pkg/makecell)
	- 🔗 [How to add a forced line break inside a table cell](https://tex.stackexchange.com/questions/2441/)
	- 🔗 [How to vertically AND left-align a cell with \makecell?](https://tex.stackexchange.com/questions/410670/)
