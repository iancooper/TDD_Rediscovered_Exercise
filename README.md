# TDD Rediscovered-Exercise

## The Exercise

### The Bowling Game Kata

Inspired by [Ron Jeffries](https://ronjeffries.com/xprog/articles/acsbowling/)

The idea is to create a console application that can calculate the [traditional score](https://en.wikipedia.org/wiki/Ten-pin_bowling#Scoring) for a Ten-Pin Bowling game.

* A game consists of ten frames.
* A frame consists of two tries to knock down ten pins.
* If the bowler knocks down less than ten pins, that is their score
* if the bowler knocks down ten pins in two tries, this is a 'spare', and their score is ten + the pins knocked down in the first try from the next frame.
* If the bowler knocks down ten pins in one try, this is a 'strike', and thier score is ten +  the pins knocked down in the next frame
* If the bowler gets a 'spare' on the last frame, they get an additional try, and their score is ten + the number of pins knocked down 
* If the bowler gets a 'strike' on the last frame, they get an additional two tries, and their score is ten + the number of pins knocked down
* On any extra tries in the last frame, knocking all the pins down does not count as a 'spare' or a 'strike'

And some scope control

* We are just calculating the final total, we don't calculate the score for intermediate frames
* We do not check for valid rolls (i.e. -1 or 11)
* We don't check the input for additional frames or rolls

For information, the score will be between 0 and 300.


## The Rules

The purpose of this kata is to experience the unit testing approach whilst using the following rules:

* We are writing Unit Tests. The Unit is a class and should be isolated from other classes.

* The prompt to write a test is a new method. If we need a method, we write a test before we write the method.

* When we discover that we need collaborators our preference is to mock them, establishing their behaviour from the client, and then implement them with their own tests. 
