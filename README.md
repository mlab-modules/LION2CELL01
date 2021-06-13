
[Czech](./README.cs.md)
<!--- module --->
# LION2CELL01D
<!--- Emodule --->

<!--- subtitle --->Li-ion battery management module<!--- Esubtitle --->

![LION2CELL01D](/doc/img/LION2CELL01D_top_big.jpg)

<!--- description --->
Integrated battery management solution for 18650 li-ion batteries. It can measure remaining energy in battery, perform charging cycle from external power source and protect batteries against over voltage or over draining conditions.

## Features 

  * Charging, balancing, termination (temperature protected)
  * Gas-gauging (temperature compensated)
  * Over-voltage protection
  * Over-current protection
  * Under-voltage is not protected - the module is constructed to power the device until battery death 

## Connection

The module could communicate on I2C or HDQ bus.

| Mark | signal| Description |
|------|-----|---|
|1 | PG |	|
|2 | STAT2 | |
|3 | GND |	|
|4 | CE | |
|5 | STAT1 | |
|6 | CMODE | |

<!--- Edescription --->
