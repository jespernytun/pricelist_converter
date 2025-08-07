# pricelist converter
#### Made at work to convert a price-list from PDF to Excel to import the prices to save time during my summerinternship at NorskeNettbutikker
Being present working full time at their warehouse in Bergen sometimes left me with time left over to do some experimentation, and this is one of the projects that came as a result
#### This project is being shared with permission of my employer
The comments have been made in Norwegian (with no experience in coding) to help my employer use it if he ever so wished to

## The problem this solves
Not all suppliers have their pricelists in CSV or Excel formats, something that makes it impossible to import their price lists with our current tools <br>
I made this program to convert a 150+ pages long pricelist from one of our suppliers into an importable pricelist <br>

It has saved me a lot of time since conception, and have been used with multiple of such vendors (the Regex had to be changed each time, but that takes a lot less time than manually changing hundreds of prices)

## How it solves it
The code takes an PDF formatted pricelist as an imput, using pdfplumber, and uses simple for loops to check every line on every page <br>
We use re to seach for regular expressions on those lines to identify different things (prices, descriptions, article ID etc) <br>
It then takes all the info and stores in an xlsx file, that can be used for importation, using pandas <br>

## DISCLAIMER
The example.pdf file I have uploaded along with this project is not an official pricelist from any supplier in any capacity. **All prices have been REDACTED, along with item IDs and product descriptions.**

The calculations for contribution margins (or equivalent) have either been set to one. The numbers in the second project are given a random multiplier just to make the output look nicer, and are not our actual prices.
