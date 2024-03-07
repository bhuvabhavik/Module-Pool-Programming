# TASK- 1 
- Create the two screens 100 and 200 and switch between these 2 screens.
1.create the program
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/abbd31ad-a5af-48db-b041-cbff092974d1)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/623baf96-c85a-4aa2-bf66-47fbda50fab9)

Right click on the program -create -screen

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c2523ae8-847d-4639-b2cb-9e80512ea5bc)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/d0d6241c-70e5-4393-a3ad-a48090d6b1c2)

## every screen has 3 parts- attributes, element list, flowlogic
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/6883d29e-07ef-4be0-acfc-b99d850a4521)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/4c573933-60f4-4339-a1e8-be99bf0d27c8)
-save it
# -right click and create another screen
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/0e5190a0-3d49-4638-9614-3ab230e7d73f)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/5da9baed-a8e4-4d67-9f4e-e480264cc67a)


# Module pool events
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8f4a09c9-2656-45af-b403-85a8e1ddd823)

# Now we will create the buttons on 2 screens-
when click on button on screen 100-navigate to screen 200
when click on button on screen 200-navigate back to screen 100

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8d584850-570b-4c2d-ad72-d37990a31ce2)

# we will create the button in the application toolbar
so we will uncomment module of screen 100. of PBO
- double click and create the new include
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/8c6cb915-2293-4a8e-b529-db80c50a0b88)
- this is the PBO Module
- now we will see how to create the button in the applicaiton toolbar
- uncomment and give the name to pf status
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/9faecbdc-e6fc-4fc7-97d7-f5dc0652f042)
- create the object
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a300e607-e109-45b5-a947-5088d6239920)
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/ec5e7f2e-97d7-4b5b-8bd6-71a1ff6131ed)
- we want button in application toolbar so expand the app toolbar
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/d366ef45-7256-406f-bd78-ae19de265372)
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/a7b60fd3-c03c-4197-a6fc-2a0d6e8abe90)
- give the name in our case HEADER, whatever we give here name is very important that will be used in the programming.
- wtever the name we give the same name we have the function code
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/def48821-3c40-4c78-ba99-8ce3cbf15276)
- everybutton in sap have function code which will be used in the programming.
- give funciton text suppose HEADER,
- icon name means symbolic image,symbol/image of the button- suppose ICON_NEXT_OBJECT
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c82be96b-8a8f-404c-bc22-067ab08f6d1b)
- we will choose some shortcut and give the icon text
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fc8e4c7d-8340-4831-9c96-405055908a57)
- continue and activate -before going back



- # @so weve covered 4 paarts of gui status, create button in PBO, create button in applicaiton toolbar in screen 100 


---
***

- now we will give the title to screen 100
- give the name , double cick and create the object and activate the object before back
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fb2dc32b-dd8e-4ab5-b075-496aed3f945f)
- ### now we have wrote the logic of pPBO in screen 100.

- uncomment process after input module and create the object
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/06747bb1-5bde-4d40-8864-e91d07c4ed49)
- here we will write the code of what shoud happen when user click the button on screen 100.

```abap
*----------------------------------------------------------------------*
***INCLUDE ZPRG1_MP_201_USER_COMMAND_0I01.
*----------------------------------------------------------------------*
*&---------------------------------------------------------------------*
*&      Module  USER_COMMAND_0100  INPUT
*&---------------------------------------------------------------------*
*       text
*----------------------------------------------------------------------*
MODULE user_command_0100 INPUT.
   call SCREEN '0200'.
ENDMODULE.
```

# now we will do the same things for screeen 200.

lets start it again for screen 200
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/78cb5c6c-c04b-4fa4-b387-fcd15e0c14ed)
> uncomment doubleclick createobjct
> -now we will go for the best practice here.
>
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c90d2545-0747-4ee5-a7a3-c396a1d3adad)
> ofcource we can create the new include heree
>   - but your every screen PBO logic we can put in one commmon include and your PAI logic of everyscreen we can  put in one common include so the best practice is to have all PBO in one include and PAI in one include.so here rather than creating the new include we will use the previous include we created.
>
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/f095c1dd-7ceb-4bea-bdab-d73d54016890)
> now we will uncomment and create the button for screen 200,giving the name item
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/91cd4b5f-11cf-4cee-af02-c584c3c7803b)
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/71a2e06c-48b5-4da3-88d6-f74ab688a216)

 ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/be6355d9-1010-468f-a065-f4d7155ed146)
provide text icon and move on..
save and activate.
back-
uncomment and provide the title
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c8475dc3-d5f8-4c76-94c3-863d2c482b1b)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/417a26ba-8e35-4197-9a9f-6f4ab55e4098)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/fa214e4c-34a4-4827-ae6c-09701c4b25cc)


# goto display mode right cick program name from sidebar and activate full program
  - before running we need to make sure ech and every part is active.
  - ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/aee9e3f0-3462-4bde-8d67-07b39906a585)

> [!NOTE]
> a tcode is cumpulsary for running module pool
> executable program we can run independently but mp program must need transaction code.
> ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c41383b9-1889-43d0-8c7d-d1c407e1c347)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/6298ec20-d45d-4021-805e-b4af6deea525)

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/1b4bf3fa-164a-4a1d-95a2-133c2bf17971)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/09dae1ad-73f5-4f77-a963-a02c3c9669bc)
now we can execute from right click as well s fom tcode.






















