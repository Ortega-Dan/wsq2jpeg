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


You can convert a jpeg image to a WSQ file from commands as well by following this steps with the corresponsing binaries:

Important !!!! Make sure the input jpeg is 8 bit grayscale otherwise youll get an error in the process mentioning something about "24 != 8".

```bash
djpegb nist [pathToYour8bitGrayscaleJpeg]
```
(the .nist file will be written next to the input jpeg)

then ...
```bash
cwsq 2.75 wsq [pathToDotNistFileFromPreviousCommand]
```


Information was found in official documentation (download from):
https://www.nist.gov/publications/users-guide-nist-biometric-image-software-nbis

![howTo](https://user-images.githubusercontent.com/24926168/134080429-feb25dfd-3b7b-4592-9c06-0d0d26f8ccaa.png)


You could also use https://sourceafis.machinezoo.com/ library from Java to get Minutia,
with: https://sourceafis.machinezoo.com/java
and
https://sourceafis.machinezoo.com/javadoc/com/machinezoo/sourceafis/FingerprintImage.html

the standards for minutia from the NIST are INCITS 378-2004 and ISO/IEC 19794-2:2005.
reference: https://www.nist.gov/services-resources/software/biomdi-software-tools-supporting-standard-biometric-data-interchange

