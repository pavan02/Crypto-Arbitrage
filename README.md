# Crypto-Arbitrage
Python script to calculate the price difference in cryptocurrencies from some of the major exchanges across the world and India.

# Getting Started

These instructions will get you a copy of the project up and running on your local machine.

# Prerequisites

  Python version 3.5.2+ (Tested on)
  
  openpyxl,requests etc...
# Initialize
 Replace below lines in arbitrage_crypto.py to your respective emailid's and password
 
emailid_sendto = 'sample@example.com'

emailid_sendfrom = 'sample2@example.com'

password_sendfrom = 'sendfrompassword'

Note: This is to send email summary if arbitrage > 25% or Fund >=0%. Comment or remove send email function call in the code if you do not wish to recieve emails.
# Running 

$python3 arbitrage_crypto.py crypto1.xlsx 

$python3 arbitrage_crypto.py crypto2.xlsx 

# Config (optional)

Files crypto1.xlsx, crypto2.xlsx contains - Rest API's url, currency conversion and response body structure.

File format is self explanatory.

You can add additional exchanges or currencies to the list if you wish.

Note: Input files are split into two just to split the load.
 
# OUTPUT

FUND column calculates (buyprice - sellprice)/sellprice*100.

It is inspired by the difficulty in depositing fiat currencies to the international exchanges. If FUND turns out to be positive this oppurtunity can be used to fund those accounts.

Other columns are self explanatory.

Note: arbitrage_data.csv - Acts as data storage, output is dumped to this file (appended) each time the script is run.

Happy Trading :-)
