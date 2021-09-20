You can also compile NIST "NBIS Software" to a different directory for other usage (described in following lines) with:
```bash
./setup [nonRelativePathToTheOutput] --64
make config
make it
make install LIBNBIS=yes
```
And you will find there all needed man pages and binaries.

And use the mindtct command to get minutia (or also called template) information.
```bash
mindtct [pathToWSQFile] [pathToOutputDir]/[outputBaseName]
```

And you can also use it to display a WSQ file with:
```bash
dpyimage [pathToWSQFile]
```

You could also use https://sourceafis.machinezoo.com/ library from Java to get Minutia, the standards for minutia from the NIST are INCITS 378-2004 and ISO/IEC 19794-2:2005.
reference: https://www.nist.gov/services-resources/software/biomdi-software-tools-supporting-standard-biometric-data-interchange
