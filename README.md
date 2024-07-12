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
	ex)
	   Training.UngatedCellLabel= NA
	   
- Data.Sample=
	Specify sample files or directory for automatic gating (CSV format)
	Given a directory, all files in it are gated.
	Multiple files can be specified by mulitple lines below.
	ex)
	   Data.Sample= E:\cytof\data1.csv
	   Data.Sample= E:\cytof\data2.csv
	   Data.Sample= E:\cytof\data3     #possible to specify directory

3. Results
- For the files specified in Data.Sample, *_cygated.csv files are generated.
- The gating results are added to the last column, named 'Gated'.

4. Data
- To download the data used in this work, visit https://drive.google.com/drive/u/1/folders/1mIR3uTnOZxciVrsooRJLr3tjkLFR3RTI
</pre>

## 5. Rights and Permissions
<pre>
- CyGate © 2023 is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International.
  This license requires that reusers give credit to the creator. It allows reusers to distribute, 
  remix, adapt, and build upon the material in any medium or format, for noncommercial purposes only. 
  If others modify or adapt the material, they must license the modified material under identical terms.
</pre>
