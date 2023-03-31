all:


lineal-regression:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i lineal-regression.mmd -o lineal-regression.png
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i lineal-regression.mmd -o lineal-regression.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i lineal-regression.mmd -o lineal-regression.pdf

cnn:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.png
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.pdf

clean:
	rm -f *.png *.svg *.pdf