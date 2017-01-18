# apmock

A set of simple tools to mock the creation of LSST raw/calibration and
catalog files and to test and tune the I/O footprint of the L1 AP processing.


### Usage

 * To create mock files:

      `mock_files -c  filemaker.ini`

      `mock_files -h` to display all options

 * To run a Alert Production Mock pipe line:

      `ap_pipe -c ap.ini`

      `ap_pipe -h` to display all options


  All option contained in the configuration can be modified from the command-line using the `—option value`


### Requirements

* python
* fitsio 
    https://github.com/esheldon/fitsio

### Configuration Files

In order to create a mock (backbone-like) archive of raw, flat, bias, templates image and catalogs, we need to first initialize this archive. The file located in `apmock/etc/filemaker.ini` provides a good example
with default values needed to create one. Please note that modifications to the `[maker-paths]` section of the `filemaker.ini` file need to be propagated to other tasks (i.e. `ap_pipe`) in order to have consistent naming convention and location of the input files


Similarly, to execute the AP Pipeline (`ap_pipe`) a default configuration file is provided in `apmock/etc/ap.ini`, all of which can be overide from the command line. Please note that definitions on `[maker-paths]` need to be kept consistent across tasks.
