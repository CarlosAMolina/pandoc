md-to-html:
	cp index.css /tmp/
	pandoc \
		--css=index.css \
		--standalone \
		--template=pandoc-config/template.html \
		--metadata title="Carlos A Molina" \
		--metadata lang="es" \
		-t html \
		page.md \
		-o /tmp/page.html

export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
