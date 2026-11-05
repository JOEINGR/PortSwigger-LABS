# **LAB 1 : Username enumeration via different responses**

## Lab description:

<img width="1030" height="486" alt="image" src="https://github.com/user-attachments/assets/1e7569ed-6f72-42ed-bf85-830bf4962b14" />

### SOLUTION:

STEP 1: Access the login page looking like this;

<img width="1132" height="447" alt="image" src="https://github.com/user-attachments/assets/369a57f5-3e97-495f-99be-831129542f5b" />

Open Burp suite &rarr; Proxy &rarr; intercept &rarr; open web browser and paste the URL &rarr; HTTP history  . Then look for the POST login request, and check for the username and password parameters and highlight the username parameter to the burp intruder.

<img width="1393" height="423" alt="image" src="https://github.com/user-attachments/assets/4069ed3c-2f1d-44b6-a3a0-14da5f7db57d" />

Add the payload position on the username , keep it as sniper attack() , and payload type we use simple list and paste the given candidate names in the payload configuration. and then start the attack.

<img width="1397" height="598" alt="image" src="https://github.com/user-attachments/assets/0721329b-1b52-483e-ac39-9f9ea97e7006" />

from the attack result , look for the payload that resulted into different length. as it indicates difference in error message. for our case it is acid

<img width="1392" height="362" alt="image" src="https://github.com/user-attachments/assets/e1c3c0ee-910e-41b3-8cb7-ecd2cc692494" />

then change the username parameter into the enumerated username " acid " and add the payload position to the password parameter. and paste the candidates passwords in the payload configuration.then run the attack

<img width="1398" height="588" alt="image" src="https://github.com/user-attachments/assets/3f5c7741-3024-4fd6-815f-9752c3a23e1b" />

then from the attack , look for the payload with different respond status . which indicates a successful login.

<img width="1381" height="326" alt="image" src="https://github.com/user-attachments/assets/1c640179-404d-42be-9cec-be746a9a9a4d" />

```
username : acid

password : 123456789

```









