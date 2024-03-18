# PROCESS ON VALUE REQUEST  >>>

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ab339817-b97f-43dc-95ea-cef6a85c3ad1)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/750c489a-7c35-42c3-9fb3-532ecd07cba6)

WE WILL LEARN IN THE MPDULE POOL PROGRAM OF MULTIPLE SCREENS WE CREATED EARLIER.

WE WILL CREATE THE SEARCH HELP FOR THIS ORDER  NUMBER FIELD.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a4b10de5-74f0-45db-8e86-c7df4c16c72d)

WE WILL DO AN EXTENSIVE PROCESS TO LEARN PROCESS ON VALUE REQUEST
```
OTHERWISE THE EASY SOLUTION FOR THE SAME IS TO
CREATE THE SEARCH HELP THROUGH SE11 AND
GOTO SCREEN PAINTER PROEPRTES OF THE INPUT FIELD AND
ASSIGN THE SEARCH HELP

```
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ae518fc2-ae19-4466-bd24-82fd4f778b9c)


# TASK
-Whenever user will press the f4 button process on value request will call and we will write the logic for the same.

-currently we dont have any search help button here
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8b393cc0-f755-4171-a123-2d09695a2ff2)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8285646a-78f8-4102-ac83-c587a5f17ed0)
and then double click and create the module
> so what we will do in the next part is fetch the order numbers from the header table and asign it to the screen field.
> we will call the function module 'F4IF_INT_TABLE_VALUE_REQUEST'
> we will pass the two most important parameters
> DYNPPROG (means screen-we can pass program name but we will pas sy-repid which contains the current program name)  and DYNPNR (dynpro number-screen number # sy-dynnr is the system variable for dynpro number )
> then asign dynprofield > you want to assign a help to which particular field pass-> 'LV_ONO' in our case
>
> now the first field retfield..it is directly connected to the internal table..
> whenever f4help will come values are in internal table whenever you select the ono which particular field of internal table you are returning?? 'ONO'
> now we will gofor value_org , 
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/b3dc4f7a-94b8-4ff0-96bc-18d113a977b3)
 - whenever we want to assign new search help we need to take 'S'.





# Conclusions..
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f3668d4b-996f-4e0c-8410-9b6e26a1d198)

```abap
*----------------------------------------------------------------------*
***INCLUDE ZMP_MULTIPLE_SUBSCREEN_F4HEI01.
*----------------------------------------------------------------------*
*&---------------------------------------------------------------------*
*&      Module  F4HELP  INPUT
*&---------------------------------------------------------------------*
*       text
*----------------------------------------------------------------------*
MODULE f4help INPUT.
    SElect ono
    FROM zordh__28
    INTO TABLE lt_ono.

*DATA DDIC_STRUCTURE   TYPE TABNAME.
*DATA RETFIELD         TYPE DFIES-FIELDNAME.
*DATA PVALKEY          TYPE DDSHPVKEY.
*DATA DYNPPROG         TYPE SY-REPID.
*DATA DYNPNR           TYPE SY-DYNNR.
*DATA DYNPROFIELD      TYPE HELP_INFO-DYNPROFLD.
*DATA STEPL            TYPE SY-STEPL.
*DATA WINDOW_TITLE     TYPE C.
*DATA VALUE            TYPE HELP_INFO-FLDVALUE.
*DATA VALUE_ORG        TYPE DDBOOL_D.
*DATA MULTIPLE_CHOICE  TYPE DDBOOL_D.
*DATA DISPLAY          TYPE DDBOOL_D.
*DATA CALLBACK_PROGRAM TYPE SY-REPID.
*DATA CALLBACK_FORM    TYPE SY-XFORM.
*DATA CALLBACK_METHOD  TYPE REF TO IF_F4CALLBACK_VALUE_REQUEST.
*DATA MARK_TAB         TYPE DDSHMARKS.
*DATA USER_RESET       TYPE C.

      CALL FUNCTION 'F4IF_INT_TABLE_VALUE_REQUEST'
        EXPORTING
*         DDIC_STRUCTURE         = ' '
          retfield               = 'ONO'
*         PVALKEY                = ' '
          DYNPPROG               = sy-repid
          DYNPNR                 = sy-dynnr
          DYNPROFIELD            = 'LV_ONO' "name of your field
*         STEPL                  = 0
*         WINDOW_TITLE           = WINDOW_TITLE
*         VALUE                  = ' '
         VALUE_ORG              = 'S'
*         MULTIPLE_CHOICE        = ' '
*         DISPLAY                = ' '
*         CALLBACK_PROGRAM       = ' '
*         CALLBACK_FORM          = ' '
*         CALLBACK_METHOD        = CALLBACK_METHOD
*         MARK_TAB               = MARK_TAB
*       IMPORTING
*         USER_RESET             = USER_RESET
        TABLES
          value_tab              = LT_ONO "whats your internal table in which you have values
*         FIELD_TAB              = FIELD_TAB
*         RETURN_TAB             = RETURN_TAB
*         DYNPFLD_MAPPING        = DYNPFLD_MAPPING
       EXCEPTIONS
         PARAMETER_ERROR        = 1
         NO_VALUES_FOUND        = 2
         OTHERS                 = 3
                .
      IF sy-subrc <> 0.
* Implement suitable error handling here
      ENDIF.


ENDMODULE.
```

































