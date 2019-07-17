# Quantifying the nativeness of antibody using LSTM

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

The tool was developped based on the following dependencies:

1. PyTorch (1.1 or greater).
2. NumPy (1.16 or greater).
3. tqdm (4.31 or greater).

Please note that the dependencies may require Python 3.6 or greater. It is recommemded to install and maintain all packages by using [`conda`](https://www.anaconda.com/) or [`pip`](https://pypi.org/project/pip/). For the installation of GPU accelerated PyTorch, additional effort may be required. Please check the official websites of [PyTorch](https://pytorch.org/get-started/locally/) and [CUDA](https://developer.nvidia.com/cuda-downloads) for detailed instructions.

## How to use

These instructions will help you properly configure and use the tool either through function-call or command-line.

## Documentation

**`ablstm.ModelLSTM.__init__()`**
> Initializes an LSTM model with the given paramters.

Parameters:

1. `embedding_dim`: *int, default is 64*
>> Embedding layer dimensions.
2. `hidden_dim`: *int, default is 64*
>> Hiddden layer dimensions.
3. `device`: *str, default is 'cpu'*
>> Device that the model will be mounted on. If GPU is available and CUDA is properly installed, you can assign `"cuda:0"` (or `"cuda:<DEVICE_INDEX>"` if you have more GPUs) that will greatly accelerate training and evaluation process.   
4. `gapped`: *bool, default is True*
>> Indicate whether the input sequences contains gaps. A gap is always signified by `"-"`.
5. `fixed_len`: *bool, default is True*
>> Indicate whether the input sequences share equal length. It can be set `False` without any issue in all circumstances, but when the sequence lengths are assured to be the same, setting it `True` will help speed up the computation significantly.

**`ablstm.ModelLSTM.fit()`**
> Fit the model via the given training and validation data.

Parameters:

1. `trn_fn`: *str*
>> Data file for training.
2. `vld_fn`: *str*
>> Data file for validation.
3. `n_epoch`: *int, default is 10*
>> Number of epochs.
4. `trn_batch_size`: *str, default is 128*
>> Batch size during training. `-1` means whole batch.
5. `vld_batch_size`: *str, default is 512*
>> Batch size during validation. `-1` means whole batch.
6. `lr`: *float, default is 0.02*
>> Learning rate. The fitting process uses Adam algorithm for optimization.
7. `save_fp`: *str, optional*
>> Path to save models. `None` or `""` means training without saving. If a valid path is given, model will be saved after each epoch as long as the validation performance is better than the past.

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
