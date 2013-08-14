The Texas Instruments TMP100 is an I2C Bus temperature sensor device. It provides accurate temperture measurement at the PCB for embedded designs.

This driver provides the following functions:


SET CONFIGURATION
BYTE temperature_set_config (BYTE config)
Returns 1 if configuration was set sucessfully, 0 if not
config:
OS/ALERT | R1 | R0 | F1 | F0 | POL | TM | 1=Shutdown

R1:0 Resolution Convertsion Time (typ)
00 9 Bits (0.5°C) 40ms
01 10 Bits (0.25°C) 80ms
10 11 Bits (0.125°C) 160ms
11 12 Bits (0.0625°C) 320ms


READ TEMPERATURE
BYTE read_temperature (SIGNED_WORD *temperature)
Returns 1 if temperature was read sucessfully, 0 if not
temperature:
Returned 12 bit temperature reading is x0.0625ºC (16 bits per 1ºC). 0×0000 = 0ºC

 

Please view the sample source code files for full information regarding the driver.