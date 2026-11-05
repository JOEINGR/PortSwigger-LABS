# **LAB 2 : Username enumeration via subtly different responses**

## **LAB Description :**

<img width="997" height="500" alt="image" src="https://github.com/user-attachments/assets/56e1d494-38ee-46dd-8c7b-c1ad128fec68" />

## **SOLUTION :**

Access the login page looking like this :

<img width="1483" height="468" alt="image" src="https://github.com/user-attachments/assets/aadcbb99-efd6-4a89-8bb1-059f82fea0eb" />

Open Burp suite &rarr; Proxy &rarr; intercept &rarr; open web browser and paste the URL &rarr; HTTP history  . Then look for the POST login request, and check for the username and password parameters and highlight the username parameter to the burp intruder.

<img width="1861" height="771" alt="Screenshot From 2026-11-05 18-36-04" src="https://github.com/user-attachments/assets/07fcfc13-7fe0-4682-9caf-e658bccfb498" />

Add the payload position on the username , keep it as sniper attack, and payload type we use simple list and paste the given candidate names in the payload configuration. and then start the attack.

<img width="1861" height="771" alt="Screenshot From 2026-11-05 18-39-08" src="https://github.com/user-attachments/assets/f7f3cfa7-fe95-47c7-af39-1675f01cb8b9" />

the attack never returned anypositive or useful result , as all length were the same . Then we had to look for a hiden change . so on payload configuration open &rarr; settings &rarr; grep extract and add the warning mentioned in the response by highlighting.


then run attack again , we can observe a certain payload with subtly result.

<img width="1863" height="931" alt="Screenshot From 2026-11-05 19-08-39" src="https://github.com/user-attachments/assets/1116e7c0-a9d8-4852-9a7c-e7f49cb797cc" />

add the username as static parameter and add the payload position on the password parameter and paste the candidate list of password given. but dont forget to remove the grep extract setting. then run the attack.

<img width="1863" height="791" alt="Screenshot From 2026-11-05 19-10-35" src="https://github.com/user-attachments/assets/13e67436-e8b9-4555-9345-2ace5312bece" />

then from the results we see a payload with different respond status (302) , which indicates that its the password which is valid.

<img width="1863" height="791" alt="Screenshot From 2026-11-05 19-14-31" src="https://github.com/user-attachments/assets/85da0d75-a999-4bcd-83b0-2bebba09233d" />

```
username : autodiscover

password : montana

```



