# Lab Report 2 (Week3) 
## By- Meiqi Lai

## Part 1: 
Code: ![image class](code.png)

## Use of the handleRequest method 

### HOMEPAGE
'        if (url.getPath().equals("/")) {
            return String.format("Hi! My name is Meiqi! Feel free to use this website I have createdas a SearchEngine!! Main features include: add and search. Familiarize yourself with the site!");
        }
The code above allows for the words to print on the website. The first if statement in the handleRequest method is true and allows for the print of the Welcome message. This url contains no specific arguments, basically implying that it is the homepage. The handleRequest method takes in a url of type URI. The url is checked by all the if statements within the method 
![image class](enter.png)



### ADDING STRINGS INTO THE ARRAYLIST

'        else if (url.getPath().equals("/add")) {
            String[] whatToAdd=url.getQuery().split("=");
            String[] parm = url.getQuery().split("=");
            if (((whatToAdd[0].equals("s")))){
                lip.add(parm[1]);
            }
            return String.format("Your" + " " + "string has been added!!!!Good Job! Use the Search Command to look for certain Strings within your added StringList or add more strings to the list!");
        } '
The code above allows for these words to be displayed on the website. The else if condition is true because the url in the search bar contains "/add". Because it contains that specific command, the code will use the split function to split the url at the equal sign. After splitting the url, the code will add the first index after the equal sign (index1) into a new string arraylist. The words that go after the equal sign will be turned into strings, when they are added to the arraystring list. The values cannot be numerical values because the code will only put Strings into the arrayStringList and not integers. 
![image class](a1.png)

### Search Query
![image class](search.png)

'        else {
            // System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/search")) {
                String[] parameterss = url.getQuery().split("=");
                    if (parameterss[0].equals("s")) {
                        for(int jj=0; jj<lip.size(); jj++){
                            if(lip.get(jj).contains(parameterss[1])){
                                lolz=lolz.concat((lip.get(jj)+ " "));
                            }
                        }
                    }
                    return String.format("Here are the results from your engine search!!!! List: "  + lolz + ",");
            }'

The code above will display that specific message on the site. What this else statement does is if the url contains "/search" it would split the url at the equal sign once again. Once it is split, it will check to see if the zero index of it contains the character string "s". If it does, it would look through the originally create array String list with the added strings and search to see if any of the strings contain the string that is in index1 of the url. If a string is found, it would return that int he statement displayed to the user. 

## None Found

![image class](none.png)
In the picture displayed above, it reveals a statement that says "404 Not Found!". This statement is printed when none of the conditional statements (if, else if, else) are met.


## Part2: