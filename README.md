ML Model Ontology

Model
hasDomain : Domain
hasObjective : Objective
hasInputVariables: [Variable]
hasOutputVariables: [Variable]
usesData: [Dataset]
hasTrainedModel: [TrainedMLModel]
 
Dataset
hasLocation: [URL]
hasTimePeriod: [TimePeriod]
hasSpatialExtent: [SpatialGeometry]
 
TrainedMLModel
usesAlgorithm: [MLAlgorithm]
usedMLTrainingDataset: [MLDataset]
hasEvaluation: [MLModelEvaluation]
 
MLDataset
hasPredictors: [MLProcessedData]
hasPredictands: [MLProcessedData]
 
MLProcessedData
hasSourceData: [Dataset]
hasOperation: [MLDataOperation]
 
MLDataOperation
Slicing
TemporalSlicing
hasDateRange: [TimePeriod]
SpatialSlicing
hasSpatialExtents: [SpatialGeometry]
Reshaping
TemporalShaping
hasStackingNumber: [int]
SpatialReshaping
Flatten
FeatureReduction
PCA
…
Normalization
VarianceScaling
NaNHandling
NaNSetToZero
 
 
MLAlgorithm
CNN
hasLayer: [NeuralNetworkLayer]
LinearRegression
…
 
 
MLModelEvaluation
usedMLTestingDataset: [MLDataset]
hasEvaluationMetric: [MLEvaluationMetric]

