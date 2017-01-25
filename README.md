# ISPyB Documentation

This project conaints all the information that describes the tables and fields of the ISPyB database.

## Tables

### AutoProcScalingStatistics



| Field                       |  Comments |Type                                      | Null | Key | Default | Extra          |
| --------------------------- | ----------| ----------------------------------------- |----- |---- | ------- | -------------- |
| autoProcScalingStatisticsId || int(10) unsigned                          | NO   | PRI | NULL    | auto_increment |
| autoProcScalingId           || int(10) unsigned                          | YES  | MUL | NULL    |                |
| scalingStatisticsType       || enum('overall','innerShell','outerShell') | NO   | MUL | overall |                |
| comments                    || varchar(255)                              | YES  |     | NULL    |                |
| resolutionLimitLow          || float                                     | YES  |     | NULL    |                |
| resolutionLimitHigh         || float                                     | YES  |     | NULL    |                |
| rMerge                      || float                                     | YES  |     | NULL    |                |
| rMeasWithinIPlusIMinus      || float                                     | YES  |     | NULL    |                |
| rMeasAllIPlusIMinus         || float                                     | YES  |     | NULL    |                |
| rPimWithinIPlusIMinus       || float                                     | YES  |     | NULL    |                |
| rPimAllIPlusIMinus          || float                                     | YES  |     | NULL    |                |
| fractionalPartialBias       || float                                     | YES  |     | NULL    |                |
| nTotalObservations          || int(10)                                   | YES  |     | NULL    |                |
| nTotalUniqueObservations    || int(10)                                   | YES  |     | NULL    |                |
| meanIOverSigI               || float                                     | YES  |     | NULL    |                |
| completeness                || float                                     | YES  |     | NULL    |                |
| multiplicity                || float                                     | YES  |     | NULL    |                |
| anomalousCompleteness       || float                                     | YES  |     | NULL    |                |
| anomalousMultiplicity       || float                                     | YES  |     | NULL    |                |
| recordTimeStamp             || datetime                                  | YES  |     | NULL    |                |
| anomalous                   || tinyint(1)                                | YES  |     | 0       |                |
| ccHalf                      || float                                     | YES  |     | NULL    |                |
| ccAno                       || float                                     | YES  |     | NULL    |                |
| sigAno                      || varchar(45)                               | YES  |     | NULL    |                |


### AbInitioModel

One or several subtractions might have got one Abinitio models if the data analysis software has run. 


| Field                          | Comments | Type         | Null | Key | Default | Extra          |
-----------------------------------------------------------------------------------------
| abInitioModelId                || int(10)      | NO   | PRI | NULL    | auto_increment |
| modelListId                    | This is a foreign key to ModelList. Models are the ab initio pdb models derived from a curve using separate threads of the program dammif. The "Fourier transform" of each of these models should fit the Saxs curve. These models are identical to each other, though, because the information contained in a Saxs curve does not constrain them enough.| int(10)      | YES  | MUL | NULL    |                |
| averagedModelId                | This is a foreign key to Model. AverageModel is the pdb model that is constructed by the application damaver as the union of all the dammif models. It is named by the application by adding the damaver string to the initial root name. The FT of the damaver model does NOT fit the Saxs data.| int(10)      | YES  | MUL | NULL    |                |
| rapidShapeDeterminationModelId | This is a pdb model that is also constructed by the damaver application by taking the intersection of all dammif models and "inflate" this obtained skeleton until getting an adequate volume. It is named by the application by adding the damfilt string to the initial root name. The FT of the damfilt model does NOT either fit the Saxs data.| int(10)      | YES  | MUL | NULL    |                |
| shapeDeterminationModelId      | ShapeDeterminationModel is a pdb model obtained using the application dammin after running it only once and starting from the envelope named with the string damstart also previously created by the application damaver.| int(10)      | YES  | MUL | NULL    |                |
| comments                       || varchar(512) | YES  |     | NULL    |                |
| creationTime                   || datetime     | YES  |     | NULL    |                |





