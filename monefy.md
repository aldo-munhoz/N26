# Monefy test cases

Monefy tests cases were defined based on the application user experience. I created a flow shown in the image below and it reflects the paths the user will take to use the functionalities of the application.

![Full flow](https://github.com/aldo-munhoz/N26/blob/master/monefy_full_flow.png)

So, first I focused on the main screen and the buttons presented to the user, then I started checking the menus and all its particularities.

Of course, the flow is designed to provide only the "happy paths", and alternate and error conditions were not included in this flow, like including invalid numbers and invalid currencies. There are cases, not shown in the flow, like trying to choose a category without providing a expense amount which causes an error and the application already handles it by changing the expense amount background from green to red for a quick moment.

The flow, however drives the tester what paths he/she needs to follow to completely test the application. 16 different paths were documented as test cases:

## Add New Expense
Error conditions not considered in this test case, but they should be addressed as well
- Click the minus icon
- Define the Expense date
- Choose type of account
- Type the expense value
- Choose the expense category
> **Expected result:**
> A New Expense is included and shown in parenthesis in the middle circle.
> Balance is computed with the difference between incomes and expenses.

![Test Case 1](https://github.com/aldo-munhoz/N26/blob/master/path_01.png)

## Add New income
Error conditions not considered in theis test case, but they should be addressed as well
At least, one test case for each screen icon must be created, to ensure expenses are created accordingly for each of them.
A test case for adding a zero expense must be considered, to check whether the app allows it.
- Click the plus icon
- Define the Income date
- Choose type of account
- Type the income value
- Choose the income category
> **Expected result:**
> A new income is included and shown in green font in the middle circle.
> A difference between the income and the expense is shown in the balance box.

![Test Case 2](https://github.com/aldo-munhoz/N26/blob/master/path_02.png)

## Modify Existing Category
- Click ellipsis button on the upper right corner
- Click the Categories icon
- Click the icon you want to modify
- Choose a new icon for the category
- Press Done
> **Expected result:**
> The chosen category icon is changed

![Test Case 3](https://github.com/aldo-munhoz/N26/blob/master/path_03.png)

## Delete Existing Category
- Click ellipsis button on the upper right corner
- Click the Categories icon
- Click the icon to be deleted
- Hit the Delete icon on the upper right corner
> **Expected result:**
> The category no longer shows among the existing ones

![Test Case 4](https://github.com/aldo-munhoz/N26/blob/master/path_04.png)

## Disable Category
- Click the ellipsis button on the upper right corner
- Click the Categories icon
- Click the category to be disabled
- Click the ellipsis button on the top right corner
- Click the Disable option presented
- Click the Done link on the top left corner
> **Expected result:**
> The disabled category is grayed out and shown in the bottom of the category

![Test Case 5](https://github.com/aldo-munhoz/N26/blob/master/path_05.png)

## Enable Category
- Click the ellipsis button on the upper right corner
- Click the Categories icon
- Click the category to be enabled
- Click the ellipsis button on the top right corner
- Click the Enable option presented
- Click the Done link on the top left corner
> **Expected result:**
> The enabled category is sorted by name and painted in white

## Merge Categories
- Click the ellipsis button on the upper right corner
- Click the Categories icon
- Click the first category to be merged
- Click the ellipsis button on the top right corner
- Click the Merge option presented
- Choose the second category to be merged
> **Expected result:**
> A backup is created and the message is presented at the bottom of the screen
> Status message informing that the two categories were merged is presented at the bottom of the screen
> First category no longer shows up in the list of Categories

![Test Case 6](https://github.com/aldo-munhoz/N26/blob/master/path_06.png)

## Create New Category
- Click the ellipsis button on the upper right corner
- Click the Categories icon
- Click the Plus icon at the right of the category name
- the other steps depend on a pro version to be checked
> **Expected result:**
> A new category is added to the list of Categories

![Test Case 7](https://github.com/aldo-munhoz/N26/blob/master/path_07.png)

## Modify Existing Account Information
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the account to be changed
- Change the currency
- Choose the Exchange rate
- Type the initial account balance
- Choose the initial balance date
- Enable the "Included in the balance" option
- Choose the account icon
- Press the Done link in the upper left corner
> **Expected result:**
> The existing account information is changed

![Test Case 8](https://github.com/aldo-munhoz/N26/blob/master/path_08.png)

## Remove Account from Balance
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the account to be changed
- Disable the "Included in the balance" option
- Press the Done link in the upper left corner
> **Expected result:**
> The existing account is removed from the balance

![Test Case 9](https://github.com/aldo-munhoz/N26/blob/master/path_09.png)

## Delete Existing Account
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the account to be deleted
- Press the trash icon button on the upper right corner
> **Expected result:**
> The account is removed from the list of Accounts

![Test Case 10](https://github.com/aldo-munhoz/N26/blob/master/path_10.png)

## Disable Account
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the account to be disabled
- Click the ellipsis button on the top right corner
- Click the Disable option presented
- Click the Done link on the top left corner
> **Expected result:**
> The disabled account is grayed out and shown in the bottom of the accounts list

![Test Case 11](https://github.com/aldo-munhoz/N26/blob/master/path_11.png)

## Enable Account
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the account to be enabled
- Click the ellipsis button on the top right corner
- Click the Enabled option presented
- Click the Done link on the top left corner
> **Expected result:**
> The enabled account is painted in white and is sorte by its name

## Merge Accounts
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the first account to be merged
- Click the ellipsis button on the top right corner
- Click the Merge option presented
- Choose the second account to be merged
> **Expected result:**
> A backup is created and the message is presented at the bottom of the screen
> Status message informing that the two accounts were merged is presented at the bottom of the screen
> First account no longer shows up in the list of Accounts

![Test Case 12](https://github.com/aldo-munhoz/N26/blob/master/path_12.png)

## Create New Account
- Click the ellipsis button on the upper right corner
- Click the Accounts icon
- Click the Plus icon at the right of the category name
- Type the account name
- Select the currency
- Select the exchange rate
- Type the initial account Balance
- Choose the initial balance date
- Enable the "Included in the balance" option
- Choose the account icon
- Press Add in the upper right corner
> **Expected result:**
> A new account is added to the list of Accounts

![Test Case 13](https://github.com/aldo-munhoz/N26/blob/master/path_13.png)

## Modify Existing currency
This item requires a pro license, so all possible test cases can't be fully identified
- Click the ellipsis button on the top right corner
- Click the Currencies icon
- Buy a Pro license
- Click the Cancel link
> **Expected result:**
> No action is performed

![Test Case 14](https://github.com/aldo-munhoz/N26/blob/master/path_14.png)

## Modify Configuration item
There should be a test case per configuration item. Here I am only presenting a single one
- Click the ellipsis button on the top right corner
- Click the Settings icon
- Select the configuration item to change
- Change the selected configuration item
> **Expected result:**
> Configuration item is changed

![Test Case 15](https://github.com/aldo-munhoz/N26/blob/master/path_15.png)

## Apply Filter
There should be a test case per filter. Here I am only presenting one
- Click the Filter icon on the top left corner
- Choose the granulairty of the Filter
> **Expected result:**
>The top of screen label is changed according to the granularity chosen
>The expenses and incomes are filtered according to the granularity chosen

![Test Case 16](https://github.com/aldo-munhoz/N26/blob/master/path_16.png)

## Check summarizing items
- Click the balance rectangle in the middle of screen
- Click each of the summarized item, to expand them
- Verify whether the number of summarized rows is equal to the value shown at the left of each category
- Verify if all lines in the category sum up the total of the summarized category
> **Expected result:**
> Categories are summarizing correctly

## Check positive balance
- Click the balance rectangle in the middle of the screen
- Verify whether the positive values (green) less the negative values (red) is equal to the value shown in the balance
- Verify whether a positive balance is shown in green
- Verify whether a negative balance is shown in red
> **Expected result:**
> Positive balance is shown as a green rectangle

## Check negative balance
- Click the balance rectangle in the middle of the screen
- Verify whether the positive values (green) less the negative values (red) is equal to the value shown in the balance
- Verify whether a negative balance is shown in red
> **Expected result:**
> Negative balance is shown as a red rectangle

## Check percentile
- Verify whether the categories included in the balance have a line connecting them to the middle circle
- Verify whether the categories included in the balance have a percentage underneath their icon
- Click the circle area related to a given category
- Check whether the sub-items show up expanded
- Calculate the total expense for the selected category
- Calculate the total expense
- Calculate the ratio (category expense total)/(expense total)
- Check whether the above ratio equals to the shown ratio
> **Expected result:**
> Shown ratio equals calculated ratio

## New Transfer
- Click the Transfer icon on the top of the screen
- Choose the transfer date
- Type the transfer amount
- Press the Save button
- Filter by account
> **Expected result:**
> Transfer information is presented in the list of transactions

## Swipe
Other filters may be applied
- Filter by Day
- Swipe the main screen from right to left
> **Expected result:**
> Expenses made in different dates show up in the corresponding dates