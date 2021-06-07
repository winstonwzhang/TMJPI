Usage Information:

DSCI_train
Input:
- [Folder path]: path to folder containing 4 .csv or .xlsx files. Number of rows in each file must be the same. These are the training patient features.
	- .csv or .xlsx file containing Articular Fossa features. Name of file must contain either "af" or "Articular" substrings.
	- .csv or .xlsx file containing Biological features. Name of file must contain either "bl" or "Biological" substrings.
	- .csv or .xlsx file containing Clinical features. Name of file must contain either "cl" or "Clinical" substrings.
	- .csv or .xlsx file containing Condyle Trabecular features. Name of file must contain either "ct" or "Condyle" substrings.

Output:
- file named "LUPI_model.mat" that contains the best performing ensemble of models trained from the input features.
  The file is output to [Folder path]

Example usage:
./DSCI_train [Folder path]



DSCI_predict
Input:
- [Folder path]: path to folder containing 4 .csv or .xlsx files. Number of rows in each file must be the same. These are the testing patient features.
	- .csv or .xlsx file containing Articular Fossa features. Name of file must contain either "af" or "Articular" substrings.
	- .csv or .xlsx file containing Biological features. Name of file must contain either "bl" or "Biological" substrings.
	- .csv or .xlsx file containing Clinical features. Name of file must contain either "cl" or "Clinical" substrings.
	- .csv or .xlsx file containing Condyle Trabecular features. Name of file must contain either "ct" or "Condyle" substrings.
- [Model path] path to previously trained "LUPI_model.mat" file.

Output:
- file named "LUPI_pred.mat" that contains the prediction (either 1 or 0 for OA or non-OA) for each testing patient.
  The file is output to [Folder path].

Example usage:
./DSCI_predict [Folder path] [Model path]
