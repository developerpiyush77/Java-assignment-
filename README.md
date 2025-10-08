class Amount 
public Account(int accountNumber, String accountHolderName, double balance, String email, String phoneNumber) {
    this.accountNumber = accountNumber;
    this.accountHolderName = accountHolderName;
    this.balance = balance;
    this.email = email;
    this.phoneNumber = phoneNumber;
}


public void deposit(double amount) {
    if (amount > 0) {
        balance += amount;
        System.out.println("Amount deposited successfully. New balance: " + balance);
    } else {
        System.out.println("Deposit amount must be positive.");
    }
}


public void withdraw(double amount) {
    if (amount > 0) {
        if (balance >= amount) {
            balance -= amount;
            System.out.println("Amount withdrawn successfully. New balance: " + balance);
        } else {
            System.out.println("Insufficient balance!");
        }
    } else {
        System.out.println("Withdrawal amount must be positive.");
    }
}


public void displayAccountDetails() {
    System.out.println("Account Number: " + accountNumber);
    System.out.println("Account Holder: " + accountHolderName);
    System.out.println("Balance: " + balance);
    System.out.println("Email: " + email);
    System.out.println("Phone Number: " + phoneNumber);
}


public void updateContactDetails(String email, String phoneNumber) {
    this.email = email;
    this.phoneNumber = phoneNumber;
    System.out.println("Contact details updated successfully!");
}

public int getAccountNumber() {
    return accountNumber;
}
