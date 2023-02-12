# PHSX815_Project1
Contains my codes for the first project



This is contains my references and instructions for how to run the codes.

Firstly: the code for this project was taken from several locations: 
1. My own code and homeworks from this class
2. Prof Rogan's github, https://github.com/crogan?tab=repositories
3. The Wikipedia for "log-normal disributions", https://en.wikipedia.org/wiki/Log-normal_distribution#Properties
4. stackoverflow https://stackoverflow.com/questions/6871201/plot-two-histograms-on-single-chart-with-matplotlib
5. https://www.geeksforgeeks.org/how-to-generate-random-numbers-from-a-log-normal-distribution-in-python/

Now... How to run my code.

First you will need to put the Random.py code into a folder and specify the location in the "DataGen.py" code, so that import knows where to find it.
Next you will need to use DataGen.py to make some .txt files containing randomly generated data. EpidemAnalysis.py takes 3 files, so 3 will be sufficient. 
I added -mux and -sigx commands to the DataGen.py file, so both mux and sigx can be changed from the commandline, to achieve distributions with different parameter values. When I run it, I preform: python3 DataGen.py -Nmeas 1000 -mux 40 -sigx 8 > Data1.txt   . I do this to make 3 data files (changing the parameters).

Next you want to run EpidemAnalysis.py, which will make the histogram used in the project. This program will take the 3 data files made from DataGen.py, read them, and make 3 arrays, which are made into a histogram comparing all 3 data sets.
To run the code, here is an example: python3 EpidemAnalysis.py -input1 Data1.txt -input2 Data2.txt -input3 Data3.txt
