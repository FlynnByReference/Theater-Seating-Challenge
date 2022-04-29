# Theater-Seating-Challenge
An algorithm that, given an input file of seat reservations, automatically assigns seats to each reservation based on customer satisfaction and outputs the results to a new file

### Requirements to run
Python 3

### Process
The program assumes ther is an input file simply named "input.txt" formatted as such:
```
R001 2
R002 4
R003 4
R004 3
```
Where "R###" indicates a reservation number and the number after indicates how many seats are being reserved.

**The input file must be in the same folder as Main.py for the program to run properly, otherwise it will result in an error.** 

The program will read the input file and determine line by line which seats to reserve for the customer. 

To account for customer satisfaction on a first come, first serve basis, the program will assign the most preferable available seating to each customer. It does this by determining which rows are most desirable and checking availablity in each with a preference of seating a party closest to the middle. Since no one likes sitting in the very front of the movie theatre, the algorithm will only check for availability in the first 3 aisles if all other aisles are not available for the given party. 

After the algorithm has chosen seats for a party, the program will create an output file called "output.txt" if one does not exist already and write to the file the reservation number and the seats assigned in the format:
```
R001 G10,G11
R002 H9,H10,H11,H12
R003 F9,F10,F11,F12
R004 I9,I10,I11
```
### How to run
In the command line, navigate to the folder containing "input.txt" and "Main.py" and use the following command:
```
python3 Main.py
```
