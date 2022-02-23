# Lab 1: Dominik Gedeon

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

![272999665_340857944593241_5888275324263124589_n](https://user-images.githubusercontent.com/99871518/155136074-23de74e1-a0f3-45b3-8352-6bc499ec1abd.jpg)


2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= ((b_i nand b_i) nand a_i) nand ((c_i nand c_i) nand (b_i nand b_i)); 
    f_nor_o  <= (b_i nor (a_i nor (c_i nor c_i)));  
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![waweforms1](https://user-images.githubusercontent.com/99871518/154935671-f7ff7c89-b33c-4c89-873b-7828706b5427.jpg)


2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/Mp2u](https://www.edaplayground.com/x/Mp2u)
