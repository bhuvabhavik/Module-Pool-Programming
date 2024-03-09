# MODAL DIALOG BOX SCREEN...

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ab97d58f-2bd7-4926-b2d5-01c664126b35)
requirement: 
screen 100: user input the order number
screen 200: modal dialog box
when user pass input and hit enter the data should be visible in modal box screen and on hitting ok/enter modal screen should go away.

program: zprg3_mp_201 //ash

create 2 type of screen layouts first..

uncomment and create pai of screen 100
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/e444ce7f-4586-4359-9cb4-57babef9e684)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c370779c-f977-4de3-840f-0753b00c8080)

now when user will click sublit buton screen 2oo will open.

now we have a okay button in screen 200 so on clicking that we havae to goback to screen 100
so lets goto screen 200 PAI


```abap
*----------------------------------------------------------------------*
***INCLUDE ZPRG3_MP_201_USER_COMMAND_0I01.
*----------------------------------------------------------------------*
*&---------------------------------------------------------------------*
*&      Module  USER_COMMAND_0100  INPUT
*&---------------------------------------------------------------------*
*       text
*----------------------------------------------------------------------*
MODULE user_command_0100 INPUT.
call SCREEN '0200' STARTING AT 10 20
ENDING AT 50 60.
ENDMODULE.
*&---------------------------------------------------------------------*
*&      Module  USER_COMMAND_0200  INPUT
*&---------------------------------------------------------------------*
*       text
*----------------------------------------------------------------------*
MODULE user_command_0200 INPUT.
leave to SCREEN 0.
ENDMODULE.
```


![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/cdbb7187-0d2f-4636-a40b-9b6098a6351d)
now we have the funcitonal structure built.
now our task is to load off the data.

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f9145704-04ca-4b7d-a10c-9ca02c6daa5d)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a7cb7ee7-475c-4e0b-9b4a-94fbcff941da)

