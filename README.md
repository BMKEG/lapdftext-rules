lapdftext-rules
===============

A project to enable other developers to use the LA-PDFText system effectively by designing their own rule files.

Examine the ```/src/test/java/edu/isi/bmkeg/lapdf/general/TestTemplate.java``` file (as shown below).

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




