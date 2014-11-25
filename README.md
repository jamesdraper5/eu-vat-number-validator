# EU VAT Number Validator

Validates the format of VAT numbers for EU countries.


## Usage

This function checks the validity of the format of an EU VAT number specified by the supplied parameter. Note that it does not check whether the code is currently allocated - this may done by interrogating the [EU database](http://ec.europa.eu/taxation_customs/vies/vieshome.do?selectedLanguage=EN).

The specifications of valid VAT numbers were originally gleaned from a variety of sources found on the web, but have since been confirmed using a VIES document. All necessary check digit validation is performed except for the new style French TVA numbers, which are not thought to be yet in use.

Non-EU Norwegian, Serbian, Swiss and Russian VAT formats are also supported.

In this JavaScript function, the country code is mandatory apart from those belonging to the UK, in which case it is optional. A description of how to make a different country's code the default is described in the embedded comments within the downloadable JavaScript code.

Embedded spaces, commas, points, and dashes are accepted, and capitalisation is ignored. If the parameter is a valid VAT number, the function returns the number with any extra characters removed and lower case alphabetic characters converted to uppercase. Otherwise it returns a value of false.

## Example

Simply call the function, passing the VAT number to it:

```
if (checkVATNumber(myVATNumber)) {
  alert("VAT number has a valid format")
} else { 
  alert("VAT number has invalid format");
}
```


## Author

This library was originally created by [John Gardner](http://www.braemoor.co.uk/software/) who kindly gave [me](http://www.jamesdraper.info) permission to add it to Github. A full changelog and pre-Github acknowledgements can be viewed [here](http://www.braemoor.co.uk/software/vatupdates.shtml).
