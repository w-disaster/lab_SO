SHELL=/bin/bash
CFLAGS=-ansi -Wpendantic -Wall

all: tutto.txt
	
tutto.txt: B1.txt B2.txt	
	touch tutto.txt && cat B1.txt > tutto.txt && cat B2.txt >> tutto.txt

B1.txt: A1.txt
	cat A1.txt > B1.txt && printf "\n" > B1.txt

A1.txt:
	echo "AAAA" > A1.txt 
 
B2.txt: A2.txt
	printf "\n" > B2.txt && cat A2.txt >> B2.txt

A2.txt:
	echo "ZZZZ" > A2.txt

.PHONY: clean touch

clean:	
	rm A1.txt A2.txt

touch:
	if [[  -e  B1.txt  ]] ; then touch B1.txt ; fi
