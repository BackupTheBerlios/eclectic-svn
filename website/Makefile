all : docs

docs : doc-overview doc-developer-guide doc-user-guide doc-release-guide

upload :
	scp *.content *.css *.shtml \
	shell.berlios.de:/home/groups/eclectic/htdocs/

doc-% : ../trunk/doc/%.txt
	cp $? ./$*.txt
	rst2html.py < $*.txt | sed -n -e '/<body>/,/<\/body>/p' > $*.content



