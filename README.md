# apmock

A set of simple tools to mock the creation of LSST raw/calibration and
catalog files and to test and tune the I/O footprint of the L1 AP processing.


### USAGE:

 * To create mock files:
   mock_files -c  filemaker.ini

 * To run a Alert Production Mock pipe line:
   ap_pipe -c ap.ini 
