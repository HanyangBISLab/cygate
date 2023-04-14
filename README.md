# cygate
Automatic gating of single cell cytometry data

##################################################################

1. Usage
- Command: java -jar CyGate.jar --c configFile
- Example: java -jar CyGate.jar --c foo.txt

##################################################################

2. Parameters
- Training.Sample= <br>
  Specify gated reference sample files for gating strategy learning (comma separated value, CSV format)<br>
  Make sure that the CSV files have a column named 'Label' in the header, where cell labels are written.<br>
  Multiple files can be specified by mulitple lines below.<br>
  Training.Sample= E:\cytof\reference_gating1.csv<br>
  Training.Sample= E:\cytof\reference_gating2.csv<br>

- Training.UngatedCellLabel= <br>
  Specify label for UNGATED cells<br>

- Data.Sample= <br>
  Specify sample files or directory for automatic gating (CSV format)<br>
  Given a directory, all files in it are gated.<br>
  Multiple files can be specified by mulitple lines.<br>
  Data.Sample= E:\cytof\data1.csv<br>
  Data.Sample= E:\cytof\data2.csv<br>
  Data.Sample= E:\cytof\data3.csv<br>
  
- See foo.txt file.

3. Results
  Itn the directory of files specified in Data.Sample, file_cygated.csv file is generated.<br>
