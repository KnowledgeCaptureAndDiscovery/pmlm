ML Model Ontology

Model
* hasCategory : ModelCategory
* hasObjective : Objective
* hasInputVariable: [Variable]
* hasOutputVariable: [Variable]
* usedData: [Data]
* hasTrainedModel: [TrainedModel]
 
Data
* hasLocation: [URL]
* hasTemporalExtent: [TimePeriod]
* hasSpatialExtent: [SpatialGeometry]
 
ProcessedData
* usedSourceData: [Data]
* appliedOperation: [DataProcessingOperation]

TrainedModel
* usesAlgorithm: [Algorithm]
* usedTrainingDataset: [LabelledSet]
* hasEvaluation: [ModelEvaluation]
 
LabelledSet
* hasPredictors: [ProcessedData]
* hasPredictands: [ProcessedData]
 
 
DataProcessingOperation
* Slicing
 * TemporalSlicing
  * hasDateRange: [TimePeriod]
 * SpatialSlicing
  * hasSpatialExtents: [SpatialGeometry]
 * Reshaping
  * TemporalShaping
   * hasStackingNumber: [int]
  * SpatialReshaping
  * Flatten
 * FeatureReduction
  * PCA
 * …
* Normalization
* VarianceScaling
* NaNHandling
 * NaNSetToZero
 
 
Algorithm
* CNN
* hasLayer: [NeuralNetworkLayer]
* LinearRegression
* …
 
 
ModelEvaluation
* usedTestingDataset: [Data]
* hasEvaluationMetric: [EvaluationMetric]

