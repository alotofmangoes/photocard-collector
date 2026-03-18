# photocard-collector
A draft of a game where you collect photocards!

# Photocard Collector

#### Website Link: https://photocard-collector.netlify.app/

## Statement

I started collecting K-pop photocards for my favourite groups in 2023 and slowed down in 2024 due to wanting to save money. Recently I got into playing card collecting games on Roblox which inspired me to make my own. Since I needed to learn HTML, CSS, and JavaScript for other purposes, I created this game to help familiarize myself with the basics. In six days I was able to learn how to make a basic and quick game that simulates collecting and upgrading cards.

Authour's note: I am a beginner and this code and webpage is definitely not the best but I have hopes on someday improving this as mentioned in the future directions further down!


### The Process

Step 1: A folder was created and opened in Visual Studio Code to then make a file called "index" in HTML. The Microsoft Live Preview extension was installed in VS Code to keep track of the changes being made as new code was added. An assets folder was also created within the main folder so all the images could be easily copied and pasted where they need to be in HTML or JavaScript file.

Step 2: At the top of the HTML file the following lines of code were written including a relative link to the CSS stylesheet where the styling rules will go:

    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="utf-8">
            <link rel="stylesheet" href="styles.css">
            <title>TXT Card Collector</title>

        </head>

Step 3: After the <head> tags the <body> tag was written to start creating the body of the document.

    <body>
            <h3>TXT Card Collector</h3>
            <h5>Try to collect all the cards and get them to max level! </h5>

The properties and values used for the headers are:

    h5 {
        margin-top: 12px;
        padding: 7px;
        border-bottom: 0.5px solid black;
        font-family: sans-serif;
    }

    h5, h3 {
        text-align: center;
        font-family: 'Franklin Gothic Medium', sans-serif;
        letter-spacing: 1px;
    }

Step 4: Two div tags were created representing the main section of the document and the content section within the main.

    <div class="main">
                <div class="content">

The div element with the class attribute of “main” has the following properties and values:

    .main {
        position: relative;
        justify-content: center;
    }

Step 5: Inside of the <div> with the class “content” there were two containers created. Each container consisted of the same structure having three rows and three columns with a <div> section for each row and a <div> section for each card in that row. An example of these lines of HTML code looks like this:

    <div class ="col1">
        <div class="card">
            <img id="s1" src="assets/soobin-bh-qm.png">
            <div class="level"><p id="sl1"></p></div>
        </div>
        <div class="card">
            <img id="s2" src="assets/soobin-bh-qm.png">
            <div class="level"><p id="sl2"></p></div>
        </div>
        <div class="card">
            <img id="s3" src="assets/soobin-bh-qm.png">
            <div class="level"><p id="sl3"></p></div>
        </div>   
    </div>

These lines were repeated two more times only changing the <image> and <p> tag ids as well as the photo used as a different member for each column. 

Descriptions of class and id names for context/clarity:

- class = “col1”: Col is being used for short form of column and the number represents which one.
- class = “card”: All individual cards were placed into this class.
- id = ”s1”: Each member had their card slots labeled. Since this is for the member Soobin this was Soobin1, the one representing the first Soobin card in the collection.
- class = “level”: This section is for CSS managing the placement of the number that shows the level of the card
id = “sl1”: As mentioned prior the letter corresponds to the member (Soobin), l is for level and the number corresponds with the card. This <p> tag is for Soobin’s level on the first Soobin card.

The properties and their values for the containers and cards as well as the <img> element are written in the CSS file as follows:

    .container {
        display: flex;
        position: relative;
        bottom: 200px;
        right: 100px;
        padding: 300px;
    }

    .container2 {
        display: flex;
        position: absolute;
        bottom: 490px;
        left: 694px;
        padding: 10px;
    }

    .card {
        position: relative;
    }

    img {
        width: 150px;
        height: 235px;
        padding: 0px;
        border: 4px solid rgb(255, 255, 255);
        border-radius: 15px;
        z-index: 2;
    }

Step 6: For the card level to appear in the top right corner of the card this was the properties and values corresponding to the <p> element in the class “level”:

    .level p {
        position: absolute;
        top: 8px;
        right: 16px;
        color: rgb(255, 255, 255);
        font-family: Arial, sans-serif;
        font-size: 20px;
    }

Step 7: There are a total of three members used in this project and as mentioned earlier, each member had their own column. The images used were placeholders letting the player know which member was going in which spot and what the odds of getting them were.

<img width="483" height="256" alt="Image" src="https://github.com/user-attachments/assets/cc97cabb-a024-4464-8622-ae67916b5d65" />

The properties and values for the layout of the cards and images were the following:

    .col1, .col2, .col3, .col4, .col5, .col6 {
        display: grid;
        grid-template-rows: repeat(4);
        padding: 2px;
    }


Step 8: After closing the <div> start tags for the content and the second container, another <div> tag was created to represent the section for where the money counter and buttons to buy cards would go. An example of how the money counter and button visuals were created:

    <div>
        <p id="money"> Money : 200</p>
        <!--buttons-->
        <div id="foeb">
            <button class="button-design" id="fight-or-escape">Fight or Escape (10,000)</button>
        </div>
    </div>
              
For the money counter, inside the <p> element the starting money total is written to show the player how much they get to spend to get their first card. Each button has its own id attribute based on what album it corresponds to. The text between the <button> start and end tags is an acronym of the album title with a “b” added to the end for “button”. For example, the Fight or Escape button is “foeb”. The amount of money to be deducted from the player’s money is written in the circle brackets beside the album name.

Step 9: The properties and values for the design of the buttons and money counter:

    .button-design {
        font-size: 17px;
        padding: 4.5px;
        font-family: 'Franklin Gothic', sans-serif;
        border-radius: 8px;
    }

    #blue-hour {
        position: fixed;
        top: 136px;
        margin: auto;
        background-color: rgb(136, 228, 215);
        border: 2px groove rgb(60, 128, 167);
    }

This is one of the six buttons serving as an example of their design. The others have different top, background-color, and border (specifically the colour) values.

    #money {
        position: fixed;
        top: 92px;
        margin-top: 3px;
        border: 2px solid ;
        border-radius: 8px;
        padding: 5px;
        background-color: white;
        font-size: 19px;
        font-family: 'Franklin Gothic', sans-serif;
    }

The buttons and money counter are in a fixed position allowing the player to access/see them even when they scroll down to the bottom cards.

Step 10: The use of the interactive pseudo-class :hover were used for the buttons:

    #blue-hour:hover, #freeze:hover, #freefall:hover {
        background-color: rgb(33, 164, 245);
    }

    #fight-or-escape:hover, #thursdays-child:hover {
        background-color: rgb(219, 113, 132);
    }

    #temptation:hover {
        background-color: rgb(44, 161, 54);
    }

Step 11: After putting the </div> end tag the <script> tag was placed to insert the JavaScript file that was going to be used. After this the <body> and <html> tags were closed completing the HTML document.

Step 12: Three different types of variables in JavaScript were created. One for the money, another for the cards and the third variable for the buttons. An example of variables are as follows: 

    var money = 200;
    var c1 = document.getElementById("s1")
    var buybh = document.getElementById("blue-hour")

Description for each variable:

- var money: The starting value of money is 200 allowing the player to buy cards at the start of the game.
- var c1: This is related to the placeholder card in the HTML file “s1”. This marks the first card which is the first Soobin card (s1) as discussed earlier. All 18 cards have their own variable using one of the 6 id attributes of each member.
- var buybh: Each of the 6 buttons have a variable with their acronym at the end of “buy”. For example this one is for the blue hour button because of the “bh”.

Step 13: An inventory for the player’s cards was created using this line of code in order to keep track of how many they have of each:

    const inventory = {
        cu1: 0, cu2: 0, cu3: 0, cu4: 0, cu5: 0, cu6: 0, cu7: 0, cu8: 0, cu9: 0,
        cu10: 0, cu11: 0, cu12: 0, cu13: 0, cu14: 0, cu15: 0, cu16: 0, cu17: 0, cu18: 0
    };

Step 14: For each button a function had to be created so that when the button was pressed the player’s money was deducted accordingly and they received a card matching that album. An example of the function is:

    var boughtbh  = function () {
        if (money >= 100) {
        money -= 100
        getcardbh()
        document.getElementById("money").innerHTML = ("Money : " + money);
        }
    }

An if statement was used so that the button would only work if the player’s money was greater than or equal to 100. This prevented the button being pressed and deducted for the money when the player was below 100 putting them into the negatives. The variable for getcardbh() is accessed which allows for a certain card to be pulled. This function will be explained further down. Changing the innerHTML after the card was bought allowed for the money visual to update the new total.

Step 15: After receiving the card the player should be able to click the card to get money. This means the card itself is similar to the button except instead of decreasing the total money it increases it. Here is an example of how this was achieved: 

    var sm1  = function () {
        if (inventory.cu1 >= 145) {
            money += 25
        }
        else if (inventory.cu1 <= 9){
            money += 5
        }
        document.getElementById("money").innerHTML = ("Money : " + money)
    }

Here the variable sm1 is defined as a function to add a certain amount of money to the player’s total depending on the cards in the inventory. The leveling system will be described later but essentially every 15 cards the player reaches a new level. The card should give them more money as it upgrades. This is a shortened version of the sm1 function with the if statement representing how much money the card makes at max level and the else if being when the card is level 0.

Description of variable sm1:

- sm1 refers to Soobin money 1. Each of the three members has 1-6 of this variable so all 18 cards and different money values with their upgrades. The rarer the card the more money it makes as it upgrades making it easier to buy the next pack.

Step 16: When the button is pressed the player should get a random card therefore a function was created to generate a random number that will associate with one of the 3 cards a player can get with each button.

    function random(num) {
        return Math.floor(Math.random() * num)
    }

This function is referenced from the official JavaScript documentation here: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random 

Step 17: For the player to actually get a card a function had to be created. Each album got a variable named “getcard” and would have the acronym of the album attached to the end. For example as previously mentioned getcardbh() for blue hour. The following lines of code show how this function works:

    var getcardbh = function () {
        var shuffle = random(6)
            if (shuffle == 0 || shuffle == 1 || shuffle == 2) {
                var cu1 = document.getElementById("s1")
                cu1.src = "assets/soobin-blue-hour.jpg"
                cu1.style.border = "4px solid rgb(136, 228, 215)"
                c1.addEventListener ("click", sm1)
                inventory.cu1 += 1
                level()
            }

When accessing getcardbh() it runs another variable named shuffle. The shuffle variable is linked to random() which has the number 6 as its value. To control for the odds that each card has (Soobin having a 50% chance) then having shuffle equal to 0, 1, or 2 will allow the variable cu1 to replace the placeholder image originally in the HTML file and the photocard image of Soobin will appear. The newly received card is given a border that matches the button.
For the other members, shuffle equals 3 or 4 for Beomgyu and shuffle equals 5 for Hueningkai making that the hardest card to get and level up
An event listener is added with the event named “click” as now everytime the player clicks the card sm1() will run. Every time the card is received it 1 gets added to the property value which then correlates to the level() function.

Step 18:

    buybh.addEventListener ("click", boughtbh)

This line of code was repeated for all 6 of the buttons using the variables created for buying and the event function that happens after the card is bought (money deduction). This allowed for the buttons to become fully functional in being clicked, receiving cards and losing money.

Step 19: After the player received 10 cards to get to level one, every 15 cards after would unlock the next level. Whenever a new level was achieved (based on its value in the card inventory) the text in the <p> element with the attribute “sl1” in the HTML was changed. This is an example of the code for the max level and the first level:

    var level = function () {
        // card number 1
        if (inventory.cu1 >= 145) {
            document.getElementById("sl1").textContent = "MAX";
        }
        else if (inventory.cu1 >= 10) {
            document.getElementById("sl1").textContent = "1"
        }

This function for levels 1- 10(max) was repeated for all 18 cards.

# Future Directions 

Since this is the first time I have created something like this and used HTML, CSS and JavaScript I know the code is not perfect and there are ways to clean it up. Not only that but there are many ideas I could not execute at the time of making this game due to lack of knowledge but hope to refine it more in the future.

### Leveling System
Being able to see how much you need until the next level creates more of an incentive to keep going.

### Autoincrement Money
Allowing the money to accumulate on its own as having to click especially for larger totals can get tiring for the player.
The cards themselves can increment in money and the player can click the card when they want to collect or the player’s money automatically increments and the player only needs to focus on buying upgrades.

### Card Grading
Many card collectors can send their cards to get graded, increasing the value. It would be nice to have this in the game where players can grade their cards making them multiply in value depending on the grade.
In other card collecting games these can be letter grades or more closely imitate PSA grading using numbers.
### Card Upgrades
Being able to purchase upgrades that give your cards are multipliers to how much money your card makes.
For example if you get a gold upgrade for your card it will give the card a gold border and give you 3 times the amount of money that card is making.
