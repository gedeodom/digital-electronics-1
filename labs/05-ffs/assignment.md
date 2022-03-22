
### Flip-flops Dominik Gedeon

1. Listing of VHDL architecture for T-type flip-flop. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of t_ff_rst is
    signal s_q : std_logic;
begin
    --------------------------------------------------------
    -- p_t_ff_rst:
    -- T type flip-flop with a high-active sync reset,
    -- rising-edge clk.
    -- q(n+1) = t./q(n) + /t.q(n)
    --------------------------------------------------------
    p_t_ff_rst : process(clk)
    begin
        if rising_edge(clk) then  -- Synchronous process
            if (rst='1') then
                s_q <= '0';
            elsif (t='0') then
                s_q <= s_q;
            else 
                s_q <= not s_q;
            end if;
                
        end if;
    end process p_t_ff_rst;

    q     <= s_q;
    q_bar <= not s_q;
end architecture Behavioral;
```

2. Screenshot with simulated time waveforms. Try to simulate both flip-flops in a single testbench with a maximum duration of 200 ns, including reset. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

  <img width="586" alt="waveforms" src="https://user-images.githubusercontent.com/99871518/159218821-0ba67713-7778-4753-a871-fba0c980737c.png">
 

### Shift register

3. Image of the shift register `top` level schematic. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

![scheme](https://user-images.githubusercontent.com/99871518/159437061-0324a293-265c-474c-9273-9211a7cbc342.png)


