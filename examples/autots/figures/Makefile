all:
	make data-preprocessing_training
	make data-preprocessing_testing
	make training_lineal-regression
	make training_cnn
	make pplan

data-preprocessing_testing:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/testing-activity.mmd -o data-preprocessing/testing-activity.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/testing-activity.mmd -o data-preprocessing/testing-activity.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/testing-activity.mmd -o data-preprocessing/testing-activity.pdf


data-preprocessing_training:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/training-activity.mmd -o data-preprocessing/training-activity.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/training-activity.mmd -o data-preprocessing/training-activity.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i data-preprocessing/training-activity.mmd -o data-preprocessing/training-activity.pdf

training_lineal-regression:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/lineal-regression.mmd -o training/lineal-regression.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/lineal-regression.mmd -o training/lineal-regression.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/lineal-regression.mmd -o training/lineal-regression.pdf


training_cnn:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/cnn.mmd -o training/cnn.pdf

training_full:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/full.mmd -o training/full.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/full.mmd -o training/full.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i training/full.mmd -o training/full.pdf


plan:
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/cnn.mmd -o pplan/cnn.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/cnn.mmd -o pplan/cnn.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/cnn.mmd -o pplan/cnn.pdf
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/data-preprocessing-training.mmd -o pplan/data-preprocessing-training.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/data-preprocessing-training.mmd -o pplan/data-preprocessing-training.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/data-preprocessing-training.mmd -o pplan/data-preprocessing-training.pdf
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/lineal-regression.mmd -o pplan/lineal-regression.png -w 2000
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/lineal-regression.mmd -o pplan/lineal-regression.svg
	docker run --rm -u `id -u`:`id -g` -v ${PWD}:/data minlag/mermaid-cli -i pplan/lineal-regression.mmd -o pplan/lineal-regression.pdf


clean:
	rm -f */*.png -w 2000 */*.svg */*.pdf