md-to-html:
	rm -rf /tmp/src-html
	mkdir -p /tmp/src-html/other-pages
	cp src/styles.css /tmp/src-html
	cp -r pandoc-config/ /tmp/
	./run-pandoc src/page.md /tmp/src-html/page.html
	./run-pandoc src/other-pages/page-2.md /tmp/src-html/other-pages/page-2.html

open-html:
	firefox /tmp/src-html/page.html

all: md-to-html open-html


export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
