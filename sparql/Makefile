LANGS ?= en nl ja

CODEFILES: \
 $(shell groovy ../findScripts.groovy ../src .out | sort | uniq)

.PRECIOUS: %.java %.groovy

all: allScriptsCompiled

distclean: clean
	@rm -f *.md *.out

clean:
	@rm -f *~ allScriptsCompiled

allScriptsCompiled: ${CODEFILES}
	@touch allScriptsCompiled

%.out: %.rq md.*.template
	@echo -n "doing $@ ... "
	@for lang in $(LANGS) ; do \
		echo -n "$$lang " ; \
		groovy preprocess $< $$lang > `echo "$@" | sed s/.out/.$$lang.out/` ; \
		groovy postprocess $< $$lang ; \
	done
	@echo ""
