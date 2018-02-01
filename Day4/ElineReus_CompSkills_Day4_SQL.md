## Instruction document on ElineReus_CompSkills_Day4_SQL.md

#### Creating the database from original files:
1. Data was changed into csv files using excel. 
2. The data tables where copied (BirdFuncDat and MamFuncDat). 
3. In the copied tables (BirdFuncCleaned and MamFuncCleaned) unnecessary data was removed. The data for diet, foraging and bodymass were left for the bird data. The data for diet, foraging, day/night activity and bodymass were left for the bird data. Also all '-' are replaced by '_' in the files. 
4. Both the initial and the clean data was loaded into SQLite, the right data types were chosen.  
5. Make a dataset wit al plant and seed eating birds.

#### Questions that I made to answer: 

**Question 1:** What diet do the heaviest bird species have?

**Question 2:** What is the most common diet for nocturnal mammals? 

#### SQL queries that I wrote to answer the questions: 
**Question 1:** 
```
CREATE VIEW CompareDietBodyMass AS 
SELECT SpecID, Diet_5Cat, BodyMass_Value 
FROM BirdFuncCleaned
GROUP BY Diet_5Cat 
ORDER BY BodyMass_Value DESC
```
**Question 2:** 
```
CREATE VIEW DietNocturnalSpecies AS 
SELECT MSW3_ID, Diet_Inv, Diet_Vend, Diet_Vect, Diet_Vfish, Diet_Vunk, Diet_Scav, Diet_Fruit, Diet_Nect, Diet_Seed, Diet_PlantO, Activity_Nocturnal 
FROM MamFuncCleaned
GROUP BY Activity_Nocturnal
```

#### Answers to the questions: 

**Question 1:** The heaviest bird species have a diet of vertebrates and fish. 
**Question 2:** Nocturnal species mostly eat insects. 
