# DateToBitcoinBlockConverter
This code takes a specific date in UTC time format and convert it into a new time format, the Bitcoin block number. Becasue Bitcoin blocks are created every 10 minutes in avarage, the conversion is not very precice, but precice enough for some use cases.

The thread describes another issue with the "correct time conversion": [What format is the time of a Bitcoin transaction stored in?](https://bitcoin.stackexchange.com/questions/7788/what-format-is-the-time-of-a-bitcoin-transaction-stored-in#23681)

"There are several things you could mean by the time of the transaction:"
1. When the transaction is created
2. When the transaction is known about by 90% of the network
3. When the transaction is first included into a block
4. When the block is known to 90% of the network

This code does not care about any specific transactions in a block, but more when the block is created.

# Status
Setting up project

# Overview

# Project Structure
```bash
DateToBitcoinBlockConverter
    ├── .gitignore                     # not tracked files by GIT  
    ├── app.py                         # Flask Web-App   
    ├── converter.py                   # Main file which input and output for web-app
    ├── data.csv                       # file which contains only time_stamp and block_height of all blocks
    ├── Procfile                       # process file needed for Heroku deployment
    ├── README.md   
    ├── xyz   
    │   └── xyz                        # TBD    
    ├── requirements.txt               # all needed dependencies created via: ' pip freeze > requirements.txt '
```

## Running code local on your Mac
### Installation of Heroku
1. Install Heroku CLI [Link](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
3. Check if Heroku it installed with: ```heroku --version```
4. Create an account on Heroku's website
5. After account creation, run in Terminal: ```heroku login```

### Make Code running locally
1. Clone/ download repository
2. cd into project folder

in Terminal/ CMD:

3. ```pip install virtualenv```   
4. Create virtual environment: ```virtualenv env```
5. Activate virtual environment:   
For macOS: ```source env/bin/activate```   
For Win: Copy in CMD:```"<PATH TO PROJECT>\env\Scripts\activate.bat"``` 
6. Intall dependencies:   
For macOS: ```pip3 install -r requirements.txt```   
For Win: ```pip install -r requirements.txt```   
7. Run app locally:
For macOS: ```python3 app.py```   
For Win: ```python app.py```

