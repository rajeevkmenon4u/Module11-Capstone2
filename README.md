# Module11-Capstone2(What drives the price of a car?)
This is the Practical Project Part of AI &amp; ML Course to create a Model
#### Link to the Project ([https://github.com/rajeevkmenon4u/Module5-Capstone1/tree/main](https://github.com/rajeevkmenon4u/Module11-Capstone2))
## Business Understanding
  The Problem: What type of used cars are in demand in a Car Dealership.\
  The Current State: Currently have all type of cars are stocked and purchased by the dealer.\
  The Impact: This can helps the dealership to understand what value the buyer sees in the used car.\
  The Desired Outcome: Reduce the cost of inventory and help customer of what they want.\
  The Benefit: Improved customer satisfaction and reduced operational costs for the dealer.
## Data Analysis & Cleaning 
   ###### Analysing the data and identfying the anamolies/ missing data 
     Below are the list of columns that has maximum missing data
     #Percentage of data missing in each column
     + size	---:71.77%
     + cylinders---:41.62%
     + condition---:40.79%
     + VIN---:37.73%
     + drive---:30.59%
     + paint_color:---30.50%
     + type:---21.75%
   ###### Graphical Representation
   ![image](https://github.com/user-attachments/assets/4824df38-1a46-4748-966e-c469ba42fb43)
    
   #### High level anaylis of price of cars
       Pricing Range check of cars from the dataset provided
       
       Pricing ranges of car from
            Avg :- 75K which looks large ????
       25% are in the 6K price range, 50% in the Range of 13K, 26K in the range of 75%
       Avg doesnt loook correct because something is high??
       Max is 3.7 million need to see what the car is ???
![image](https://github.com/user-attachments/assets/945cf5cd-293d-4d25-bd28-6e6d48d16358)

###### Graphical Representation
![image](https://github.com/user-attachments/assets/dbeb0ae7-2bcb-4d4c-85ea-01e02028dbb1)
### Hypothesis
There are few cars who price are 3 million and above
There are few cars who price are between 1 million and above
Majority are in the less then 50K

## Price Detail Analysis  
# 1. What proportion of cars are less than 50,000?
###### Analysis-Findings
        
      1:---413,839 cars data are less than 50k	
      2:---12,344 cars data are of 50k and less than 100K
      3:-- 620 cars data are of 100 K and above and less than 300 K
      4:-- 77 cars data are of 300K and above
      5:-- 60 cars data are of 1Million and above
![image](https://github.com/user-attachments/assets/a545f23a-6da4-4639-9809-4bd7aa915aac)
     
![image](https://github.com/user-attachments/assets/9599c775-cece-4bd8-aaa4-ea323e82069e)

![image](https://github.com/user-attachments/assets/c07a075d-4f9b-4a66-a17c-453773815f12)
      
### Hypothesis      
    Data of not much use 1. model 2, VIN 3. size
    Data useful are   1. fuel ( gas other disel),  transmission ( Auto, manual, other ) 2. title_status ( clean , salvage) 3. drive (rwd, 4wd, fwd) 4. condition (good excellent . salvage) 5. cylinders 6, manufacturer
    Data useful ok    1. color 2. type ( truck , pick , SUV)
    ### Based on general knowledge
    What factors depends on the car value ( Year, transmission, Fuel, odometer, condition , cylinders, title ) will decide the value of the car
    These factors will impact little bit paint, drive, type,  and others
    
# Data Preparation
###### Removing 0 & NUll Values & cars Price > 1 M 
 Total = 426,880
 Total after removing price 0 = 393,985
 32,895 rows of 0 removed
 Total records of 393,932 remaining After removing price more then 1 M
 
![image](https://github.com/user-attachments/assets/a04760cd-50c8-4a02-82e8-5ab5cd8c6a4d)

### Analysis Raw data & after removing 0 & NULL Values & cars Price > 1 M  

## Pricing ranges of car from Earlier 
            Avg :- 75K which looks large ????
       25% are in the 6K price range, 50% in the Range of 13K, 26K in the range of 75%
       Avg doesnt loook correct because something is high??
       Max is 3.7 million need to see what the car is ???

## Pricing ranges of car after Removing 0 & NUll Values & cars Price > 1 M
          Avg :- 18.9K which has come down
       25% are in the 7K price range, 50% in the Range of 15K, 27K in the range of 75%
       Avg doesnt loook correct because something is high??
       Max is 1 million need to see what the car is ???
![image](https://github.com/user-attachments/assets/28f4477a-6a9d-463a-84db-39e6c4524ee0)
       
## What more data can be removed  
  1. Three Freatures ( Cylinders, Drive & Condition Missing data)
![image](https://github.com/user-attachments/assets/2ccfe4ec-d65c-480e-a5f5-4c6ce33afd06)
  2. Null Value comparison before cleaning data
![image](https://github.com/user-attachments/assets/eb67aa9c-68b1-42c2-a7d8-6c172a0cfd80)

3. Null Value comparison After cleaning data
    
![image](https://github.com/user-attachments/assets/80396674-e92d-488c-bfc7-9fd5964f6e46)

## Pricing ranges of car from Earlier 
            Avg :- 75K which looks large ????
       25% are in the 6K price range, 50% in the Range of 13K, 26K in the range of 75%
       Avg doesnt loook correct because something is high??
       Max is 3.7 million need to see what the car is ???

## Pricing ranges of car after Removing 0 & NUll Values & cars Price > 1 M
          Avg :- 18.9K which has come down
       25% are in the 7K price range, 50% in the Range of 15K, 27K in the range of 75%
       Avg doesnt loook correct because something is high??
       Max is 1 million need to see what the car is ???
## Fairly the same after removing 0 Odometer entries
![image](https://github.com/user-attachments/assets/3381da93-d4f9-4262-9782-a48808556eb6)

## Car Price Distribution & Spread
![image](https://github.com/user-attachments/assets/c3736afa-c1c9-4e6b-ac1f-a574f010431e)

## Car Manufacturer Distribution
![image](https://github.com/user-attachments/assets/0cd76e13-ec39-441b-9c3a-647e50fadc59)
     
# Price & 6 features (year , odometer , fuel,  cylinders , condition , drive, transmission , title_status) analysis
## 1. Analysis-Findings for Year
  Of the overall cars of 380,280 
  Count of cars > 1980 = 372,114 
  Count of cars < 1980 = 8431
     
###### Graphical Representation
![image](https://github.com/user-attachments/assets/2bc972a8-d10f-4539-b605-bab93a845554)

![image](https://github.com/user-attachments/assets/50ba8824-90ea-4d07-993e-bd743ed8edc9)

## 2. Analysis-Fuel & Price 

  1. Top 3 acceptance of coupons cateogry ( All temp 80)
      1. Coffee house
      2. Restaurant(<20)
      3. Carry out & Take away "Carry out & Takeaway"
  2. Top 3 Rejection of coupons cateogry
      1. Coffee house - Temp 80
      2. Restaurant(<20)  - Temp 55
      3. Bar - Temp 55
     
# 4. Investigating the Bar Coupons
###### Analysis-Findings

|  Y         | coupon        | Count  |	
| ---------- |:-------------:| ------:|
| 0 |	Coffee House |2001|
|   |	 Bar	|	1190
|   |	Restaurant(20-50) |		834
|  |	Restaurant(<20) |		816
|   |	Carry out & Take away	 |	633
| 1	|	Coffee House|		1995
|   |	 Restaurant(<20)	 |	1970
|   |	Carry out & Take away	 |	1760
|   |	 Bar |		827
|   |	 Restaurant(20-50) |		658

0 Bar	9.38 - Rejection
1 Bar 6.52 - Acceptance
### Hypothesis 
 So overall 6 % accepted the Bar coupons & 9% rejected Bar coupons
 
# 5. Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.
###### Analysis-Findings
| coupon     | Bar        | Count  |	 Mean  |
| ---------- |:----------:| ------:| ------:|
| Bar |	1~3 | 397| 0.647355|
| Bar |	4~8 | 150| 0.780000|
| Bar |	gt8	| 49| 0.734694|
| Bar |	less1 | 570| 0.443860|
| Bar |	never | 830| 0.187952|
###### Graphical Representation
![image](https://github.com/user-attachments/assets/edbe4c56-465d-4c44-b347-6a93af77ebd4)

### Hypothesis 
  The acceptance rate is more when compared to passengers who went to Bar less than 3 times or lesser. it is around 64%.
  The acceptance rate is 78% to the passengers who when 4-8 times but the count is 150 which is less than half to the count of passengers who went to bar 1~3 times
  The acceptance rate is 73% when they went more than 8 times but the count is very less on 50.
# 5. Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others. Is there a difference?
###### Analysis-Findings
![image](https://github.com/user-attachments/assets/9bca9750-d132-4253-b32c-2a35c451ff87)

###### Graphical Representation
![image](https://github.com/user-attachments/assets/af5694bf-b664-41a3-9e0c-1a942b0bca40)
![image](https://github.com/user-attachments/assets/dfa47b38-3f74-4f2e-8bd3-5e151b0c17c0)

### Hypothesis 
  1. Age 50 PLus has maximum count of 1050 and 45% acceptance when compared to 21 years age group of count 849 and 55%
  2. People of the Age of 21 went to Bar 1`3 more times when compared to any other age category
  3. Age of 21 people went to BAR "less 1 " compared to any other group

# 6. Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.
###### Analysis-Findings
  ![image](https://github.com/user-attachments/assets/ea0cc811-98d2-461e-8b47-cc5ac0b878e0)

###### Graphical Representation
  ![image](https://github.com/user-attachments/assets/5e719207-1ce0-4025-9126-76c6216ae87b)
  ![image](https://github.com/user-attachments/assets/a802e57c-75f0-4f7e-abcf-82cae296b40c)
  ![image](https://github.com/user-attachments/assets/8a35cd8c-eaec-4817-91b0-24625154b936)

### Hypothesis 
  1. Based on the data we can see the people who are unemplyeed and who are alone goes to a Bar 1-3 times with a acceptance rate of 62%
  2. Based on the data we can see the people who are unemplyeed and who are with frimnds goes to a Bar 4-8 times with a acceptance rate of 61%
  3. Based on the data we can see the people who are unemplyeed and who are with frimnds goes to a Bar 1-3 times with a acceptance rate of 85%
  4. People who are working in managemnet also has acceptnace rate of 56% & 62% even if they are alone or with frinnds . they go 1-3 & 4-8
  5. Top 10 Jobs that go bar more often are Unemployed , Student, Computer & Mathematical, Management, Sales & Related, Office & Administrative Support	, Business & Financial	, Education&Training&Library
  6. Passengers traveling alone goes to the bar more often
  7. what we find is passenger who are Alone and with occupation "unemployed" goes to the bar (190)
  
# 6. Compare the acceptance rates between those drivers who:
     go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
     go to bars more than once a month and are under the age of 30 OR
     go to cheap restaurants more than 4 times a month and income is less than 50K.
###### Analysis-Findings
 ![image](https://github.com/user-attachments/assets/c6974b73-6165-4315-abc2-0e29eb4c234e)
###### Graphical Representation 
  ![image](https://github.com/user-attachments/assets/3a51076b-cb3d-4ebb-8ed9-80e3153416dd)
  ![image](https://github.com/user-attachments/assets/3617e7b2-b209-4b89-94ed-c75e6083188d)
  ![image](https://github.com/user-attachments/assets/0e97122f-e52b-41f1-9be0-d1d7c137d6a9)
  
### Hypothesis 
  1. passenger with friends who are aged 21 has acceptance rate of 80% but the count is vey less so it has to be ignored
  2. passenger with the age below 21 does not go to the bar that often
  3. passenger with age of 26 has good acceptance rate with all 3 (travelling with friends , partner or alone)
  4. passenger who are travelling alone go to the cheaper resturant more often and the acceptance ratio is 78% for the age of 21 and they have gone to restutnat many times.
     
## Results / Observation
   1. Passenger with age of 26 has good acceptance rate with all 3 (travelling with friends , partner or alone)
   2. passenger who are travelling alone go to the cheaper resturant for the age of 21.
   3. Passengers with the age group of 50 pLus has a 45% acceptance
      
# 7. Analysis the acceptance rate of Carryout & Takeaway
###### Analysis-Findings
![image](https://github.com/user-attachments/assets/253a6919-9dab-43b8-a87e-efc110928086)
###### Graphical Representation 
![image](https://github.com/user-attachments/assets/f7793a4e-3e57-447a-b5c0-ca0e07ae94e8)
![image](https://github.com/user-attachments/assets/4220be50-6387-43dd-86a6-c8522d1fd413)

### Hypothesis 
 1. Based on the data you see the acceptance rate for carryout with pasengers travelling alone, or frineds , partner , kids are fairly same
 2. But the count when passengers travelling with partner & kids are less than 20 when compared to passengers travelling alone , with friends
 3. Hence partner & kids can be ignored

## Results / Observation
