# Corona_data_analysis_using_hive

Choose a domain where you can apply big data analysis. In the selected domain:
1.	Write a schema of some important tables.
2.	Identify 10 problems that an individual might face.
3.	Find a solution to these challenges using big data analysis. Explain your solution with the help of HiveQL.

My chosen domain is Government and Health Sector.

There are 5 tables of different data of specifically current COVID-19 pandemic, they are named as: - 
1.	Total_India_case
2.	Datewise_India_case
3.	Daily_casedeath
4.	CFR
5.	Total_confirm_permillion

The Question and teir solutions are as follows:
1.	What is the total number of confirmed deaths due to current pandemic in India?
    This is calculated using function sum () on table total_india_case in hive whose result came out to be 489 till 2020-04-18.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809141-4819f880-ab5a-11eb-8650-544a2a78fde6.png)


2.	What is the daily number of confirmed cases in our country?
    This was calculated using different function and operation on queries i.e. sum (), count () whose result came out to be 240.8113 till 2020-04-18.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809147-4e0fd980-ab5a-11eb-8904-753d53a33550.png)

 
3.	In India, which state is adversely affected due to Covid-19 mass-spread?
    This problem was calculated using simple SQL concepts of where clause and multiple conditions on required table. The result is clear these 6 states are conditioned in worse  state of pandemic. 
    
    ![image](https://user-images.githubusercontent.com/50805925/116809153-52d48d80-ab5a-11eb-9f0e-1b9d729ea56d.png)

 

4.	Which state is in good condition and is predicted to recover soon from this mass-spread?
    This problem is to figure out the recovering state or the state in good condition, here multiple conditions were used on the table to get result, here the % of recoverins   where lesser the % better is the result.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809160-5831d800-ab5a-11eb-8496-55555079d769.png)

 

5.	What is the case fatality rate (CFR) of each state in India?
    CFR is an important factor in determining the extend of mass-spread which awakens us and is easy to calculate
    
    ![image](https://user-images.githubusercontent.com/50805925/116809171-6253d680-ab5a-11eb-9825-f7de0b668e4c.png)

 
    CFR is not constant it varies with many parameters but as per acquired and available data, this is the current CFR of each state. When there are people who have the disease but are not diagnosed, the CFR will overestimate the true risk of death. There might be many undiagnosed people. So testing is also major factor on which CFR depends.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809166-5e27b900-ab5a-11eb-96f6-1f18d9483dd2.png)

 

6.	What is the current average CFR of India? What does it tell us? 
    This is the problem where we used SQL function avg () to calculate the average CFR in whole India, which turned out to be 2.566.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809183-70095c00-ab5a-11eb-98a8-795556fa792f.png)

 

7.	Maharashtra has been declared severely affected and so many others. How much has the Maharashtra and all other affected states contributed to the Total Indian cases of   Covid-19?
   This problem took two queries to complete as together they got very complex. Here Contribution in total confirmed cases was measured firstly taking the total confirmed cases in India and then Using it in the formula
   In the query using max (), group by etc…

   Contribution per state = (Total confirmed in state / Total in India) *100
   
   ![image](https://user-images.githubusercontent.com/50805925/116809215-93340b80-ab5a-11eb-8f9a-f1e9770d78c0.png)
   
   ![image](https://user-images.githubusercontent.com/50805925/116809219-97602900-ab5a-11eb-8a36-4b33d7c4fa0a.png)



8.	Which state is considered to be untouched/not-affected with the Covid-19 virus?

    This problem is simple SQL query to find a state where the effect of pandemic and mass-spread is almost null. The query result came out to be Nagaland. 
    
    ![image](https://user-images.githubusercontent.com/50805925/116809232-a1822780-ab5a-11eb-853c-dea1824a91da.png)
  
 

10.	What is the estimated IFR (Infection Fatality Rate) for the whole India?

    This problem is solved using various function and formula where the data was limited and not updated regularly so IFR for India till date 2020-04-18 is 3.305

    The IFR = number of deaths from a disease divided by the total number of cases.
    
    ![image](https://user-images.githubusercontent.com/50805925/116809245-aa72f900-ab5a-11eb-9a42-5ee08d4b34e5.png)


 





