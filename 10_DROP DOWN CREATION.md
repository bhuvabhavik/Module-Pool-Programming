# ⏬DROP DOWN CREATION..⏬


here we willl create the dropdown list as shown:
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/3e3484b0-766c-40c4-bb21-a2b71eac966a)


so we will start with creating the table, withh two colums to maintain the states and regions.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1ef2224c-02a2-40c6-a5ab-0609bfeea5a5)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/0e9f76ed-01a5-4736-8f84-25f28b9daf52)
first column always mandt
create data element >> domain
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/527a080a-9da5-4dbe-a2ce-1e5e9c0c5e55)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/255b024e-2fa4-472a-b86b-570177734176)


NOW WE WILL GO FOR ANOTHER COLUMN REGION--
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8e888530-735d-45fd-9111-c718a7cfc839)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/b14adba2-3958-42a6-a1b8-9c46ddbe3fd4)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1175efa6-25ea-44d4-8b00-a76885591d37)

  ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/52b284df-6ba2-4d3a-874f-f2ce336043ce)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/84ef4a66-50a2-47e0-b9a9-bc7342b3534e)

NOW WE HAVE CREATED THE TABLE SO NOW WE WILL MAINTAINT THE DATA USING SM30.
FIRST WE WILLL CREATE THE tMG- TABLE MAINTAINANCE GENERATOR  AND THEN WE'LL MAINTAIN THE DATA.

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/3ee69a99-9ebd-4493-bab6-49242c516217)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fb6c1c8b-08ab-40ab-8e33-2be5e082c32e)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a0cc4b4b-f5ee-4a04-9a7c-dd73e6ab4091)


WE HAVE CREATED THE TMG

-NOW WE WILL GO TO SM30
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f2bbcc8d-12aa-4dfd-8da2-fc5a7d413de0)


NOW WE WILL GOTO SE38 AND CREATE A MODULE POOL PROGRAM.

> create a new screen.
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/bf61442b-cc8a-4488-b7ab-8eff71c248b1)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/218add36-7329-4691-9b26-34077d8e188f)
> dont have dropdown menu directly so we will take input output field as of now.
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/3a629e9b-56b4-4a49-b3cb-a353cad37fb7)
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/2741e601-dc62-4d16-96ac-b09bca40682e)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/4cb11b46-31b1-4bfa-9cbe-c14a0788578e)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/070c068e-f4a4-4c84-ba6f-d810ff1798d6)

now when user click the state suppose gujarat
then we have the cities of gujarat in lt_data
- we need to bind that data into region dropdown
- so where will we write our code??

> we will write in the PBO section as it is a layout specific change.
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fb43ae18-0c29-48b0-878f-52767fa31fbc)

>[!TIP]
>which function module we use to bind the data to the screen field.
>ANSWER : VRM_SET_VALUES

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/7365516f-8373-4335-bdbc-40b0cc5ea1b4)

> call function module: VRM_SET_VALUES

>[!WARNING]
> here we are passing lt_values to the function module.
>but lt_values is empty
>we have our data in lt_data
>so now anyhow somehow we have to move our data from lt_data to lt_values.
>
>![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/86fed7a7-5b1d-4ac8-a94f-8be3277c3ef1)
>![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fc033e0e-de37-46e0-b98f-96d61968983a)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/9a7d5b4a-f610-416c-bcbb-ba9963a016cb)

```abap
*----------------------------------------------------------------------*
***INCLUDE ZTABLE_REGION_STATUS_0100O01.
*----------------------------------------------------------------------*
*&---------------------------------------------------------------------*
*& Module STATUS_0100 OUTPUT
*&---------------------------------------------------------------------*
*&
*&---------------------------------------------------------------------*
MODULE status_0100 OUTPUT.
* SET PF-STATUS 'xxxxxxxx'.
* SET TITLEBAR 'xxx'.
 IF ztstate_region-state is not INITIAL.
DATA LT_VALUES TYPE VRM_VALUES. " internal table
DATA lwa_value TYPE vrm_value. "structure

refresh: lt_values. "refresing the internal table
loop at lt_data into lwa_data.
  lwa_value-key = lwa_data-region.
  lwa_value-text = lwa_data-region.
  append lwa_value to lt_values.
  ENDLOOP.

    CLEAr: ZTSTATE_REGION-REGION. "clear screenfield so always fresh data comes
   CALL FUNCTION 'VRM_SET_VALUES'
     EXPORTING
       id                    = 'ZTSTATE_REGION-REGION' "which field we are binding values ??
       values                = LT_VALUES
    EXCEPTIONS
      ID_ILLEGAL_NAME       = 1
      OTHERS                = 2.
   IF sy-subrc <> 0.
* Implement suitable error handling here
   ENDIF.
 ENDIF.
ENDMODULE.
```








