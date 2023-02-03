# ML Model Ontology

## Ontology Terms

### Data Entities & their properties
Data ⊆ prov:Entity
* usedSourceData: [Data]
* appliedOperation: [DataProcessingOperation]
* hasSpatialCoverage [SpatialGeometry]
* hasTemporalCoverage [TimePeriod]
* hasURI [anyURI]

LabelledDataset ⊆ prov:Entity
* hasPredictors: [Data] or [Tensor]
* hasPredictands: [Data] or [Tensor]

TrainingDataset ⊆ LabelledDataset

TestingDataset ⊆ LabelledDataset

TrainedModel ⊆ prov:Entity
* usesAlgorithm: [Algorithm]
* usedTrainingDataset: [TrainingDataset]
* hasEvaluation: [ModelEvaluation]

-------------
#### Data Class Hierarchy

* Data
	* GraphData
	* Image
	* SequentialData
		* Audio
		* Text
		* TimeSeries
		* Video
	* TabularData
	* VolumetricData


----------

### Algorithm Properties and Class Hierarchy

Algorithm
* usesFramework: [SoftwareFramework]
* hasParameter: [AlgorithmObject]

NeuralNetwork ⊆ Algorithm
* hasLayer: [Layer]

#### Algorithm and related Classes Hierarchy
----------
* Algorithm
	* DecisionTree
	* EnsembleAlgorithm
		* GradientBoosting
		* RandomForest
	* KernelMethod
		* SupportVectorMachine
	* LinearAlgorithm
		* LinearRegression
		* LogisticRegression
	* NeuralNetwork
		* ConvolutionalNeuralNetwork
		* EncoderDecoderModel
			* Transformer
		* GenerativeAdversarialNetwork
		* GraphNeuralNetwork
		* RecurrentNeuralNetwork
			* LongShortTermMemory
	* ProbabilisticAlgorithm
		* LogisticRegression
		* NaiveBayes

----------

* AlgorithmObject
	* NativeParameter
		* BooleanParameter
		* FloatParameter
		* IntegerParameter
		* StringParameter
			* EnumeratedParameter
	* NeuralNetworkObject
		* Layer
			* ActivationLayer
				* HardActivation
					* HardTanH
					* ReLU
						* LeakyRelU
				* SmoothActivation
					* Sigmoid
					* SoftPlus
					* TanH
			* ConvolutionLayer
				* Conv1D
				* Conv2D
				* Conv3D
			* DenseLayer
			* Downsample
				* AveragePooling
				* MaxPooling
					* MaxPool1D
					* MaxPool2D
					* MaxPool3D
			* RecurrentLayer
				* GRU
				* LSTM
				* SimpleRNN
		* LossFunction
		* Optimizer
	* Tensor
		* Tensor0D
		* Tensor1D
		* Tensor2D
		* Tensor3D
		* Tensor4D
		* Tensor5D


-----------

* LearningApproach
	* ReinforcementLearning
	* SemiSupervisedLearning
	* SupervisedLearning
		* Classification
			* BinaryClassification
			* MultiClassClassification
		* Regression
	* UnsupervisedLearning
		* Clustering
		* DimensionalityReduction


--------------

* LearningTask
	* AudioTask
		* AudioClassification
		* TextToSpeech
	* MultiModalTask
		* ImageToText
		* TextToImage
	* TabularTask
		* TabularClassification
		* TabularRegression
	* TextTask
		* QuestionAnswering
		* Summarization
		* TextClassification
		* TextGeneration
		* Translation
	* TimeSeriesTask
		* TimeSeriesForecasting
	* VisionTask
		* ImageClassification
		* ImageGeneration
		* ImageSegmentation
		* ObjectDetection

-------------
* SoftwareFramework
	* Keras
	* PyTorch
	* SkLearn
	* Tensorflow


-----------
### DataPreprocessing Class Hierarchy

* DataPreprocessing
	* DimensionalityReduction
	* FeatureEngineering
	* FeatureExtraction
	* HandlingMissingValues
	* Normalization
	* Reshaping
	* Vectorization
		* ImageVectorization
			* ImageEmbedding
		* TextVectorization
			* OneHotEncoding
			* WordEmbedding


-------------

### Activities & their properties

DataPreprocessingActivity ⊆ prov:Activity
* usedInput : [Data] or [Tensor]
* appliedDataPreprocessing: [DataPreprocessing]
* producedOutput : [Data] or [Tensor]
 
-----------

TrainingActivity ⊆ prov:Activity
* usedInput: [TrainingData]
* usedAlgorithm: [Algorithm]
* usedLearningApproach: [LearningApproach]
* hadLearningTask: [LearningTask]
* producedTrainedModel: [TrainedModel]

-----------
 

 
