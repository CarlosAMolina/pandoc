md-to-html:
	rm -rf /tmp/src-html
	mkdir -p /tmp/src-html/other-pages
	cp src/styles.css /tmp/src-html
	cp -r pandoc-config/ /tmp/
	pandoc \
		--css=/tmp/src-html/styles.css \
		--standalone \
		--template=/tmp/pandoc-config/template.html \
		-t html \
		/tmp/pandoc-config/metadata.yml \
		src/page.md \
		-o /tmp/src-html/page.html
	pandoc \
		--css=/tmp/src-html/styles.css \
		--standalone \
		--template=/tmp/pandoc-config/template.html \
		-t html \
		/tmp/pandoc-config/metadata.yml \
		src/other-pages/page-2.md \
		-o /tmp/src-html/other-pages/page-2.html

open-html:
	firefox /tmp/src-html/page.html

all: md-to-html open-html


export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
