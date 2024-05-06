# LAB 1 - GHDL and GTKWave

### Process
- Went to the GitHub repository of Digital System Design (DSD) + Studied VHDL and GHDL
- Went to the GHDL folder and followed [this](https://www.youtube.com/watch?v=H2GyAIYwZbw) tutorial to download necessary software

## HALF ADDER - OUTPUT

<img width="827" alt="image" src="https://github.com/will-chimbay/CPE322/assets/123396327/f93560fd-e938-4c52-bd4c-2b8fc05c8565">

### CODE (ha and ha_tb files):
ha.vhdl:
```
library ieee;
use ieee.std_logic_1164.all;

entity ha is
    port
    (
        a:  in  std_ulogic;
        b:  in  std_ulogic;
        o:  out std_ulogic;
        c:  out std_ulogic
    );
end ha;

architecture behave of ha is
begin
    o <= a xor b;
    c <= a and b;
end behave;
```
ha_tb.vhdl:
```
library ieee;
use ieee.std_logic_1164.all;

entity ha_tb is
end ha_tb;

architecture test of ha_tb is
	component ha
		port
		(
			a:	in	std_ulogic;
			b:	in	std_ulogic;
			o:	out	std_ulogic;
			c:	out	std_ulogic
		);
	end component;
	
	signal a, b, o, c : std_ulogic;
begin
    half_adder: ha port map (a => a, b => b, o => o, c => c);
    
    process begin
    
    a <= 'X';
    b <= 'X';
    wait for 1 ns;
    
    a <= '0';
    b <= '0';
    wait for 1 ns;
    
    a <= '0';
    b <= '1';
    wait for 1 ns;
    
    a <= '1';
    b <= '0';
    wait for 1 ns;
    
    a <= '1';
    b <= '1';
    wait for 1 ns;
    
    assert false report "Reached end of test";
    wait;
    
    end process;
    
end test;
```
## D Flip-Flop Implementation - OUTPUT

<img width="791" alt="image" src="https://github.com/will-chimbay/CPE322/assets/123396327/08eb5ba3-8c14-403e-b09f-95745f4ebc69">

> created new project (dff) and implemented changes in code
