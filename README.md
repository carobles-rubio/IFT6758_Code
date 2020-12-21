# IFT6758_Code
Code for IFT6758 Kaggle Project

Main file:  notebook.ipynb

## How to run the code:
- You need to have OpenCV installed
- The training and testing CSV files must be in the same directory as the notebook
- The training images must be in this directory: './train_profile_images/profile_images_train/'
- The testing images must be in this directory: './test_profile_images/profile_images_test/'
- Load the file 'notebook.ipynb'
- Run the whole code and it will output file 'predictions.csv'
- This file has the predictions we submited to Kaggle for Kernel Ridge (no feature selection)


## Additional results

If you want to obtain other predictions, replace the variable `kridgeReg` with the desired predictor in the following line after the "Testing" heading (box `In [33]`):

`out['Predicted'] = (np.exp(kridgeReg.predict(tst_df.iloc[:,1:-1]))-1).astype('int32') # TODO: real predictions`

Replace by the following:
- `lassoReg` to get the Lasso results submitted to Kaggle.
- `kridgeWLasso` to get the Kernel Ridge with Feature Selection by Lasso results submitted to Kaggle.