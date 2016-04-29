pl-macro-etym.pdf : pl-macro-etym.md
	cat pl-macro-etym.md works-cited.md > pl-macro-etym-full.md
	pandoc -o $@ pl-macro-etym-full.md \
		--smart \
		--latex-engine=xelatex \
		-V colorlinks \
		-V mainfont='Linux Libertine O' \
		--filter pandoc-crossref \
		--filter pandoc-citeproc
	evince '$@' &

mla: 
	cat pl-macro-etym.md works-cited.tex > pl-macro-etym-full.md
	pandoc -o pl-macro-etym-mla.pdf pl-macro-etym-full.md \
		--smart \
		-V colorlinks \
		-V mainfont='Linux Libertine O' \
		--latex-engine=xelatex \
		--template=mla-template.tex \
		--filter pandoc-crossref \
		--filter pandoc-citeproc
	evince pl-macro-etym-mla.pdf &
