![](images/pasted-image-20260809211737.png)

the V and Z in switches in the command are 
![](images/pasted-image-20260809211850.png)

![[Pasted image 20260809212007.png|700]]


let's see what type of port is this                                                                                                             
![](images/pasted-image-20260809213442.png)

more about what we got                                                                  
![](images/pasted-image-20260809213847.png)

while normal samba ports are `139` and `445` here we are getting this `53687` , also its open so we can run smbclient 
```bash
smbclient -L mysterious-sea.picoctf.net -p 51292 -N
```

![](images/pasted-image-20260809214442.png)

As its a smaba client we can use `smbclient` and `smbutil`
	Now we want to navigate into the `shares` so we can use this command 
	
```bash
smbclient //mysterious-sea.picoctf.net/shares -p 51292 -N
```

![](images/pasted-image-20260809214848.png)

![[Pasted image 20260809215126.png|700]]

get the files using the `mget <pattern_or_*>`                                                                                            
![](images/pasted-image-20260809215245.png)


![](images/pasted-image-20260809215453.png)

```
picoCTF{5mb_pr1nter_5h4re5_7a400ec3}
```

