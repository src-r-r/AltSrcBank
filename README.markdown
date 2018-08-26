# AltSource Bank

The AltSource Bank is a full-stack(ish) application that simulates a bank
application. The program does the following operations:

-Create a new account
-Login
-Record a deposit
-Record a withdrawal
-Check balance
-See transaction history
-Log out

The application is **menu-driven**, so once the program runs, the operations are
able to be performed. However, data is not persistent, so the session will not
be saved after the program exits.

## Running the program.

The program is run on the command line and takes no arguments (a very agreeable
program, indeed):

    > ASCBCLI.exe

Upon first run of the program, this will be displayed to the user:

    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    ======================
    Choice (0 - 2):

To select an item, press the corresponding number key. If the number typed is
incorrect the application will warn you and ask you to try again. Note that
due to a known issue, the choice range at the prompt may initially start with
a "0." Even so, only the listed numbers above (in this case, 1 and 2) are valid
choices.

To set up a user account we need to type "1."

    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    ======================
    Choice (0 - 2): 1

## User Menu

Now we've entered the user menu.

    ==============
    User Menu
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3):

Since no users are in the system, we must add a new user. Type "2" to add
a new user.

    ==============
    User Menu
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3): 2

You'll then be prompted for an email and password, which must be entered twice.

    Email address: hello@world.com
    Password: 
    Password (Confirm): 
    1 Users
    Press ENTER to continue...

If the email is invalid or passwords do not match an error will be displayed.
To cancel account creation, simply make one of the password fields blank.

Upon creation of a user account you can now log in.

## Logging in.

After account creation the user menu is displayed once again.

    ==============
    User Menu
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3):

Press "3" to log in.

    ==============
    User Menu
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3): 3

    Enter an empty email address to cancel logging in.
    Email address: hello@world.com
    Password:
    Press ENTER to continue...

If you entered the correct credentials you used to sign in you'll see the user
menu appear with a "Log Out" menu item:

    ===================
    User Menu
    -------------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. (hello@world.com) Log Out
    ===================
    Choice (0 - 3):

There's also a new submenu within the main menu. Press "0" to return to the
root menu.

    ===================
    User Menu
    -------------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. (hello@world.com) Log Out
    ===================
    Choice (0 - 3): 0

## Account Sub-Menu

Once a user is logged in an "Account Menu" is displayed in the main menu.

    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    3. Account Menu
    ======================
    Choice (0 - 3):

Press "3" to enter the account menu.

    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    3. Account Menu
    ======================
    Choice (0 - 3): 3

The account menu has 4 items:
    - *Deposit*. Deposit an amount in the user account.
    - *Withdraw*. Deposit an amount from the user account.
    - *View Balance*. View the current balance for the user account.
    - *Transaction History*. Show an ordered list of account transactions.

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4):

## Account Deposits <a name="deposits">

To record a deposit, press "1" in the menu.

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 1

Enter the deposit amount as either a whole number (e.g. `7`) or a decimal (e.g.
`2.99`). If the number is in an invalid format (e.g. `7.2.1.2`), an error will
be displayed and you'll need to enter a valid number.

    Deposit Amount (e.g. 4.25): 89.32
    Press ENTER to continue...

Upon successful creation of a deposit, the Account Menu will be displayed
again.

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4):

## View Balance

To view your account balance, type "3" into the menu prompt:

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 3
    Your balance is 89.32
    Press ENTER to continue...

## Account Withdrawals

To record a withdrawal type "2" in the Account Menu.

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 2

The same rules apply as with the [Account Deposits](#deposits). The only thing
to note is that you are allowed to withdraw more money than what is in your
account. Your account will just be a negative balance.

## Account Transaction History

Finally, to view your account history, select "4" in the account menu.

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 4
    Deposit                       8/25/2018 9:27:29 AM                         89.32
    Withdrawal                    8/25/2018 9:27:51 AM                          9.11
    Press ENTER to continue...

The columns are listed as follows:

1. Type of transaction
2. Timestamp of transaction
3. Amount associated with the transaction.

## Logging out

To log out of the application, go to the previous menu by pressing "0":

    =======================
    Account Menu
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 0
    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    3. Account Menu
    ======================
    Choice (0 - 3):

Now select "1" to enter the User menu.

    ===================
    User Menu
    -------------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. (a@a.a) Log Out
    ===================
    Choice (0 - 3):

To log out, press "3".

    ===================
    User Menu
    -------------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. (a@a.a) Log Out
    ===================
    Choice (0 - 3): 3
    Press ENTER to continue...
    
This is the state of the User menu when the user is logged out:

    ==============
    User Menu
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3):

In addition, the root menu lacks the Account menu.

    ======================
    AltSrcBank
    ----------------------
    1. User Menu
    2. (Exit Application)
    ======================
    Choice (0 - 2):