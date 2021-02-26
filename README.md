# Thermostat

Specification:

1. Thermostat starts at 20 degrees
2. You can increase the temperature with an up function
3. You can decrease the temperature with a down function
4. The minimum temperature is 10 degrees
5. If power saving mode is on, the maximum temperature is 25 degrees
6. If power saving mode is off, the maximum temperature is 32 degrees
7. Power saving mode is on by default but it can also be turned off
8. You can reset the temperature to 20 with a reset function
9. You can ask about the thermostat's current energy usage: < 18 is low-usage, <= 25 is medium-usage, anything else is high-usage.
10. (In the challenges where we add an interface, low-usage will be indicated with green, medium-usage indicated with black, high-usage indicated with red.)


Tests:

Unit Test 1. Temp (that starts at 20 degrees) can increase
Unit Test 2. Temp (that starts at 20 degrees) can decrease
  Feature Test 1. "+" can increase temp
  Feature Test 2. "-" can decrease temp
Unit Test 3. Temp can only decrease to 10 degrees
  Feature Test 3. "-" decrease stops at 10 degrees
    * Refactor Note: May be able to combine with FT2
Unit Test 4. While Power Save Mode is on (default) temp can only increase to 25 degrees
  Feature Test 4. "+" increase temp to 25 degrees when Power Save Mode is on
  Feature Test 5. "+" increase temp to 32 degrees when Power Save Mode is off
    * Refactor Note: May be able to combine FT4 & FT5 with FT1 for 2 tests, on and off
  Feature Test 6. Reset button resets temp to 20 degrees
  Feature Test 7. Usage button displays the current energy usage