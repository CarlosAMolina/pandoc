DESTINATION_PATHNAME:=/tmp/web
HTML_DESTINATION_PATHNAME:=$(DESTINATION_PATHNAME)/html
PANDOC_CONFIG_DESTINATION_PATHNAME:=$(DESTINATION_PATHNAME)/pandoc-config

md-to-html:
	rm -rf $(DESTINATION_PATHNAME)
	mkdir $(DESTINATION_PATHNAME)
	mkdir $(HTML_DESTINATION_PATHNAME)
	mkdir $(PANDOC_CONFIG_DESTINATION_PATHNAME)
	cp src/styles.css $(HTML_DESTINATION_PATHNAME)/
	cp pandoc-config/* $(PANDOC_CONFIG_DESTINATION_PATHNAME)/
	./run-pandoc src/page.md $(HTML_DESTINATION_PATHNAME)/page.html $(HTML_DESTINATION_PATHNAME)/styles.css $(PANDOC_CONFIG_DESTINATION_PATHNAME)/template.html $(PANDOC_CONFIG_DESTINATION_PATHNAME)/metadata.yml
	mkdir $(HTML_DESTINATION_PATHNAME)/other-pages
	./run-pandoc src/other-pages/page-2.md $(HTML_DESTINATION_PATHNAME)/other-pages/page-2.html $(HTML_DESTINATION_PATHNAME)/styles.css $(PANDOC_CONFIG_DESTINATION_PATHNAME)/template.html $(PANDOC_CONFIG_DESTINATION_PATHNAME)/metadata.yml

open-html:
	firefox $(HTML_DESTINATION_PATHNAME)/page.html

all: md-to-html open-html

export-template-html:
	# https://pandoc.org/MANUAL.html#option--print-default-template
	pandoc -D html > /tmp/template-default.html
