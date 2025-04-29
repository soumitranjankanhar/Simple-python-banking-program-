# Simple-python-banking-program-#

class SimpleBanking:
    def __init__(self):
        self.balance = 0

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            return f"Deposited: {amount}. New balance: {self.balance}"
        else:
            return "Invalid deposit amount"

    def withdraw(self, amount):
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
            return f"Withdrawn: {amount}. New balance: {self.balance}"
        elif amount > self.balance:
            return "Insufficient balance"
        else:
            return "Invalid withdrawal amount"

    def check_balance(self):
        return f"Current balance: {self.balance}"

# Example usage
bank = SimpleBanking()
print(bank.deposit(100))
print(bank.withdraw(50))
print(bank.check_balance())
