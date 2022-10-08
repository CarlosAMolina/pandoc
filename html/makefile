DESTINATION_PATHNAME:=/tmp/web
HTML_DESTINATION_PATHNAME:=$(DESTINATION_PATHNAME)/html

md-to-html:
	rm -rf $(DESTINATION_PATHNAME)
	mkdir -p $(HTML_DESTINATION_PATHNAME)/other-pages
	cp src/styles.css $(HTML_DESTINATION_PATHNAME)
	cp -r pandoc-config/ $(DESTINATION_PATHNAME)/
	./run-pandoc src/page.md $(HTML_DESTINATION_PATHNAME)/page.html
	./run-pandoc src/other-pages/page-2.md $(HTML_DESTINATION_PATHNAME)/other-pages/page-2.html

open-html:
	firefox $(HTML_DESTINATION_PATHNAME)/page.html

all: md-to-html open-html

export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
