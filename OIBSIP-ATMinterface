import java.util.Scanner;
class BankAccount 
{
    	int remaining_amout;
  	 int previous_transaction;
    	String Name;
    	String Id;
    	int flag = 0;
	BankAccount(String cName, String cId)
	{
		Name = cName;
        		Id = cId;
   	}
	void checkId()
	{
		System.out.println("Welcome " + Name);
        		System.out.println();
        		System.out.print("Please enter the Customer ID or PIN: ");
        		Scanner id = new Scanner(System.in);
        		String chk = id.nextLine();
        		if (chk.equals(Id)) 
		{
           			showMenu();
        		}
 		else 
		{
            			System.out.println("*********************************");
            			System.out.println("Sorry....! Wrong Login!!");
            			System.out.println("*********************************");

            			if (flag < 3) 
			{
                				flag++;
                				checkId();
            			}
        		}
    	}

    	void deposit(int amount) 
	{
        		if (amount != 0) 
		{
            			remaining_amout = remaining_amout + amount;
            			previous_transaction = amount;
        		}
    	}

   	void withdraw(int amount) 
	{
        		if (this.remaining_amout > amount) 
		{
           	 		remaining_amout = remaining_amout - amount;
            			previous_transaction = -amount;
        		} 
		else 
		{
          			System.out.println("*********************************");
            			System.out.println("Sufficient balance not available for the withdrawl!");
            			System.out.println("*********************************");
        		}
    	}

    	void getPrevTransaction() 
	{
        		if (previous_transaction > 0) 
		{
            			System.out.println("Deposited: " + previous_transaction);
        		} 
		else if (previous_transaction < 0) 
		{
            			System.out.println("Withdraw: " + Math.abs(previous_transaction));
        		} 
		else
		{
            			System.out.println("No Transaction Occured ");
        		}
    	}

    	public void transfer(double amount, BankAccount acc) 
	{
        		if (this.remaining_amout < amount) 
		{
			System.out.println("*********************************");
            			System.out.println("Transfer Fails due to insufficient balance!");
            			System.out.println("*********************************");
        		} 
		else 
		{
            			this.remaining_amout -= amount;
            			acc.remaining_amout += amount;
            			System.out.println("Account of " + this.Name + " becomes $" + this.remaining_amout);
            			System.out.println("Account of " + acc.Name + " becomes $" + acc.remaining_amout);
            			System.out.println("\n");
        		}
   	 }

    private void showMenu() {
        char option;
        Scanner sc = new Scanner(System.in);
        System.out.println("Welcome " + Name);
        System.out.println("Your ID is  " + Id);
        do {
           // System.out.println("\n");
            //System.out.println("\n");
            System.out.println("A. Check balance");
            System.out.println("B. Deposit");
            System.out.println("C. Withdraw");
            System.out.println("D. Previous Transaction");
            System.out.println("E. Transfer");
            System.out.println("F. Exit");

            System.out.println("*********************************");
            System.out.println("Enter your option");
            System.out.println("*********************************");
            option = sc.next().charAt(0);
            option = Character.toUpperCase(option);
            System.out.println("\n");

            switch (option) {
                case 'A':
                    //clrscr();
                    System.out.println("*********************************");
                    System.out.println("Remaining amout " + remaining_amout);
                    System.out.println("*********************************");
                    System.out.println("\n");
                    break;

                case 'B':
                   // clrscr();
                    System.out.println("*********************************");
                    System.out.println("Enter the amount to deposit");
                    System.out.println("*********************************");
                    int amount = sc.nextInt();
                    deposit(amount);
                    System.out.println("\n");
                    break;
                
                case 'C':
                   // clrscr();
                    System.out.println("*********************************");
                    System.out.println("Enter the amount to withdraw");
                    System.out.println("*********************************");
                    int amount2 = sc.nextInt();
                    withdraw(amount2);
                    System.out.println("\n");
                    break;

                case 'D':
                    //clrscr();
                    System.out.println("*********************************");
                    getPrevTransaction();
                    System.out.println("*********************************");
                    System.out.println("\n");
                    break;

                case 'E':
                    //clrscr();
                    System.out.println("*****");
                    System.out.println("To whom");
                    BankAccount bb = new BankAccount("moorthy", "1342");
                    System.out.println(bb.Name);
                    System.out.println("*****");
                    System.out.println("Amount to Transfer");
                    double am = sc.nextDouble();
                    System.out.println("*****");
                    transfer(am, bb);
                    break;

                case 'F':
                    //clrscr();
                    System.out.println("*****");
                    break;
                
                default:
                   // clrscr();
                    System.out.println("Invalid Option!!! Please Enter Again");
            }

        } while (option != 'F');
        System.out.println("ThankYou For using our services");

    }
}

public class ATMinterface {
    public static void main(String[] args) {
        BankAccount ba = new BankAccount("Sudheeksha", "2001");
        ba.checkId();
    }

}
