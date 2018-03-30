![alt text](https://i.imgur.com/epNr8Vs.jpg)
```
:::::::..  .,:::::::::::::-.   .,:::::: .,::::::  .        :   .,::::::  :::::::..   
;;;;``;;;; ;;;;""`" ;;,   `';,,;;;;""`" ;;;;""`"  ;;,.    ;;;  ;;;;""`"  ;;;;``;;;;  
 [[[,/[[['  [[cccc  `[[     [[  [[cccc   [[cccc   [[[[, ,[[[[,  [[cccc    [[[,/[[['  
 $$$$$$c    $$""`"   $$,    $$  $$""`"   $$""`"   $$$$$$$$"$$$  $$""`"    $$$$$$c    
 888b "88bo,888oo,__ 888_,o8P'  888oo,__ 888oo,__ 888 Y88" 888o8888ooo,__ 8888b 88bo,
 MMMM   "W" ""`"YUMMMMMMMP"`    ""`"YUMMM`"'"YUMMMMMM  M'  "MMM"'""YUMMMMMMMM   "WW" 
```

# Welcome to Redeemer

Leqet is an old Hebrew concept.  In order to protect the more disadvantaged members of society, God had the Hebrews institute a practice known as Leqet whereby the poor could come by the fields and glean what was left over after harvest.  The practice is made famous in the *Book of Ruth* who met her future kinsman redeemer, Boaz, while gleaning in his fields.  This is exaclty what this program does.  It gleans the tick data from the web (ruth.py), so that we, the disadvantaged, non-institutionalized equity traders can glean a little of the fortune left behind by Wall Street. But ```Ruth``` is only the first installment in this trilogy.  One day, this program may be able to redeem you quite a bit of cash.

See ["Future Improvements"](https://github.com/kotamichael/Redeemer#future-improvements) for more.

## -----------------IMPORTANT NOTICE REGARDING V2.0 ------------

For those select few of you who joined when it was just lonely Ruth, this new rollout is a massive overhaul. Boaz has caught Ruth gleaning in his field, and the romance has begun.  In order to begin this beautiful trilogy, the user must delete the old ```Redeemer``` program and start--<em>almost</em>--from scratch.  But it will be "Oh, so worth it!"  These instructions have been updated accordingly. Enjoy and God bless!


## GETTING STARTED

In order to begin using this exciting new addition to the world of financial software, create a folder dedicated to your financial projects.  If you already have one, then move on the the next step.  

First, I would recommend downloading [Git](https://git-scm.com/), this is an improved command prompt/terminal, and everyone who's anyone is using this.  

The user must also download the [Python](https://www.python.org/) programming language.  As the download proceeds, check that Python is added to your PATH variables.  This should be done by default but one can never be too sure.  

Next up is [Anaconda](https://anaconda.org/) -- this will be used to manage the Python packages most helpful in utilizing the data you'll be exploring. In the same way, check on the status of the PATH variables, and make sure that this is located in the same area as your folder for financial projects. Once those two downloads are done, you're ready to begin setting up your environment.

## Downloading the Project

If you're familiar with Git, ignore this step:

For those of you who have never cloned a Github repository, this will possibly be the most useful thing you learn to do on this page.  First, open up Git which should be done downloading by now.  You're going to need to navigate to the folder where you want to house your finance-related projects, and in order to do that, you'll have to use the ```cd``` or 'change directory' command.  Simply type that command followed by the folder you want to navigate to on the Git prompt.  For instance, if you wanted to navigate to the "Cheese" folder, you would type ```cd cheese```.  In order to use the command though, the folder has to be directly above or below the disired location.  So if "Cheese" is inside the current folder it would work, but not if "Cheese" is within a different folder, or more than one folder away.  You can use ```cd ..``` to move back a level if you go into the wrong directory.  You'll get the hang of it quickly.

Once you're in the correct location, you simply clone the project.  Run the command ```git clone https://github.com/kotamichael/Redeemer.git``` and viola! You now have the project files on your machine.  Open up your file GUI and make sure they're there.  If so, move on to the next step! 

## Setting Up the Environment 

The environment is contained ```environment.yml``` file.  To create the environment, open the "Anaconda Prompt" which came with Anaconda as an administrator.  Navigate to the folder you cloned from Github using the ```cd [folder]``` command, then run the following command: ```conda env create -f environment.yml```.  Then watch--feeling like you just coded the matrix--as all the packages are installed and go flying by on the prompt.  Even after all this, the user must still install the Alpha Vantage API Python Wrapper developed by [RomelTorres](https://github.com/RomelTorres/alpha_vantage), but running the command ```pip install alpha_vantage```.

### Robinhood

In order to run even Ruth, the user must be set up to work with the Robinhood API.  The first step in that is [creating an account](https://www.robinhood.com/).  Once that's done, the user must get the wrapper to interact with the API from [Jamonek's repository](https://github.com/Jamonek/Robinhood).  In Git, navigate to inside the "Redeemer" folder path, and then clone the repository.  Click on [this link](https://github.com/Jamonek/Robinhood) and then click on the green button to the right which says "Clone or download v", then copy the address which the dropdown menu supplies.

![alt text](https://i.imgur.com/Daeqb4b.png)

Then go back to Git and type ```git clone https://github.com/Jamonek/Robinhood.git"``` assuming his address is the same when the user attempts this.  

Go back to your Anaconda Prompt.  Navigate into the newly installed ```\Robinhood\``` folder and then run ```pip install .```.  This will setup the Robinhood API wrapper for you.  Use ```cd ..``` to go back to the ```\Redeemer\``` folder and you should be good to go.

### Credentials

If you already had an account with Robinhood, or skipped setting one up, now's the time.  In order to Ruth to run, Boaz has to have your credentials.  Open up ```boaz.py``` in your favorite IDE or code editor (definitely Sublime Text 3).  Locate the easy-to-find area to enter your credentials marked "YOUR_USERNAME" and "YOUR_PASSWORD" respectively:

![alt text](https://i.imgur.com/t1bwVyY.png)

Replace the placeholders "YOUR_USERNAME" and "YOUR_PASSWORD" with... what? You guessed it, your username and password.  And, that's it. That's really all there is to setting up Boaz... for now! See ["Future Improvements"](https://github.com/kotamichael/Redeemer#future-improvements)

## Ruth

Ruth is a function within the Redeemer program.  That's a fancy word for a piece of the program that does some specified work.  ```ruthGlean()``` is the function that iterates through the list of stocks you create and gleans the information from the Robinhood API.  By default, Ruth gleans every stock on 1 second increments, simply because I'm impatient when developing--she waits the given wait period before starting and to sit and watch her wait over and over again would be a colassal misuse of time.

It's easy to change the increments, simply look [here](https://github.com/kotamichael/Redeemer#interacting-with-and-editing-the-program).

![alt text](https://i.imgur.com/9L7XQsH.png)

Once the wait has expired, Ruth executes the request for data, and receives it back in JSON format.  This is then transcribed into files named after the specified equity.  For the Microsoft (MSFT) symbol, the file would be named 'MSFT.json'.  Ruth will run uniterupted at the specified wait period until you terminate the program: ```ctrl + c```.  This JSON file is indexed according to the "updated_at" key within the data.  This means the user can call out time intervals by referencing this timestamp: ```data["2018-03-30 09:30:00"]```.  This makes the data easy to pull into the Pandas dataframe in order to play around with it. In order to call for the bid price at 12:30 on April 4 for instance, the call would look like this:

```python
import json

with open('MSFT.json') as rFile:
		data = json.load(rFile)

print data["2018-04-04 12:30:00"]["bid_price"]
```

with the resulting output being similiar to this:

```
"1028.0000"
```

![alt text](https://i.imgur.com/OjRJXcS.png)
<sup>The JSON output. This was snapped on Good Friday; since the markets were closed, nothing was changing.</sup>

## Boaz

Because Ruth gleans directly from the field of the Robinhood API, there's no need to construct a complicated interaction of multiple APIs. Everything can be done directly on Robinhood.  Boaz buys from the same place the Ruth gleans. Boaz doesn't yet have his own function on the redeemer platform, but check the ```boaz_example_scripts.py``` for some examples of how Boaz has the capability to execute buys and sells once Naomi is instituted. 

See ["Future Improvements"](https://github.com/kotamichael/Redeemer#future-improvements) for more information on what's to come.

## Running the Program

To run the program from the "Anaconda Prompt" all you have to do is type ```python [file_name].py``` where "[file_name].py" is replaced with the desired program.  This has to be done from inside the ```Redeemer``` folder on the prompt. So to run our main script go to the Anaconda Prompt and type:

```linux
python redeemer.py
```

This will run the program on the command line.

## Interacting with and Editing the Program

In order to customize these files, you're going to need a text editor (used for writing code).  I would recommend [Sublime Text 3](https://www.sublimetext.com/3) for anyone on a Windows computer.  Once it's installed, simply open Sublime Text and within the program  open any of the ```Redeemer``` files.  For more information about text editors and IDEs simply run a google search.

In order to edit which stocks Ruth gleans, you simply update the ```fieldsToGlean``` list at the top of the file:

![alt text](https://i.imgur.com/OszCqLu.png)

In order to change the interval at which Ruth gleans, go to the bottom of the file and change the number and time unit to whatever you desire.

![alt text](https://i.imgur.com/IwtIZol.png)

## Future Improvements

As of now, all the program does is glean the data.  This in and of itself is only good for seeing prices and creating charts.  But you have yet to truly Redeem all information that is publicly available...

#### Naomi

Over the next few months watch for the last installment, Naomi, which will implement machine learning and vizualization techniques to make predictions and recommendations for buys and sells. Just as Naomi provided Ruth with sagacious wisdom when she needed it most, so too this program will have your best interest in mind... when it comes to equities, that is.

#### Boaz

Boaz is the third installment in this trilogy.  He is the source of action in this story.  Based on the information gathered by Ruth, Boaz will buy and sell according to Naomi's recommendations.  We have plans for this, but it is forthcoming.  

Continue to check back on the progress and feel free to leave notes of encouragement as you feel appropriate.

## Happy Trails

You've officially embarked on your path to glean what the others have left behind.  If you're successful, maybe one of the owners of the field may even take notice and offer to redeem you.... Ok, maybe I've overextended the metaphor... Ok, maybe it was overextended before I began.  In conclusion, I digress.

![alt text](https://i.imgur.com/l72HZse.jpg)