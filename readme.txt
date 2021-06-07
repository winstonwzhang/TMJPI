Usage Information:

DSCI_train
Input:
- path to folder containing 4 .csv or .xlsx files. Number of rows in each file must be the same. These are the training patient features.
	- .csv or .xlsx file containing Articular Fossa features. Name of file must contain either "af" or "Articular" substrings.
	- .csv or .xlsx file containing Biological features. Name of file must contain either "bl" or "Biological" substrings.
	- .csv or .xlsx file containing Clinical features. Name of file must contain either "cl" or "Clinical" substrings.
	- .csv or .xlsx file containing Condyle Trabecular features. Name of file must contain either "ct" or "Condyle" substrings.

Output:
- file named "LUPI_model.mat" that contains the best performing ensemble of models trained from the input features.

Example usage:
./DSCI_train [Path to folder containing 4 .csv or .xlsx files]



DSCI_predict
Input:
- path to folder containing 4 .csv or .xlsx files. Number of rows in each file must be the same. These are the testing patient features.
	- .csv or .xlsx file containing Articular Fossa features. Name of file must contain either "af" or "Articular" substrings.
	- .csv or .xlsx file containing Biological features. Name of file must contain either "bl" or "Biological" substrings.
	- .csv or .xlsx file containing Clinical features. Name of file must contain either "cl" or "Clinical" substrings.
	- .csv or .xlsx file containing Condyle Trabecular features. Name of file must contain either "ct" or "Condyle" substrings.
- path to previously trained "LUPI_model.mat" file.

Output:
- file named "LUPI_pred.mat" that contains the prediction (either 1 or 0 for OA or non-OA) for each testing patient.

Example usage:
./DSCI_predict [Path to folder containing 4 .csv or .xlsx files] [Path to model file "LUPI_model.mat"]