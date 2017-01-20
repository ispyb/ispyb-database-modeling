# ISPyB Documentation

This project conaints all the information that describes the tables and fields of the ISPyB database.

## Tables

### AutoProcScalingStatistics

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |


| Field                       | Type                                      | Null | Key | Default | Extra          |
| --------------------------- | ----------------------------------------- |----- |---- | ------- | -------------- |
| autoProcScalingStatisticsId | int(10) unsigned                          | NO   | PRI | NULL    | auto_increment |
| autoProcScalingId           | int(10) unsigned                          | YES  | MUL | NULL    |                |
| scalingStatisticsType       | enum('overall','innerShell','outerShell') | NO   | MUL | overall |                |
| comments                    | varchar(255)                              | YES  |     | NULL    |                |
| resolutionLimitLow          | float                                     | YES  |     | NULL    |                |
| resolutionLimitHigh         | float                                     | YES  |     | NULL    |                |
| rMerge                      | float                                     | YES  |     | NULL    |                |
| rMeasWithinIPlusIMinus      | float                                     | YES  |     | NULL    |                |
| rMeasAllIPlusIMinus         | float                                     | YES  |     | NULL    |                |
| rPimWithinIPlusIMinus       | float                                     | YES  |     | NULL    |                |
| rPimAllIPlusIMinus          | float                                     | YES  |     | NULL    |                |
| fractionalPartialBias       | float                                     | YES  |     | NULL    |                |
| nTotalObservations          | int(10)                                   | YES  |     | NULL    |                |
| nTotalUniqueObservations    | int(10)                                   | YES  |     | NULL    |                |
| meanIOverSigI               | float                                     | YES  |     | NULL    |                |
| completeness                | float                                     | YES  |     | NULL    |                |
| multiplicity                | float                                     | YES  |     | NULL    |                |
| anomalousCompleteness       | float                                     | YES  |     | NULL    |                |
| anomalousMultiplicity       | float                                     | YES  |     | NULL    |                |
| recordTimeStamp             | datetime                                  | YES  |     | NULL    |                |
| anomalous                   | tinyint(1)                                | YES  |     | 0       |                |
| ccHalf                      | float                                     | YES  |     | NULL    |                |
| ccAno                       | float                                     | YES  |     | NULL    |                |
| sigAno                      | varchar(45)                               | YES  |     | NULL    |                |


