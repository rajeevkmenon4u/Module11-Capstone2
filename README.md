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
![image](https://github.com/user-attachments/assets/fdd95c8e-251a-4241-9f73-de2d27e2bd64)

  1. Greater than year 1980 - Ratio of cars
      1. gas cars  83.96% and  diesel cars are at 6.85% hybrid  1.27% &  electric 0.42%
      2. Price Range
      3. Diesel cars 33,766.26 , electric  25,698.23 , gas 16,951.67 , hybrid 15,539.89 other 27997.98
  2. Before year 1980
      1. gas 96.59% and diesel 1.12% , electric 0.13%
      2. Price Range
      3. diesel 11,177.46,  electric  6731.72 , gas  18,298.07 other - 18,628.20
## where there Electic cars before 1980 ??? - Anamoly  
### Hypothesis 
 So overall gas cars less expensive after year 1980 , where as disel cars were less expensive before 1980
 
# 3. Analysis-Cylinders & Price
![image](https://github.com/user-attachments/assets/d5c5b065-dbfb-48e1-8c57-d54a00ab4d32)

  1. Greater than year 1980 
      1. 41% contains missing cylinders data & 6 cylinders  22.58% -  4 cylinders    18.43% -  8 cylinders     16.31%
      2. Price Range
      3. 10 cylinders    22476.702882 , 12 cylinders    57,354.994819 ,  3 cylinders   13074.536332 4 cylinders     11060.367327
  2. Before year 1980
      1. 8 cylinders     46.389678 %  - 32.776989% contains missing ,  & 6 cylinders  10.58% -  4 cylinders    9.2%
      2. Price Range
      3. 10 cylinders    20,000.000000 , 12 cylinders    15,500.000000 ,  3 cylinders    7541.666667  4 cylinders  - 11,979.129321

### Hypothesis 
 So overall price gets reduces with less cylinders
 
# 4. Analysis-Condition & Price
![image](https://github.com/user-attachments/assets/09fef1ad-ce22-4213-9e92-18394fd472ef)

 1. Greater than year 1980 
      1. Missing    38.69%  good         31.04% excellent    22.97%
      2. Price Range
      3. Missing      20005.54,  excellent    15,261.95, fair          3878.65,  good         21,157.20,  like new     18997.15,   new          26928.86
  2. Before year 1980
      1. Missing      30.10%  good         29.46%  excellent    25.48%
      2. Price Range
      3. Missing      18696.88 , excellent    25,680.73 , fair          5773.23, good         12,898.81,   like new     33225.74 , new          35211.00
### Hypothesis 
  More than 30 % data are missing condition data
  Good cars are expensive than Excellent condition cars after 1980 ??? 
  Excellent cars are expensive than good condition cars before 1980 - Make sense
    
# 5. Analysis-Drive & Price
![image](https://github.com/user-attachments/assets/1f917f5a-dc88-4ebf-be2d-f1daa3fe9741)

1. Greater than year 1980 
      1. 4wd        30.965164  Missing    30.021753 fwd        25.602994  rwd        13.410089
      2. Price Range
      3. 4wd        23570.34 Missing    18640.59 fwd        12580.87 rwd        21207.17
  2. Before year 1980
      1. rwd        51.006155 Missing    39.287405 4wd         7.054924 fwd         2.651515
      2. Price Range
      3. 4wd        14675.04 Missing    19323.90 fwd        15816.58 rwd        18015.10
### Hypothesis 
  More than 30 % data are missing drive data
  4wd are expensive when compared to fwd & rwd.


# Remove missing data from drive , condition and other columns and perform one hot encoding for ( drive & Gas)
## Data Greater than 1980
  ![image](https://github.com/user-attachments/assets/e71e86fe-db98-4721-8ac7-6c87a4c62729)
## Data Less than 1980
![image](https://github.com/user-attachments/assets/434ba04c-57ee-4881-83c0-dbb5bddfe8e4)

# Data Modelling
## Correlation for Data Grreater than 1980  
  ![image](https://github.com/user-attachments/assets/7f810c86-038f-46d3-ae32-8556df285559)
# Heat Map - Greater than year 1980 
![image](https://github.com/user-attachments/assets/1d46ded2-79ee-4dad-99cc-e8bdb18c94ca)
# Correlation - Greater than year 1980 
![image](https://github.com/user-attachments/assets/e2aa55fd-e4c0-4c72-9b45-e0e64f82b00d)


## Correlation for Data Less than 1980  
 ![image](https://github.com/user-attachments/assets/8ac6351f-dbc3-4834-98e4-5bbad54bdc40)
# Heat Map - Less than year 1980 
![image](https://github.com/user-attachments/assets/b8081515-3e47-474a-809c-c33b77584374)
# Correlation - Less than year 1980 
![image](https://github.com/user-attachments/assets/3aa90ff4-29d7-4124-a8be-618bbd68d4e2)

### Hypothesis 
  1. Based on the above it indicates that
  2. Drive_rwd & drive_4wd, Fuel_other & Fuel_other has positive impact on prices for year > 1980
  3. Drive_fwd , fuel_gas, odometer and fuel_hybrid has nagative impact on price for year > 1980
  4. Drive_rwd & fuel_gas has positive impact on prices for year < 1980
  5. Drive_fwd , fuel_gas,fuel_disel, drive_4wd , odometer , fuel_other and fuel_hybrid has nagative impact on price for year < 1980
  
  
# Scaling & Applying models( Linear, Ridge & Lasso)
# Analysis
 ![image](https://github.com/user-attachments/assets/71c36cbd-a766-444a-a2d1-0b6f4421b769)
 ![image](https://github.com/user-attachments/assets/9de2448b-b688-4442-8d03-496ce1d845d5)
 ![image](https://github.com/user-attachments/assets/c56360a7-eda6-4dd8-8bb1-e13cba1bd43e)

## Prediction againt Traindata 
![image](https://github.com/user-attachments/assets/652a23db-b313-40df-9136-ebb35b1eec87)
![image](https://github.com/user-attachments/assets/43f9bc16-477a-4a20-a631-033f25761541)
### Hypothesis 
  1. Not a good prediction

## Prediction againt Testdata 
![image](https://github.com/user-attachments/assets/5695c173-05a9-4d7d-9fee-4eef846ffffc)

### Hypothesis 
  1. Not a good prediction

## Evaluation 
## RMSE Comparison
Price Prediction with (Fuel & Drive categorical values)  = 19,037.70 K

![image](https://github.com/user-attachments/assets/ab31d3e8-6062-40f9-912b-583989815e79)
# with Fuel & Drive ( Train & Test Prediction Performance)
Train 13219.052453	Test :- 13551.160857
Mean :- #price = 19,037.70 -- Off by 5.8K

## Coefficients Comparison
  ![image](https://github.com/user-attachments/assets/2381e286-3771-435d-b5b5-d02811f1b250)
### Hypothesis 
  1. Fuel_disel, drive_4wd, fuel_other, drive_rwd all has positive impact on price for all the 3 models 
  2. Fuel hybrid, Fuel_gas, drive_fwd and odometer has negative impact on price for all the 3 models 
  3. only for fuel_ electic ) both liner & ridge has positive impact , Lasso has negaive impact.
![image](https://github.com/user-attachments/assets/75d9f7a1-cda6-4b54-a5fb-8a27b3004993)
  
     
## Results / Observation
   1. In this case all 3 models worked almost similar. 
   2. The price prediction was not that good and not close to the actual price  
   3. Not a good model as the error in prediction was 5K for each of the models
      

