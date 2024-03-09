# SCREEN PAINTER..

> [!NOTE]
> now we will design the header layout on the 100 screen and item layout on the screen 200.
> we will use screen painter for designing the screen in module pool.
> how to go to screen painter?
> click screen and goto layout.
> we will crete this type of design
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/2ac3dc2d-2d40-45a5-bb28-652f57fa1375)
>  ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/4f22dc30-18ff-4036-ad3c-2670c197415f)

- now we will create the input field where user can input the field.
- select and drop input output field

- we will name as tablename-columnname
- zordh__28-ono
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/703ee135-e97c-4f59-8d5f-793ed54b9d4b)
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f44cc637-5714-4820-8bc4-4dd3dba41be3)


 > [!NOTE]
> as we all know every function requires a function code so give it to button.
>
>![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/036452af-3eab-4ac2-b0b4-095e78bd07d0)


now we need to fetch display various data from header table when user passes the order number in the input field.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a6b8cc13-c9e8-48d2-ace1-2f5cc5c150cc)
goto dictionary/program field
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/cab8386b-2523-4354-b1ec-4a324779037c)
select the fields you want
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f5b0676d-1e4c-4b91-a474-38b8f0d3aaec)
this isthe automatic and shortcut method, else we can doit manually too.

>[!NOTE]
>this 4 are our output field not input so
>so double click > goto properties > goto attributes > program > and deselect input.
>we have designed this screen so far
>![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/5f84adaf-510b-4a06-9209-4468c0b7cc10)
>now we will write the logic to fetch data from header table and display it.
>

next we will crete the structure
```abap
PROGRAM zprg1_mp_201.

TYPES: BEGIN OF lty_data,
         odate TYPE zordh__28-odate,
         pm    TYPE zordh__28-pm,
         ta    TYPE zordh__28-ta,
         curr  TYPE zordh__28-curr,
       END OF lty_data.
DATA: lt_data TYPE table of lty_Data,
      lwa_data TYPE lty_data. 

INCLUDE zprg1_mp_201_status_0100o01.

INCLUDE zprg1_mp_201_user_command_0i01.
```


now we need to write the logic part in PAI because we need to fetch data when the user passed the input.

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/315a8bdf-f31a-4124-a41e-8d4134d1e02e)

now we will  work on item details so we will create the structures and all for screen 200.

```abap
*&---------------------------------------------------------------------*
*& Modulpool ZPRG1_MP_201
*&---------------------------------------------------------------------*
*&
*&---------------------------------------------------------------------*
PROGRAM zprg1_mp_201.
TABLES: zordh__28,ZORDI_28.

TYPES: BEGIN OF lty_data,
         ono   TYPE zordh__28-ono,
         odate TYPE zordh__28-odate,
         pm    TYPE zordh__28-pm,
         ta    TYPE zordh__28-ta,
         curr  TYPE zordh__28-curr,
       END OF lty_data.


TYPES: BEGIN OF lty_data1,
         oin    TYPE zdeoitmno_28,
         odesc TYPE   zdeodesc_28,
         icost  TYPE zdeoitcost_28,
       END OF lty_data1.


DATA: lt_data  TYPE TABLE OF lty_data,
      lwa_data TYPE lty_data.

DATA: lt_data1  TYPE TABLE OF lty_data1,
      lwa_data1 TYPE lty_data1.


INCLUDE zprg1_mp_201_status_0100o01.

INCLUDE zprg1_mp_201_user_command_0i01.
```



now we will learn how to create table control using wizard.

>[!NOTE]
>goto screen 200 > layout > drag and drop table control
>![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/53675b87-631e-4d16-9a47-afcfdbd44b82)


perform all the steps 1 by one which have appeared.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a67657a8-7be1-40ce-a032-4af04edc9768)

select interal table and workarea
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/7a4b53bb-3853-424e-a09b-72e0d811da55)

select all fields and go next
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ec01d23d-9589-4b50-9db0-94a15297fd59)
CONTINUE THIS
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/e0aa47ad-4dfb-4981-bdc5-af99f1cc7b67)
SCROLL YES CONTINUE...CONTINUE..COMPLETE..🎉🎉🙌🙌🥂🥂

- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/aadf6734-14db-49df-b9fc-a13fbf1ac81f)


🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁🍁

NOW WE WILL WRITE THE LOGIC FOR FETCHING THE DATE IN THE ITEM TABLE
-SO FIRST WE WILL CHECK IF THE DATA EXISTS IN THE PRIMARY OR HEADER TABLE
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/0c6aec26-087e-44ac-b65b-eb8d9f04c725)






