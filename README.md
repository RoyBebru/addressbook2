# addressbook2

The program is an address book that runs in a command-line mode in terminal window.


To run program use command

    $ python3 main.py

The command prompt looks like this:

    (101(17(1((C>

or

    (101(17(1((@>

where:
  - **101** means amount of all records;
  - **17** means amount records in **MATCH set**;
  - **1** means amount records in **MATCH subset** of **MATCH set**;
  - **C** means that address book is not modified yet;
  - **@** means that address book is modified and must be saved to file.

Most commands work with 2 sets: **MATCH set** and **MATCH subset**. **MATCH set** is formed by the **show** or **all** command. The **search** command selects **MATCH subset** from **MATCH set** based on a regular expression. **change** and **delete** commands are worked with **MATCH subset**. Each command has an Ukrainian synonym and can be shortened while ambiguity is absent. So, command **search** can be entered as **sea** or **se**, but not **s** because other command **show** has first letter **s**.

Application support the following commands:
  - **all**|**всі** - select to **MATCH set**/**subset** all record:
    ```
    (0(0(0((C> all
    (93(93(93((C>
    ```
  - **add**|**додати**|**додай** - add to address book new record or field:
    ```
    (93(93(93((C> add Мар'яна Архипівна Вандер-Вілька
    (94(94(1((@> show
    #94 Name: Мар'яна Архипівна Вандер-Вілька
    (94(94(1((@> add phone +38 (099) 730-99-90
    (94(94(1((@> show
    #94 Name: Мар'яна Архипівна Вандер-Вілька
        Phone: +38 (099) 730-99-90
    (94(94(1((@>
    ```
    Name can be up to 3 words with "'" and "-" symbols.

    There exists the following fields:
      - **phone**: 
      - **address**:
      - **birthday**:
      - **comment**:
     
