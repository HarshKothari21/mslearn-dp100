### Tabular

- The data is read from the dataset as a table. You should use this type of dataset when your data is consistently structured and you want to work with it 
  in common tabular data structures, such as Pandas dataframes.

### Files

- The dataset presents a list of file paths that can be read as though from the file system. Use this type of dataset when your data is unstructured, 
  or when you need to process the data at the file level (for example, to train a convolutional neural network from a set of image files).
  
## Register
- tab_ds = Dataset.Tabular.from_delimited_files(path=csv_paths)
- file_ds = Dataset.File.from_files(path=(blob_ds, 'data/files/images/*.jpg'))

## Retrieving a registered dataset
- The get_by_name or get_by_id method of the Dataset class.

#Get a dataset by name from the datasets class

ds2 = Dataset.get_by_name(ws, 'img_files')

## pass a file dataset as a script argument

This provides an access point that the script can use to read the files in the dataset. In most cases, you should use as_download, 
which copies the files to a temporary location on the compute where the script is being run. However, if you are working with a large 
amount of data for which there may not be enough storage space on the experiment compute, use as_mount to stream the files directly from their source.

- script_config = ScriptRunConfig(source_directory='my_dir', script='script.py', arguments=['--ds', file_ds.as_download()])
