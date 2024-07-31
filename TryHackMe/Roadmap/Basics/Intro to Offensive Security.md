###### Task 1

```
Q: Which of the following options better represents the process where you simulate a hacker's actions to find vulnerabilities in a system?
 	- Offensive Security
 	- Defensive Security
 	
A: Offensive Security
```

###### Task 2

Open terminal and type:
```
gobuster -u http://fakebank.com -w wordlist.txt dir
```

You will notice a **/bank-transfer** site. In Firefox, in the search bar, visit fakebank.com/bank-transfer and transfer 200$ from 2276 to 8881. You will see the answer to the question when you return to your account.

```
Q: If your transfer was successful, you should now be able to see your new balance reflected on your account page. Go there now and confirm you got the money! (You may need to hit Refresh for the changes to appear)

  

Above your account balance, you should now see a message indicating the answer to this question. Can you find the answer you need?

A: BANK-HACKED
```