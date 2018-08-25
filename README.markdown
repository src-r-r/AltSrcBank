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
    1. User
    2. (Exit Application)
    ======================
    Choice (0 - 2):

### User Menu

So far, only the user sub-menu is displayed. Enter `1` to enter the User
sub-menu.

    ==============
    User
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3):

### User Menu: Account Creation

    ==============
    User
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3):

To create a user select `2`. Set an email address and password and hit
`ENTER` to once the user is created.

If the email is invalid or the passwords do not match then the program will
notify the user and ask the information to be put in again.


### User Login

Now that a user is created, the user can log in.

    ==============
    User
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3): 3

Choose "3" from the provided menu. a login prompt will be displayed. 

    ==============
    User
    --------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. Log In
    ==============
    Choice (0 - 3): 3

    Enter an empty email address to cancel logging in.
    Email address: a@a.b
    Password: Press ENTER to continue...

If invalid credentials are supplied, an error will be shown and the user will
be asked to log in again.

If the user is successful, the following menu will be shown:

    ===================
    User
    -------------------
    0. (Previous Menu)
    1. List Users
    2. Add User
    3. (a@a.b) Log Out
    ===================
    Choice (0 - 3):

To see account deails (since this is a banking application after all,
select `0` to go to the previous menu).

    ======================
    AltSrcBank
    ----------------------
    1. User
    2. (Exit Application)
    3. Account View
    ======================
    Choice (0 - 3): 

Yay! Looks like there's an "Account View" menu item. Select `3` to go to the
account menu.

### Account Overview

    =======================
    Account View
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 

Within the account view, a user can add a deposit or withdrawal, view the user's
balance, or view the user's transaction history.

### Account Depsoit.

To add a depost select `1`.

    =======================
    Account View
    -----------------------
    0. (Previous Menu)
    1. Deposit
    2. Withdraw
    3. View Balance
    4. Transaction History
    =======================
    Choice (0 - 4): 1

Enter the deposit amount.

    Deposit Amount (e.g. 4.25):6.45
    Press ENTER to continue...

This value can either be a whole number (e.g. `4`) or a decimal. To accomodate
for differente currencies and exchange rates any number of decimal places is 
valid.

If, however, an invalid value is entered, the application will ask the user
to enter a different value.