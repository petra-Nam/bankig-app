### **Hey Everyone! Here's a Banking System I Built in Java**  

Hey there, fellow coders! 👋  

I recently took on a fun project to sharpen my Java skills: I created a simple **banking system**! It’s a menu-driven console application that simulates some basic banking operations, and I’m pretty excited to share what I built and learned along the way.

https://github.com/petra-Nam/learn-java/discussions/7
---

### **What Does It Do?**  

The program revolves around a single `Account` class, which acts as the blueprint for managing bank accounts. Here’s a quick rundown of the features:  
- **Create an Account**: Start by creating an account with an initial deposit.  
- **Deposit Money**: Add funds to the account (because who doesn’t like growing their balance?).  
- **Withdraw Money**: Safely withdraw funds, but only if you have enough balance.  
- **View Account Information**: Check the account holder's name and current balance.  

The program runs through a menu system, making it easy to interact with each feature step by step.  

---

### **How I Did It**  

1. **The Core Class: `Account`**  
   I designed an `Account` class with private fields for `accountHolderName` and `balance`. The methods like `deposit()`, `withdraw()`, and `displayAccountInfo()` handle the operations. Here's a snippet:  

   ```java
   class Account {
       private String accountHolderName;
       private double balance;

       public Account(String accountHolderName, double initialBalance) {
           this.accountHolderName = accountHolderName;
           this.balance = initialBalance;
       }

       public void deposit(double amount) {
           if (amount > 0) {
               balance += amount;
               System.out.println("Successfully deposited $" + amount);
           } else {
               System.out.println("Deposit amount must be positive.");
           }
       }

       public void withdraw(double amount) {
           if (amount > 0 && amount <= balance) {
               balance -= amount;
               System.out.println("Successfully withdrew $" + amount);
           } else if (amount > balance) {
               System.out.println("Insufficient balance!");
           } else {
               System.out.println("Withdrawal amount must be positive.");
           }
       }

       public void displayAccountInfo() {
           System.out.println("Account Holder: " + accountHolderName);
           System.out.println("Current Balance: $" + balance);
       }
   }
   ```

2. **Interactivity with a Menu**  
   Using a `Scanner`, I built a menu-driven interface to interact with the user dynamically. The user can pick options like depositing, withdrawing, or viewing the account info.  

3. **Validation**  
   I added basic validation to ensure that users can’t deposit negative amounts or withdraw more than their balance.  

---

### **What I Learned**  

- **Object-Oriented Programming**: Designing the `Account` class was a great way to practice encapsulation and method-driven programming.  
- **Error Handling**: It was fun thinking about edge cases—like what happens if someone tries to withdraw more than they have?  
- **User Interaction**: Building a menu-driven system makes the program feel interactive and user-friendly.  

---

### **What’s Next?**  

This was a great start, but there’s so much room to grow:  
- Adding **multiple accounts** so you can manage more than one user.  
- Keeping a **transaction history** to show deposits and withdrawals.  
- Introducing **data persistence** by storing account details in a file or database.  
- Maybe even building a **GUI version** using JavaFX!  

---

### **Final Thoughts**  

Creating this project was a lot of fun, and it really helped me understand some key Java concepts. If you’re looking for a practical project to try, I’d definitely recommend building a banking system—it’s simple, but you can keep adding features to make it more complex and interesting.  

What do you think? Any ideas on how I can improve it? Let me know! 😊
