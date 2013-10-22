lapdftext-rules
===============

A project to enable other developers to use the LA-PDFText system effectively by designing their own rule files.

Examine the ```/src/test/java/edu/isi/bmkeg/lapdf/general/TestTemplate.java``` file (as shown below).

This test will run the new ```edu.isi.bmkeg.lapdf.bin.DebugLapdfFeatures.main()``` command on the ```*.pdf``` 
file using the ```*.drl``` file. 

    package edu.isi.bmkeg.lapdf.general;

    import java.io.File;
    import java.net.URL;
    import org.junit.Test;
    import edu.isi.bmkeg.lapdf.LAPDFTextEpochCheck_BaseTest;
    import edu.isi.bmkeg.utils.Converters;
    import edu.isi.bmkeg.utils.springContext.BmkegProperties;

    public class TestTemplate extends LAPDFTextEpochCheck_BaseTest
    {
        @Test
        public void test_001() throws Exception {	
            this.runBlockifyClassifyImagify(
                     "edu/isi/bmkeg/lapdf/makki-2010-8-e1000441.pdf", 
                     "edu/isi/bmkeg/lapdf/general.drl"
            );
        }
    }

The system creates three files in the ```./target/test-classes/``` subdirectory.

1. An open-access ```*.xml``` file consisting of all chunks classified as non-headers and footers (including unclassified text).
2. A directory with images for each page consisting of every block and their existing classification (with no words). 
3. A ```*.csv``` file with all the features for all the blocks precalculated. Reconfigure this file to create rules. 
 
**NOTE: This is intended as a vehicle of interaction.**
Please use develop your own rule files in this project as test cases  and then issue a pull 
request so that we can incorporate them into our system. We hope to build up a catalog.
