# CyGate: Automatic gating of single cell cytometry data

CyGate is a semiautomated method for classifying single cells into their respective cell types. CyGate learns a gating strategy from a reference data set, trains a model for cell classification, and then automatically analyzes additional data sets using the trained model. CyGate also supports the machine learning framework for the classification of “ungated” cells, which are typically disregarded by automated methods. CyGate’s utility was demonstrated by its high performance in cell type classification and the lowest generalization error on various public data sets when compared to the state-of-the-art semiautomated methods. Notably, CyGate had the shortest execution time, allowing it to scale with a growing number of samples.
<hr>

## 1. Usage
<pre>
- Command: java -jar CyGate.jar --c configFile
- Example: java -jar CyGate.jar --c foo.txt
</pre>

## 2. Parameters (See foo.txt file)
<pre>
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
</pre>
## 3. Results
<pre>
- For the files specified in Data.Sample, *_cygated.csv files are generated.
- The gating results are added to the last column, named 'Gated'.
</pre>
## 4. Data
<pre>
- To download the data used in this work, 
  visit https://drive.google.com/drive/u/1/folders/1mIR3uTnOZxciVrsooRJLr3tjkLFR3RTI
</pre>
## 5. Citation
<pre>
- CyGate Provides a Robust Solution for Automatic Gating of Single Cell Cytometry Data.
  Seungjin Na, Yujin Choo, Tae Hyun Yoon, and Eunok Paek. 
  Analytical Chemistry <b>2023</b>, 95(46), 16918-16926.
</pre>	
## 6. Rights and Permissions
<pre>
- CyGate © 2023 is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International.
  This license requires that reusers give credit to the creator. It allows reusers to distribute, 
  remix, adapt, and build upon the material in any medium or format, for noncommercial purposes only. 
  If others modify or adapt the material, they must license the modified material under identical terms.
</pre>
