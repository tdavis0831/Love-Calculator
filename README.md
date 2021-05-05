""""This code was made to check the love capatability by taking the input of 2 people's name and then seeing how many times the letters from TRUE LOVE appear in the name that was input.  Depending on the score of the combined totals, the program will produce the score and compatability rating """



#set var to store the names that are entered
person1=(input("Type your name:"))
person2=(input("Type your name: "))

#var set to store the combined names in order to convert the letter to lower case so they can be counted without running an error. Using Count function I am able to run through each individual letter to see how many times it appears in the varaible lower_names. I then set another variable which adds the total from each varaible from the word true
combined_names=person1+person2
lower_names= combined_names.lower()
t = lower_names.count("t")
r=lower_names.count("r")
u= lower_names.count("u")
e=lower_names.count("e")

first_digit=t + r + u + e
#this is repeated for the second word, love
l=lower_names.count("l")
o=lower_names.count("o")
v=lower_names.count("v")
e=lower_names.count("e")

second_digit= l+o+v+e
#I then set the score variable to store the addition value of the first digit and the second digit. I used .format to input the int into the string
score=int(str(first_digit) + str(second_digit))
print("Your compatability score is {}".format(score))

if (score<10) or (score>90):
  print("This is your one true love <3")
elif (score>=40) and (score<=50):
  print("It could go either way")
else:
  print("RUN AWAY AS FAR AS YOU CAN")
