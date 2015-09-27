# HackTX2015
import java.util.Scanner;

public class ChooseYourOwnAdventure
{
	//defaults
	public static int strength = 0, agility = 0, intelligence = 0, charisma = 0, stamina = 0, 
			points = 40, pointsToAdd = 0, attribute = 0; 
	public static String strengthString = "strength", agilityString = "agility", intelligenceString = "intelligence", 
			charismaString = "charisma", staminaString = "stamina", humanString = "human", dwarfString = "dwarf", 
			trollString = "troll", elfString = "elf", unknownString = "mysterious"; 
	public static String speciesName = "none", charName = "Switzerland";
	public static Scanner scan = new Scanner(System.in);

	public static void main(String args[])
	{		
		character();	
		goblin();
		orcs();
		skeletalDragon();
	}
	
	//a method to create a character based on input from the user
	public static String character()
	{
		theNaming();
		
		//call the method associated with the user-selected character
		System.out.println("\n\nGreetings, " + charName + ". Tell me about yourself. Are you a(n): "
					+ "\nHuman? \nTroll? \nElf? \nDwarf? \nUnknown creature?");		
		String species = scan.nextLine();
		
		//sets stats for human: jack-of-all-trades, master of none
		if(species.equalsIgnoreCase("human"))
		{
			setStats(humanString, 5, 6, 5, 6, 6);
		}
		//sets stats for troll: strong but stupid
		else if(species.equalsIgnoreCase("troll"))
		{
			setStats(trollString, 10, 4, 3, 3, 8);
		}
		//sets stats for elf: intelligent but weak
		else if(species.equalsIgnoreCase("elf"))
		{
			setStats(elfString, 2, 7, 10, 8, 2);
		}
		//sets stats for dwarf: robust but slow
		else if(species.equalsIgnoreCase("dwarf"))
		{
			setStats(dwarfString, 7, 5, 4, 4, 10 );
		}
		//sets stats for unknown: random number between 3 and 7
		else
		{
			setStats(unknownString, (int)(Math.random() * 4 + 3), (int)(Math.random() * 4 + 3), (int)(Math.random() * 4 + 3),
					(int)(Math.random() * 4 + 3), (int)(Math.random() * 4 + 3));
		}			
		
		addToStats();
		return charName;
	}

	//forces the user to choose hero or villain, asks for a name or assigns a neutral one
	public static void theNaming()
	{
		String choice = "Switzerland";
		while(!choice.equalsIgnoreCase("hero") || !choice.equalsIgnoreCase("villain"))
		{
			System.out.println("Hero or villain?");
			choice = scan.nextLine();
			
			if(choice.equalsIgnoreCase("hero"))
			{
				System.out.println("\nWhat is your name, hero?");
				charName = scan.nextLine();
				if(charName.equals("") || charName.equals(" "))
				{
					charName = "Switzerland";
				}
				break;
			}
			else if(choice.equalsIgnoreCase("villain"))
			{
				System.out.println("\nWhat is your name, villain?");
				charName = scan.nextLine();
				if(charName.equals("") || charName.equals(" "))
				{
					charName = "Switzerland";
				}
				break;
			}
		}	
	}
	
	public static void setStats(String speciesName, int setStrength, int setAgility, int setIntelligence, 
			int setCharisma, int setStamina)
	{
		System.out.println("\nHmmm, " + speciesName + ", are you?");
		strength = setStrength;
		agility = setAgility;
		intelligence = setIntelligence;
		charisma = setCharisma;
		stamina = setStamina;
	}
		
	//use points to level the character up
	public static void addToStats()
	{
		while(points > 0)
		{
			System.out.println("\nYou have " + points + " points to spend as you wish.");
			System.out.println("Your attributes: \nStrength: "+ strength + "\nAgility: " + agility + "\nIntelligence: " + intelligence 
						+ "\nCharisma: " + charisma + "\nStamina: " + stamina);
			
			//pick an attribute and add to it 
			System.out.println("Which attribute would you like to add to?");
			String attributeToAddTo = scan.nextLine();
			
			if(attributeToAddTo.equalsIgnoreCase("strength"))
			{
				actualAdding(points, pointsToAdd, strength, strengthString);
				strength = attribute;
			}
			else if(attributeToAddTo.equalsIgnoreCase("agility"))
			{
				actualAdding(points, pointsToAdd, agility, agilityString);
				agility = attribute;
			}
			else if(attributeToAddTo.equalsIgnoreCase("stamina"))
			{
				actualAdding(points, pointsToAdd, stamina, staminaString);
				stamina = attribute;
			}
			else if(attributeToAddTo.equalsIgnoreCase("charisma"))
			{
				actualAdding(points, pointsToAdd, charisma, charismaString);
				charisma = attribute;
			}
			else
			{
				System.out.println("Yes, intelligence is always a good place to add points.");
				actualAdding(points, pointsToAdd, intelligence, intelligenceString);
				intelligence = attribute;
			}
		}		
		System.out.println("\n\n\nNow, " + charName + ", aren't you curious about your quest? Do you want to "
				+ "start with... look out, behind you!");
	}
	
	//does the adding for the addToStats class... does most of the work, actually
	public static void actualAdding(int totalPoints, int pointsToAdd, int attributeInt, String attributeString)
	{
		System.out.println("How many points would you like to add? Note: the maximum is 20 points.");
		pointsToAdd = (int)scan.nextDouble();
		
		totalPoints -= pointsToAdd;
		if((totalPoints < 0) || (attributeInt + pointsToAdd) > 20)
		{
			System.out.println("Don't think I don't see what you're trying to do, " + charName + ".");
			String catchThatLine = scan.nextLine();
			totalPoints += pointsToAdd;
		}
		else
		{
			attributeInt += pointsToAdd;
			System.out.println("You now have " + attributeInt + " " + attributeString + " points.");
			String catchThatLine = scan.nextLine();
		}
		points = totalPoints;
		attribute = attributeInt;
	}
	
	
	public static void goblin() 
	{
    	int estrength = 4;
    	int eintelligence = 2;
    	int eagility = 5;
    	int estamina = 5;
    	int echarisma = 1;
    	int randomizer = 1;
    	randomizer = (int)(Math.random()*2+1);
    	estrength = estrength + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eintelligence = eintelligence + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eagility = eagility + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	estamina = estamina + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	echarisma = echarisma + randomizer;
    	battleAttack(estrength, eintelligence, eagility, estamina, echarisma);   	 
    	battleDefensive(estrength, eintelligence, eagility, estamina, echarisma);
   	 
	}
    
	public static void orcs ()   
	{
    	int estrength = 7;
    	int eintelligence = 6;
    	int eagility = 4;
    	int estamina = 9;
    	int echarisma = 2;
    	int randomizer = 1;
    	randomizer = (int)(Math.random()*2+1);
    	estrength = estrength + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eintelligence = eintelligence + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eagility = eagility + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	estamina = estamina + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	echarisma = echarisma + randomizer;  	 
    	battleAttack(estrength, eintelligence, eagility, estamina, echarisma);
    	battleDefensive(estrength, eintelligence, eagility, estamina, echarisma);
	}
    
	public static void skeletalDragon() 
	{
    	int estrength = 14;
    	int eintelligence = 17;
    	int eagility = 19;
    	int estamina = 14;
    	int echarisma = 20;
    	int randomizer = 1;
    	randomizer = (int)(Math.random()*2+1);
    	estrength = estrength + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eintelligence = eintelligence + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	eagility = eagility + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	estamina = estamina + randomizer;
    	randomizer = (int)(Math.random()*2+1);
    	echarisma = echarisma + randomizer;
    	battleAttack(estrength, eintelligence, eagility, estamina, echarisma);   	 
    	battleDefensive(estrength, eintelligence, eagility, estamina, echarisma);
	}


    
	public static void battleDefensive(int estrength, int eintelligence, int eagility, int estamina, int echarisma)   
	{
    	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
    	int emATK = (eintelligence*10)/8 + (echarisma*10)/2;
    	int epATK = (estrength*10)/7 + (estamina*10)/3;
    	double edodge = eagility/20.;
    	double echarmed = echarisma/50.;
    	int ehealing = eintelligence*10;
   	 
    	int strength = 5;
    	int intelligence = 5;
    	int agility = 6;
    	int stamina = 6;
    	int charisma = 6;	 
    	double randy = Math.random()-500;
    	double randyTwo = Math.random()-500;
    	int randomizer = (int)((Math.random()*10)+1);
   	 
    	int hitPoints = (strength*100)/4 + (stamina*100)/6;
    	int mATK = (intelligence*10)/8 + (charisma*10)/2;
    	int pATK = (strength*10)/7 + (stamina*10)/3;
    	double dodge = agility/70.;
    	double charmed = charisma/100.;
    	double defense = ((strength *10)/2 + (stamina *10)/8 +randomizer);
    	int healing = intelligence*10;
   	
    	if (dodge<randy)	{
        	System.out.println("\nThe enemy's attack missed!");
    	}else if (echarmed<randyTwo)	{
        	System.out.println("\nYou have been seduced by the enemy and have missed your opportunity to strike!");
    	}else  {
        	hitPoints = hitPoints - (emATK + epATK) + (int)((emATK + epATK)*defense/100);
        	System.out.println("\nThe enemy's attack suceeded! You have lost " + ((emATK + epATK) - (int)((emATK + epATK) * 
        			defense/100)) + " hit points and you have " + hitPoints + " hitpoints left!");	 
	}  
}

	public static void battleAttack(int estrength, int eintelligence, int eagility, int estamina, int echarisma)   
	{
    	int randomizer = (int)((Math.random()*10)+1);
    	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
    	int emATK = (eintelligence*10)/8 + (echarisma*10)/2;
    	int epATK = (estrength*10)/7 + (estamina*10)/3;
    	double edodge = eagility/20.;
    	double echarmed = echarisma/50.;
    	double edefense = ((estrength*10)/8 + (estamina*10)/8+randomizer);
    	int ehealing = eintelligence*10;
   	 
    	int strength = 5;
    	int intelligence = 5;
    	int agility = 6;
    	int stamina = 6;
    	int charisma = 6;	 
    	double randy = Math.random()-500;
    	double randyTwo = Math.random()-500;
 
   	 
    	int hitPoints = (strength*100)/4 + (stamina*100)/6;
    	int mATK = (intelligence*10)/8 + (charisma*10)/2;
    	int pATK = (strength*10)/7 + (stamina*10)/3;
    	double dodge = agility/70.;
    	double charmed = charisma/100.;
    	double defense = ((strength *10)/2 + (stamina *10)/8 +randomizer);
    	int healing = intelligence*10;
   	  
    	if (edodge<randy)	
    	{
        	System.out.println("" + randy);
        	System.out.println("\nYou have missed your attack!");
    	}
    	else if (charmed<randyTwo)	
    	{
        	System.out.println(""+ randyTwo);
        	System.out.println("\nYour enemy has become entranced by you and has missed their opportunity to attack");
    	}
    	else  
    	{
        	ehitPoints = ehitPoints - (mATK + pATK) + (int)((mATK + pATK)*defense/100);
        	System.out.println("\nYour attack succeeded! Your enemy lost " + ((mATK + pATK) - (int)((mATK + pATK) *
        			edefense/100)) + " hit points and now has " + ehitPoints + " hitpoints left!");
    	}
	}
}
