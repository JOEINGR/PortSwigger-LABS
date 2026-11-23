# **LAB 3 :SQL injection UNION attack, determining the number of columns returned by the query**

# **Lab Description:**

<img width="1750" height="794" alt="2026-11-23_04-13" src="https://github.com/user-attachments/assets/4bad22e6-04cd-4a61-9942-c0cd32093ddb" />

# **SOLUTION:**

Access the lab website seen as below;

<img width="3000" height="1776" alt="2026-11-23_04-18" src="https://github.com/user-attachments/assets/77c9ee9e-9f03-42a5-ba47-f9d82c642456" />

Open Burp suite → Proxy → Intercept → Open Browser → switch the intercept on and paste the login page URL onto the Burp browser and load it , Then select any category from the displayed ones (Food & Drinks) then on the burp side it will be displayed as seen below;

<img width="2974" height="1634" alt="2026-11-23_04-19" src="https://github.com/user-attachments/assets/acd67c14-af85-4070-8ff6-e23e29f18ff7" />

Then from the burp interceptor modify the filtering category parameter by adding (' UNION SELECT NULL-- ) after the filtered category name as seen below;

<img width="2974" height="1660" alt="2026-11-23_04-19_1" src="https://github.com/user-attachments/assets/9c1809a0-9e14-4838-a4f5-d20d0148c18b" />

After forwarding the request the website replied with an error because we only tested if there is one column using single NULL and its not the correct number of columns as seen below;

<img width="1758" height="630" alt="2026-11-23_04-20" src="https://github.com/user-attachments/assets/ec554d18-7b23-4074-9636-cb0d92583c04" />

Then after adding the 3 NULL's in to the payload ( ' UNION SELECT NULL,NULL,NULL-- ) Automatically it returned the columns present and hence it confirms there three columns, as seen below.

<img width="2956" height="1636" alt="2026-11-23_04-24" src="https://github.com/user-attachments/assets/582f5a6d-9911-4b20-ae54-81278f8d83f0" />

and the lab was solved.

<img width="2748" height="1630" alt="2026-11-23_04-26" src="https://github.com/user-attachments/assets/dfb6268b-360e-4daf-9610-ddf44ce0b555" />
