# cygate
Automatic gating of single cell cytometry data
<hr>

<pre>
1. Usage
- Command: java -jar CyGate.jar --c configFile
- Example: java -jar CyGate.jar --c foo.txt

2. Parameters (See foo.txt file)
- Training.Sample=
	Specify gated reference sample files for gating strategy learning (comma separated value, CSV format)
	Make sure that the CSV files have a column named 'Label' in the header, where cell labels are written.
	Multiple files can be specified by mulitple lines below.
	ex)
		Training.Sample= E:\cytof\reference_gating1.csv
		Training.Sample= E:\cytof\reference_gating2.csv
	
- Training.UngatedCellLabel=
	Specify label for UNGATED cells

- Data.Sample=
	Specify sample files or directory for automatic gating (CSV format)
	Given a directory, all files in it are gated.
	Multiple files can be specified by mulitple lines below.
	ex)
		Data.Sample= E:\cytof\data1.csv
		Data.Sample= E:\cytof\data2.csv
		Data.Sample= E:\cytof\data3.csv

3. Results
- In the directory of files specified in Data.Sample, file_cygated.csv file is generated.

</pre>
