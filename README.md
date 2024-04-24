# IvyWallet to Cashew CSV Converter
Use this script to convert [Ivy Wallet](https://github.com/Ivy-Apps/ivy-wallet) to [Cashew](https://github.com/jameskokoska/Cashew).

The reason I am doing this is because Iliyan, the creator and the maintainer of Ivy, recently mentioned on Telegram that he is no longer using his app, reverted to using a spreadsheet, and is thinking of stopping using the app completely.

Now Ivy Wallet works great for me, but I do not want to use an app that the creator does not use. So I decided to look for an alternative and found Cashew. It seems to be built similarly by a single developer and is open-sourced. So I am giving it a try.

Moving my data from Ivy to Cashew was not straightforward, and I am writing a small guide to help those who want it.

# How to move data from Ivy Wallet to Cashew?

1. Export data from Ivy Wallet
2. Use the code in this repo with the backup CSV file obtained from step 1 `python Converter.py BACKUP_FILENAME.CSV`
3. Import the `CashewPrelim.csv` file obtained from step 2 into Cashew

## If you have transfers how to set them correctly?
Cashew saves transfers as two transactions of the "Balance Correction" category. Unfortunately, they are not detected correctly from importing the CSV. So here is what you can do:
1. Create a small transfer between two accounts (will be deleted later). This will create the native hidden "Balance Correction" category.
2. Go to More -> Categories, and you will find in the list two "Balance Correction" categories. One which has only two transactions (the one created in step 1), and one with all your Ivy Wallet transactions.
3. Go the the one with the Ivy Wallet transactions, press on "Merge Category", and select the other "Balance Correction" category.
4. Don't forget to delete your transfers from step 1, and you're done.

## Now set up the app to your liking. All the transactions should have moved properly.
