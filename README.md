# Module11-Capstone2(What drives the price of a car?)
This is the Practical Project Part of AI &amp; ML Course to create a Model
####### Link to the Project ([https://github.com/rajeevkmenon4u/Module5-Capstone1/tree/main](https://github.com/rajeevkmenon4u/Module11-Capstone2))
## Business Understanding
  #The Problem: What type of used cars are in demand in a Car Dealership.
  #The Current State: Currently have all type of cars are stocked and purchased by the dealer.
  #The Impact: This can helps the dealership to understand what value the buyer sees in the used car.
  #The Desired Outcome: Reduce the cost of inventory and help customer of what they want.
  #The Benefit: Improved customer satisfaction and reduced operational costs.Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? 
## Data Analysis
   ###### Analysing the data and identfying the anamolies/ missing data 
     Below are the list of columns that has maximum missing data
     + car---:12576
     + CoffeeHouse---:217
     + Restaurant20To50---:189
     + CarryAway---:151
     + RestaurantLessThan20:---130
     + Bar:---107
   ###### Graphical Representation
   ![image](https://github.com/user-attachments/assets/07787ac4-a175-4cd6-bf93-1e90bad8b1c1)
    
   #### Results / steps for Missing data
       Column Car has the maximum missing data as it is not used anywhere in the analysis we are ignoring the data
       Rest of the columns has the same ratio of missing data, hence it will not impact our analysis
       
       CoffeeHouse:---0.017108
       Restaurant20To50:---0.014901
       CarryAway:---0.011905
       RestaurantLessThan20:---0.010249
       Bar:---0.008436

## Various Scenarios that are considered for Analayis 
# 1. What proportion of the total observations chose to accept the coupon?
###### Analysis-Findings
        
      Y:---coupon	
      0:---0.431567
      1:---0.568433
### Hypothesis      
    Based on the analysis we can see that 57 % accepted and 43% rejected
# 2. bar plot to visualize the coupon column
###### Analysis-Findings
  
| coupon        | Y             | Count  |
| ------------- |:-------------:| -----:|
| Bar           | 0             |  1190 |
|               | 1             |   827 |
| Carry out & Take away | 1      |   1760|
|  |   0     |   633|
|  Coffee House	 | 0      |   2001|
| | 1      |   1995|
| Restaurant(20-50)	 |   0     |   834|
|  	 |1      |   658|
| Restaurant(<20) |   1     |   1970|
|  	 |0      |   816|

###### Graphical Representation
![image](https://github.com/user-attachments/assets/a8ec9a5f-24ba-4950-a884-ebc1b8680e02)
![image](https://github.com/user-attachments/assets/f95ac9a5-b627-4c6a-ab54-d624f40a4a0b)

### Hypothesis 
  1. Maximum acceptance is for "coffehouse" and "Resturant<20"
  2. 3rd place if "Carry out & Takeaway"
  3. For CoffesHouse the Rejection rate is also high 

# 3. Use a histogram to visualize the temperature column.
###### Analysis-Findings
  Of the overall coupon data of 12K, Temp 80 contibuties to 6.5k of the data, 4K data for Temp55 and remainik 2k Data to Temp30
     Temperature	
      30	0.531088
      55	0.536719
      80	0.600337

###### Graphical Representation
![image](https://github.com/user-attachments/assets/1f332d0f-d7f1-400a-846f-8ff63cae3b55)
![image](https://github.com/user-attachments/assets/571bbbdd-930a-47d8-8e3e-ae6d861d1230)
![image](https://github.com/user-attachments/assets/29ff00a9-dad1-4244-b10d-17501ed2af3d)
### Hypothesis 
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
