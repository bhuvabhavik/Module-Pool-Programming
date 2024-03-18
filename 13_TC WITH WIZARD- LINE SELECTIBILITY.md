# TABLE CONTROL WITH WIZARD - SELECTIBILITY

## --# LINE SELECTIBILITY..


![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1cc634da-e789-4526-9659-5b9fff6d85f5)


![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1fca0c6a-0e34-485a-b658-f2c657d09ef7)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/07912a3d-c308-48eb-ac1f-f581ac3f1ded)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/9f09bfaf-8d28-4db3-8a90-8e5529a034e8)

> we will not select the first row because this column will be used for single and multiple records seleciton of the table.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8ac28f5c-8337-4a8f-9365-5bb193eaaab7)

here we will select line selectability and pass the corrospinding column. we can choose single and multiple selection.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/e856547c-5e0b-4352-95ca-a91461114ecc)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/08ef5788-815a-482c-994e-9639b171c9df)

continue ... complete...
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/b38bca48-afca-4b7d-9965-bfb4d0277247)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/02199b43-3c84-40ad-8f32-01c1f08fec73)


go to pai of screen 100, uncomment user command module..and create object
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/160a58a7-b5df-4755-9f30-47d2146b38e8)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/82aa79bd-ffee-4fa4-add3-fff8d0f3fd18)
then declare lv_ono in global program
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/60575821-05be-496b-b711-225fd7daec97)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/044f69f0-d026-4328-aac8-c4c91a859087)

# PROBLEM-old data not going
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/17ee25e7-50e0-4df7-91e6-ae464b356cbb)


WE WILL CREATE NEW TABLE FOR MAINTAING SELECTED RECORDS EXAMPLE ZPAYMENT
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/d06b6e1d-d581-4dd9-aaeb-ecfad36883cc)


![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/39a5d72a-84af-41d3-a8e8-95974fa18b88)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/6dced398-cb3e-442e-983f-4753ef2cf114)
g0to technical settings
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/74062199-9df4-4e0c-b9f8-2995e93c7ea2)
save and activate
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1e3b849d-0f7e-443b-a0a6-85413353b0db)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/e277d92a-eb79-4ab6-a061-f6a76bc47b7d)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/bd063efd-b979-4808-bac0-b221e9262c6a)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/733d0de5-c061-4ab6-9b72-8b1f3d850e13)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/91042274-574f-4ed0-99b6-21fb63d1448b)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a156e367-5561-4f07-ac09-6b608f8100c3)
now we have data in the internal table we will push that data in the table now zpayment
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ba261421-4870-496c-a5c3-924d5920346e)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/be5eb55c-3d5b-4bb6-b4ac-4a580c6336d5)

if we push data to zpayment then that data will deleted from the final list.
but if we execute the program again the data will be shown again because that data is coming from header and item table so lets fix it
> but we cant just directly delete the data from the item table directly because thats the main table and might be using in some other place too...so customer requirement is dont delete but it but dikhna bhi nhi chahiye..😥
> so lets look what can we do it..
> 
-so we will declare a new internal table structure and wa.
now we will write the logic to fetch the data from the new table.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/d899d839-f28f-4c8c-8fd4-148d00ba7355)

> now we will simply compare, if we find the matching records we will delete that records.
>
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a86c4773-f706-4b2d-a87a-9274a6365abf)
>
> 




















