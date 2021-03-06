# Lab 2: Dominik Gedeon

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   <img width="352" alt="greaterthan" src="https://user-images.githubusercontent.com/99871518/156147946-c0d672a8-023f-4d17-afd4-9a0c7394b30f.png">


   Less than:

   <img width="349" alt="lessthan" src="https://user-images.githubusercontent.com/99871518/156147993-6d2d3a74-cc21-4efb-972c-172d2db8c389.png">

2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   Greater than:
   
   <img width="233" alt="greaterthanfn" src="https://user-images.githubusercontent.com/99871518/156149102-6b43070b-1537-4e3b-b790-fc366ec3950f.png">
   
   Less than:
   
   <img width="305" alt="lessthanfn" src="https://user-images.githubusercontent.com/99871518/156149152-df1a3c30-3d47-4bb2-9062-d684f57fb8a8.png">


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx59**

```vhdl
   p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;
        
        --ID digits: 59
        --5 --> 0101
        --9 --> 1001

        -- First test case
        s_b <= "0101"; 
        s_a <= "1001";        
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination b=0101, a=1001 FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   <img width="707" alt="log" src="https://user-images.githubusercontent.com/99871518/156160523-b2c50761-95ee-4697-826e-75ac38b8ef8d.png">


3. Link to your public EDA Playground example:

   https://www.edaplayground.com/x/gtVs
