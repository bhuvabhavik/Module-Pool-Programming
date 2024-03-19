# PROCESS ON HELP REQUEST -- F1 HELP

NOW IN THE SAME FIELD WE WILL CREATE THE F1 HELP ALSO
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c015750b-4e46-4ddd-9e31-4a8044104a21)

- WHENEVER WE WANT TO CREATE DOCUMENTATION IN SAP WE ALWAYS USE SE61

- SO WE WILL CREATE THE DOCUMENTAION THROUGH SE61 AND WE THEN WE WILL CREATE IN THE PROGRAM.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/51be2358-e08a-4354-83f5-1502b54e2f6b)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/6232c50b-dda2-431b-8235-f3fcda72db2e)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/9c7df1d0-4a40-4090-a660-7ea91caa660f)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/77d72231-2a36-45f3-839e-06826fa2bbc6)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/e14f949a-d513-42ba-85b9-9463a3cc2dd6)
- double click > create
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/4bcdbee1-f457-4a6c-b31a-08e4dacc99e2)
- now we will call the function module to call the documentation inside our module.
- the function module name is # help_object_show, so lets call that first..
- 😎😎😎😎

```abap
*----------------------------------------------------------------------*
***INCLUDE ZMP_MULTIPLE_SUBSCREEN_F1HEI01.
*----------------------------------------------------------------------*
*&---------------------------------------------------------------------*
*&      Module  F1HELP  INPUT
*&---------------------------------------------------------------------*
*       text
*----------------------------------------------------------------------*
MODULE f1help INPUT.

*DATA DOKCLASS TYPE DSYSH-DOKCLASS.
*DATA DOKLANGU TYPE DSYSH-DOKLANGU.
*DATA LINKS    TYPE STANDARD TABLE OF TLINE.

  CALL FUNCTION 'HELP_OBJECT_SHOW'
    EXPORTING
      dokclass                            = 'TX' "which we provided while creating documentation
*     DOKLANGU                            = SY-LANGU
      dokname                             = 'ZONO' "name we provided while creating documentation.
*     DOKTITLE                            = ' '
*     CALLED_BY_PROGRAM                   = ' '
*     CALLED_BY_DYNP                      = ' '
*     CALLED_FOR_TAB                      = ' '
*     CALLED_FOR_FIELD                    = ' '
*     CALLED_FOR_TAB_FLD_BTCH_INPUT       = ' '
*     MSG_VAR_1                           = ' '
*     MSG_VAR_2                           = ' '
*     MSG_VAR_3                           = ' '
*     MSG_VAR_4                           = ' '
*     CALLED_BY_CUAPROG                   = ' '
*     CALLED_BY_CUASTAT                   = CALLED_BY_CUASTAT
*     SHORT_TEXT                          = ' '
*     CLASSIC_SAPSCRIPT                   = ' '
*     MES_PROGRAM_NAME                    = ' '
*     MES_INCLUDE_NAME                    = ' '
*     MES_LINE_NUMBER                     = MES_LINE_NUMBER
*     MES_EXCEPTION                       = ' '
*   TABLES
*     LINKS                               = LINKS
   EXCEPTIONS
     OBJECT_NOT_FOUND                    = 1
     SAPSCRIPT_ERROR                     = 2
     OTHERS                              = 3
            .
  IF sy-subrc <> 0.
* Implement suitable error handling here
  ENDIF.


ENDMODULE.
```
  
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/bfc33ed6-cdce-47f4-ba9e-64dc2e1c0f54)


