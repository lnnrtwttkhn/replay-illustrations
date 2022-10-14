# Replay Illustrations

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![made-with-datalad](https://www.datalad.org/badges/made_with.svg)](https://datalad.org)

## About

This repository contains illustrations that I regularly use in talks about [my work](https://scholar.google.de/citations?user=GXvJB1kAAAAJ&hl=de&oi=ao) on investigating fast sequential memory reactivation (replay) in humans using fMRI.

## DataLad datasets and how to use them

This repository is a [DataLad](https://www.datalad.org/) dataset.
It provides fine-grained data access down to the level of individual files, and allows for tracking future updates.
In order to use this repository for data retrieval, [DataLad](https://www.datalad.org/) is required.
It is a free and open source command line tool, available for all major operating systems, and builds up on Git and [git-annex](https://git-annex.branchable.com/) to allow sharing, synchronizing, and version controlling collections of large files.
You can find information on how to install DataLad at [handbook.datalad.org/en/latest/intro/installation.html](http://handbook.datalad.org/en/latest/intro/installation.html).

### Get the dataset

This DataLad dataset can be `cloned` by running

```bash
datalad clone https://github.com/lnnrtwttkhn/replay-illustrations
```

Once the dataset is cloned, it is a light-weight directory on your local machine.
At this point, it contains only small metadata and information on the identity of the files in the dataset, but not actual *content* of the (sometimes large) data files.

### Retrieve dataset content

After cloning a dataset, you can retrieve file contents by running

```bash
datalad get <path/to/directory/or/file>`
```

This command will trigger a download of the files, directories, or subdatasets you have specified.

For example, you can retrieve all illustrations in `.pdf`-format by running

```bash
datalad get illustrations/*/*.pdf
```

### Stay up-to-date

DataLad datasets can be updated.
The command `datalad update` will *fetch* updates and store them on a different branch (by default `remotes/origin/master`).
Running

```bash
datalad update --merge
```

will *pull* available updates and integrate them in one go.

### Find out what has been done

DataLad datasets contain their history in the ``git log``.
By running ``git log`` (or a tool that displays Git history) in the dataset or on specific files, you can find out what has been done to the dataset or to individual files by whom, and when.

### More information

More information on DataLad and how to use it can be found in the DataLad Handbook at [handbook.datalad.org](http://handbook.datalad.org/en/latest/index.html).
The chapter "DataLad datasets" can help you to familiarize yourself with the concept of a dataset.

## Requirements

### Affinity Designer

To edit the `.afdesign` files you need [Affinity Designer](https://affinity.serif.com/de/designer/).
I currently use version 1.5.5.
Affinity Designer is not free but cheaper than Adobe Illustrator.

## Credit

Several illustrations contain images from [BioRender.com](https://biorender.com/) which were created under a plan for the [Max Planck Society](https://www.mpg.de/en) which allows publication in journals and for other academic purposes (for details, see BioRender's [overview of Licensing and Usage](https://public.biorender.com/info/plans.pdf)).
The illustrations are used for academic purposes only.

Illustrations in [`replay-linear-track`](illustrations/replay-linear-track) were inspired by Figure 1 in [Carr et al., 2011, *Nature Neuroscience*](https://doi.org/10.1038/nn.2732).
Please refer to the original paper for reference:

> Carr, M., Jadhav, S. & Frank, L. Hippocampal replay in the awake state: a potential substrate for memory consolidation and retrieval. *Nature Neuroscience* 14, 147–153 (2011). https://doi.org/10.1038/nn.2732

## License

All illustrations are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
Details can be found in the [LICENSE](LICENSE) file.

## Contact

If you have questions or any suggestions for improvement, please [contact Lennart Wittkuhn](mailto:wittkuhn@mpib-berlin.mpg.de) or [create a new issue on the issue board](https://github.com/lnnrtwttkhn/replay-illustrations/issues).
Thank you! :pray:


