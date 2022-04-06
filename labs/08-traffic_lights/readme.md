1. See [schematic](https://github.com/tomas-fryza/digital-electronics-1/blob/master/docs/nexys-a7-sch.pdf) or [reference manual](https://reference.digilentinc.com/reference/programmable-logic/nexys-a7/reference-manual) of the Nexys A7 board and find out the connection of two RGB LEDs, ie to which FPGA pins are connected and how. How you can control them to get red, yellow, or green colors? Draw the schematic with RGB LEDs.

| **RGB LED** | **Artix-7 pin names** | **Red** | **Yellow** | **Green** |
| :-: | :-: | :-: | :-: | :-: |
| LD16 | N15, M16, R12 | `1,0,0` | `1,1,0` | `0,1,0` |
| LD17 | N16, R11, G14 | `1,0,0`| `1,1,0` | `0,1,0` |

![schema_LED](https://user-images.githubusercontent.com/99871518/161964011-8d5680ba-d0bd-4dec-9731-d85b22a15a26.png)


2. See [schematic](https://github.com/tomas-fryza/digital-electronics-1/blob/master/docs/nexys-a7-sch.pdf) or [reference manual](https://reference.digilentinc.com/reference/programmable-logic/nexys-a7/reference-manual) of the Nexys A7 board and find out to which FPGA pins Pmod ports JA, JB, JC, and JD are connected.

![pmod_frontview](https://user-images.githubusercontent.com/99871518/161964027-a19337e5-f620-4daf-a44c-91772b443989.png)
![pmod_pin_table](https://user-images.githubusercontent.com/99871518/161964021-75978a86-074a-4e1a-ac3b-28396e88846f.png)

