output/papers.csv:
	mkdir -p output
	python src/download_papers.py

csv: output/cvf.csv output/cvf_without_paper_text.csv

working/no_header/papers.csv: output/papers.csv
	mkdir -p working/no_header
	tail +2 $^ > $@

working/no_header/authors.csv: output/authors.csv
	mkdir -p working/no_header
	tail +2 $^ > $@

working/no_header/paper_authors.csv: output/paper_authors.csv
	mkdir -p working/no_header
	tail +2 $^ > $@

all: csv

clean:
	rm -rf working
	rm -rf output
