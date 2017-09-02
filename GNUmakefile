N = $(PWD)/node_modules/.bin/

.SUFFIXES:
.PHONY: all clean
.PRECIOUS: node_modules build/%.html

all: node_modules build/pres.html

clean:
	rm -rf build

node_modules:
	npm i

build/%.html: src/%.md
	mkdir -p $(dir $@)
	$(N)markdown-to-slides -d --level 2 -o $@ $<
