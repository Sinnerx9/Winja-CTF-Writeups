# Bomb Defusal<br />
We got a login console malware :-P<br />

## Target<br />
[\*] Find Password <br />
[\*] Get The FLAG!!!!!! <br />

## Solution<br />
lets head to analysis the malware using IDA Pro.<br />
![](images/1.png)<br />
Here We get a lot things<br />
**[\-] the malware write bat script called `temp.bat` and write `0%|0%`**<br />
**[\-] Also its request for password and check if it equal to 00000000, Length = 7**<br />
**[\-] if we enter the password correct it will call function named `winner`**<br />
**[\-] Lets Jump to it :D**<br />
![](images/2.png)<br />
**[\-] Here it will Print not that easy or something like this**<br />
**[\-] But there is someting intersting we got string "akf\`|600abe0cc7bf15764460Xd7i\`u3stX7iXC6aart6i\`Xso4Xe7jez\`", and XOR key 0x07**<br />
**[\-] the string used in the code but not printed....**<br />
**[\-] Xor this string with 0x07 we will get the flag...**<br />
## YES THATS EASY :-P<br />
flag{177feb7dd0ea62013317_c0ngr4ts_0n_D1ffus1ng_th3_b0mb}<br />