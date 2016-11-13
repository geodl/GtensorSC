# The Data Format:
The input of the algorithm is a *non-negative*, *symmetric*, *square* tensor. If your data do not meet these requirements, please preprocess the data. For the data file, each row represent one non-zero element of the tensor, with the format index1, index2, ... , value.

## English n-gram Data
Please visit [here](http://www.ngrams.info) to
register and get the 1-million freelist n-gram data. After downloading the data, we will have
* `w3_.txt` the text file of 3gram English data
* `w4_.txt` the text file of 4gram English data

**Put the above two files** in the `English_ngram` folder then run the python script `ngramEn.py` Under `script` folder to generate the tensor data:
```bash
$ cd script
$ python ngramEn.py
```
You will have the following four files:
* `tensor_w3_.txt`
* `dic_w3_.txt`
* `tensor_w4_.txt`
* `dic_w4_.txt`

where `tensor_w3_.txt` and `tensor_w4_.txt` are the tensors with sparse tensor format. `dic_w3_.txt` and `dic_w4_.txt` are the dictionary between nodes in the tensor and actual words.

## Chinese n-gram Data
Click [here](https://www.cs.purdue.edu/homes/wu577/data/Chinese_ngram.zip)
to download Chinese n-gram data. **Put** the folder `Chinese_ngram` folder under the `data` folder. then run the python script `ngramCh.py` Under `script` folder to generate the tensor data:
```bash
$ cd script
$ python ngramCh.py
```
Similar with the English n-gram case, you will have two tensors with dic files.


## Enron Data
Click [here](https://www.cs.purdue.edu/homes/wu577/data/Enron.zip)
to download the Enron data. **Put** the folder `Enron` under the `data` folder. You will have a tensor with its dic file.


## Openflight Data
It is already included in the openFlight folder:
* `airline.txt` contains ID and airline description
* `airport.txt` contains ID and airport description
* `tensor_openflight.txt`   is the tensor data
* `dic_openflight.txt`  ID (first number) of the tenosr and ID (second number) of the airline/airport (539airlines+2939airports).
* `rectangle.txt`  is the raw rectangular tensor of openFlight data.

