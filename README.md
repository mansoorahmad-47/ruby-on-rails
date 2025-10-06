# Ruby on Rails

## p, puts, print, variables, and reverse
address = [1,2,3,4,5,6,7,8]

p address  &nbsp;&nbsp;&nbsp; -----> &nbsp;&nbsp;&nbsp;&nbsp;<sub>This prints the address array</sub>

new_address = address.reverse! &nbsp;&nbsp;&nbsp;----->&nbsp;&nbsp;&nbsp;&nbsp;<sub>The reverse! method will reverse data and destroy the original address with the new reversed one</sub>

p new_address

new_address2 = address.reverse &nbsp;&nbsp;&nbsp;----->&nbsp;&nbsp;&nbsp;&nbsp;<sub> meanwhile the reverse only reverse the address and save it in new_address2 but the original address remains the same as before </sub>