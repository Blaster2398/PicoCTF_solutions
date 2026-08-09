![](images/pasted-image-20260809145354.png)

When we put this on the terminal 
.
![](images/pasted-image-20260809145732.png)

1)  We are already provided with a scrambled/encoded flag 
2) the Hint suggests that its base64 encoded 

### Failed Attempts
we try to reverse the process 
.
![](images/pasted-image-20260809145850.png)

so we need to put some command that can reverse it on the net cat terminal 
.
some failed attempts 
![](images/pasted-image-20260809150100.png)

this is the site that was there in the hints 
https://man7.org/linux/man-pages/man1/tr.1.html

so i am guessing we have to reverse the whole encoded string using the tr command .

another failed attempt ( I was trying ROT13 )
.
![](images/pasted-image-20260809150833.png)


This time we get something different in the nc terminal 
.
![](images/pasted-image-20260809150947.png)


### Finally 
1) use  baes64 -d to decode the encoded string 
2) and then reverse the string 
.
![](images/pasted-image-20260809152215.png)

4) ![](images/pasted-image-20260809152359.png)
5) ![](images/pasted-image-20260809152542.png)
6) ![](images/pasted-image-20260809152707.png)

so all the commands in line are 

```bash 
base64 -d
rev
tr '-' '_'
tr '()' '{}' 
tr 'a-zA-Z' 'n-za-mN-ZA-M'
```

```
picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_7a89a9da}
```

