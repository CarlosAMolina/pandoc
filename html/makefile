DESTINATION_PATHNAME:=/tmp/src-html

md-to-html:
	rm -rf $(DESTINATION_PATHNAME)
	mkdir -p $(DESTINATION_PATHNAME)/other-pages
	cp src/styles.css $(DESTINATION_PATHNAME)
	cp -r pandoc-config/ /tmp/
	./run-pandoc src/page.md $(DESTINATION_PATHNAME)/page.html
	./run-pandoc src/other-pages/page-2.md $(DESTINATION_PATHNAME)/other-pages/page-2.html

open-html:
	firefox $(DESTINATION_PATHNAME)/page.html

all: md-to-html open-html

export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
