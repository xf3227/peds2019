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

### Installing

After resolving all dependencies, you can use the tool without further installation.

## How to use

These instructions will help you properly configure and use the tool either through function-call or command-line.

### Data format

All antibody protein sequences must be stored in plain-text format. A sequence consists of 20 amino acid symbol letters along with `"-"` to indicate gap. Sequences are deliminated by one single line-break. Please do not include spaces or extra line-breaks. The following lines show what the data is supposed to look like. Also, you can find sample data files under `<tool root>/data/sample/`

```
-QVQLVQS-GAEVKKPGSSVKVSCTTSG-GTFSS-----FVINWMRQAPGQGLGWRGGIMPV---
-EVQLLES-GGGLVQPGGSLRLSCAGSG-FTFSS-----YAMSWVRQTPGKGLEWVSVISGS---
-QVQLVES-GGGVVQSGRSLRLSCAASG-FTFRS-----HAIHWVGQAPGKGLEGVGVMSHD---
-QVHLVQS-GAEVHKPGASLRISCKASG-YTFPN-----FFLHWVRQAPGQGLEWMGIINPI---
-QVQLQES-GPGLMKPSGTLSLTCDVSG-ASISN----TNWWGWVRQPPGLGLEWIGEIHH----
```

If you want to generate data using Windows notepad, please be careful what the underlying line-break symbol is. 

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

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
