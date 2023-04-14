# cygate
Automatic gating of single cell cytometry data

##################################################################

1. Usage
- Command: java -jar CyGate.jar --c configFile
- Example: java -jar CyGate.jar --c foo.txt

##################################################################

2. Parameters
- Training.Sample= 
  Specify gated reference sample files for gating strategy learning (comma separated value, CSV format)
  Make sure that the CSV files have a column named 'Label' in the header, where cell labels are written.
  Multiple files can be specified by mulitple lines below.
  Training.Sample= E:\cytof\reference_gating1.csv
  Training.Sample= E:\cytof\reference_gating2.csv

- Training.UngatedCellLabel= 
  Specify label for UNGATED cells

- Data.Sample= 
  Specify sample files or directory for automatic gating (CSV format)
  Given a directory, all files in it are gated. 
  Multiple files can be specified by mulitple lines.
  Data.Sample= E:\cytof\data1.csv
  Data.Sample= E:\cytof\data2.csv
  Data.Sample= E:\cytof\data3.csv
  
  See foo.txt file.
