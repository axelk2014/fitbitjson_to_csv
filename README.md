# fitbitjson_to_csv
Bash script to extract values from Fitbit data export

Fitbit allows you to export your data as json files. This script will extract the values from all heart_rate json files and convert them into CSV files.

The CSV files are limited to 500k rows to enable them being opened by most spreadsheet software. This can be changed in the script according to your needs.

System requirements:
1. bash
2. sed
3. jq (https://stedolan.github.io/jq/)


Tested on Mac OS X
GNU bash, version 3.2.57(1)-release (x86_64-apple-darwin15)
jq-1.5

Your mileage may vary with this script on different versions of the above.


## Instructions:
1. Go through the Fitbit dashboard and export the data zip file
2. Extract the zip file
3. Clone/download the Fitbitjson_to_csv.sh file and place it in the folder of the extracted fitbit zip archive
4. Run the script ``./Fitbitjson_to_csv.sh``
5. When the script stops running, you will have in the directory:
- heart.csv  which will be all the extracted heartrate jsons in csv format
- multiple "heartrate[number].csv" files which will be the split up version of heart.csv with 500k rows each


## Disclaimer:
This scripts comes without warranty of any kind. Use it at your own risk. I assume no liability for the accuracy, correctness, completeness, or usefulness of any information provided by this script nor for any sort of damages using this script may cause.
