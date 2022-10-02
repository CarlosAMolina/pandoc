md-to-html:
	cp index.css /tmp/
	pandoc \
		--css=index.css \
		--standalone \
		--template=pandoc-config/template.html \
		-t html \
		pandoc-config/metadata.yml \
		page.md \
		-o /tmp/page.html

open-html:
	firefox /tmp/page.html

all: md-to-html open-html


export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
