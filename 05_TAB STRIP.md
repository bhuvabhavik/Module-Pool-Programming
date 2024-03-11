# TAB STRIP >>>

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/208b3f19-c801-44d6-8c65-728fc1f2f421)

when we want the output in different tabs then we will create the tab strip
- so in our case we will create the two tabs one for the header data and one for the item data,
- so lets see how to create the tab strip in module pool.
- zprg4_mp_201 //program name ssuppose

- firsat we will create the screen suppose 0100.

- we will create some elements
- ![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/02b60a8b-ca75-44a7-bd90-0e59e9038bb0)

drag and drop tab strip wuith wizard..
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/b2aab304-f5af-45b6-957f-0b4fd2929c0b)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/43b8f17b-082b-466c-bd35-1079b6b03676)
for every tab sap will automatically create the sub screen.
continue..continue and complete..

now we will design the layout on the subscrens..

so lets start with creating the structures.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/c4ee3659-ad53-4f0f-8c51-71bb496301a3)
craete structures and was
goto screen 0101 and design the subscreen for header items
gto data/dictionary object>pass table and implement the layout for required items.

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/cb1c7c17-9aec-43fa-9bec-bdbc283847f4)

same way we will go to 102 screen and designt the item layout.

because item data can be multiple for one header so we will create the table control.

so goto 102 screen layout and design the table control
-drag and drop table control with wizard.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/2ad4e070-6700-4808-a26f-b6c6f4614235)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/079fe5b7-c885-4b8d-b8f4-6d6117a69b79)
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/3f1acdf6-998a-4852-bd37-af2390ccee96)

select all/required fields and continue

continue..enable scroll..continue..continue...🥂🥂🥂

![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/99e2f955-a61b-46d4-a008-01a7496a8f2c)
create tcode for execute

>[!NOTE]
> so now we will write the logic for displaying the data at process after input of screen 100.
>so we will goto screen 100 code and uncommment the PAI module of screen 100 and write the code.
![image](https://github.com/bhuvabhavik/Module-Pool-Programming/assets/49744703/60328ebd-0e3c-4873-a2f0-bbd0fed4edd4)


