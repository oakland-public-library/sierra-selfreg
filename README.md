# millennium-selfreg

Customized Patron Self Registration for Innovative Sierra

This form was created to suit the needs of the [Oakland Public Library](http://www.oaklandlibrary.org). The sample form distributed by Innovative provides only trivial input validation, and relatively inflexible token-replacement for user-facing display elements.

Features:

- Highlighting on empty/unacceptable fields with accompanying help messages
- Display different form fields based on patron age using CSS
- Calculate age based on birth date
- Printer-friendly confirmation page using CSS
- Validation of format for email and phone number fields
- Convert city name to library jurisdiction code

### Importing Language Strings from Excel

To help collect translated language strings, the python script `csv_to_js.py` will convert a CSV file to a snippet of javascript code that can be used in `language_tokens.js`. CSV files exported by Microsoft Excel may need to be converted to UNIX style line endings and/or ISO codeset. After exporting `token_data.xlsx` to `token_data.csv`, try the following to generate the required snippet:

    dos2unix -c iso token_data.csv
    ./csv_to_js.py

### Email Confirmation Message

Confirmation messages sent via email by the Millenium/Sierra server use content from the live/screens file `newpat.html` and is not handled by this script.
