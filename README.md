/**
 *determines basic enemy stats and
 *
 * @author (your name)
 * @version (a version number or a date)
 */
import java.util.Scanner;
public class Fantasy
{

   
	public static void turn()   {
    	double randomizerTurn = Math.random()-500;
    	int hitpoints = 1;
    	int ehitpoints = 1;
    	if (randomizerTurn<.3)  {
        	for(hitpoints = 1; hitpoints>0 && ehitpoints>0; hitpoints++)	{
        	ehitpoints = goblinAttack();
        	hitpoints = goblinDefensive();
        	String hat = scan.nextLine();
    	}
   	 
   	 
    	} else if (randomizerTurn <.6) {
                  	for( hitpoints = 1; hitpoints>0 && ehitpoints>0; hitpoints++)	{
        	ehitpoints = orcsAttack();
        	hitpoints = orcsDefensive();
        	String hat = scan.nextLine();
    	}
    	} else {
                  	for( hitpoints = 1; hitpoints>0 && ehitpoints>0; hitpoints++)	{
     	hitpoints = skeletalDragonAttack();
     	hitpoints = skeletalDragonDefensive();
     	String hat = scan.nextLine();
    	}
   	 
    	}
    	if (hitpoints >0)   {
       	 
        	System.out.println("Congratulations, you survived. Press Enter to continue");
        	String hat = scan.nextLine();
       	 
   	 
   	 
    	} else {
       	System.out.println("You've failed. Go somewhere and recover. Game Over.");
       	String hat = scan.nextLine();
      	 
      	 
    	}
    
	}
	public static int goblinAttack() {
    	int estrength = 4;
    	int eintelligence = 2;
    	int eagility = 5;
    	int estamina = 5;
    	int echarisma = 1;

    	System.out.println("You are facing a goblin!");
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
    	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
   	 
    	int hitpoints = battleAttack(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);   	 

   	 
        	return hitpoints;
	}    
    
	public static int goblinDefensive() {
    	System.out.println("You are facing a goblin!");
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
    	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
   	 
    
  	 
    	int hitpoints = battleDefensive(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);
   	 
   	 
    
    	return hitpoints;
	}
    	public static int orcsDefensive ()   {
    	System.out.println("You facing an orc!");
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
            	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
    	int hitPoints = battleDefensive(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);
    	return hitPoints;
	}
	public static int orcsAttack ()   {
    	System.out.println("You are facing an orc!");
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
            	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;
    	ehitPoints = battleAttack(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);
    	return ehitPoints;
	}
    	public static int skeletalDragonDefensive() {
        	System.out.println("You are facing a skeletalDragon!");
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
            	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;

    	int hitPoints = battleDefensive(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);
    	return hitPoints;
	}
	public static int skeletalDragonAttack() {
    	System.out.println("You are facing a skeletalDragon!");
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
            	int ehitPoints = (estrength*10)/4 + (estamina*10)/6;

    	ehitPoints = battleAttack(estrength, ehitPoints, eintelligence, eagility, estamina, echarisma);   	 
    	return ehitPoints;

    	 
	}


    
	public static int battleDefensive(int estrength,int ehitPoints,  int eintelligence, int eagility, int estamina, int echarisma)   {

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

        	System.out.println("The enemy's attack missed!");
    	}else if (echarmed<randyTwo)	{

        	System.out.println("You have been seduced by the enemy and have missed your opportunity to strike!");
    	}else  {
        	hitPoints = hitPoints - (emATK + epATK) + (int)((emATK + epATK)*defense/100);

        	System.out.println("The enemy's attack suceeded! You have lost " + ((emATK + epATK) -(int)((emATK + epATK)*defense/100)) + " hit points and you have " + hitPoints + " hitpoints left!");
       	 
               	 
   	 
	}
	return hitPoints;
    
    
}

	public static int battleAttack(int estrength, int ehitpoints, int eintelligence, int eagility, int estamina, int echarisma)   {
    	int randomizer = (int)((Math.random()*10)+1);
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
   	 
   	 
   	 
    	if (edodge<randy)	{
        	System.out.println("You have missed your attack!");
    	}else if (charmed<randyTwo)	{

        	System.out.println("Your enemy has become entranced by you and has missed their opportunity to attack");
    	}else  {
        	ehitpoints = ehitpoints - (mATK + pATK) + (int)((mATK + pATK)*defense/100);

        	System.out.println("Your attack succeeded! Your enemy lost " + ((mATK + pATK) -(int)((mATK + pATK)*edefense/100)) + " hit points and now has " + ehitpoints + " hitpoints left!");
       	 
       	 
   	 
	}
	return ehitpoints;
    
    
}



	//defaults
	public static int strength = 0, agility = 0, intelligence = 0, charisma = 0, stamina = 0,
        	points = 40, pointsToAdd = 0, attribute = 0;
	public static String strengthString = "strength", agilityString = "agility", intelligenceString = "intelligence",
        	charismaString = "charisma", staminaString = "stamina", humanString = "human", dwarfString = "dwarf",
        	trollString = "troll", elfString = "elf", unknownString = "mysterious";
	public static String speciesName = "none", charName = "Switzerland";
	public static Scanner scan = new Scanner(System.in);
	//BE CAREFUL THAT THESE DON'T GET REASSIGNED TO ENEMIES
    
	//changed all System.out.println to System.out.println
	//changed all scan.nextLine() to scan.nextLine()
	//private static GUI_project gui_project;
    
	public static void main(String args[])
	{   	 
    	character();
   	 
    	for(int i = 1; i<10;i++)	{
        	turn();
    	}
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
    
	//stats for goblin: weak
	public static void weakEnemy()
	{
    	System.out.println("You come upon a goblin!");
    	//random number between 2 and 7
    	strength = (int)(Math.random() * 4 + 3);
    	agility = (int)(1 / Math.random());
    	intelligence = (int)(1 / Math.random());
    	charisma = (int)(1 / Math.random());
    	stamina = (int)(1 / Math.random());
	}
    
	//stats for orc: mid
	public static void midEnemy()
	{
    	System.out.println("You come upon an enemy!");
    	//random number between 5 and 10
    	strength = (int)(Math.random() * 4 + 3);
    	agility = (int)(1 / Math.random());
    	intelligence = (int)(1 / Math.random());
    	charisma = (int)(1 / Math.random());
    	stamina = (int)(1 / Math.random());
	}
    
	//stats for skeletal dragon: strong
	public static void strongEnemy()
	{
    	System.out.println("You come upon a threatening enemy!");
    	//random number between 9 and 16  
    	strength = (int)(Math.random() * 4 + 3);
    	agility = (int)(1 / Math.random());
    	intelligence = (int)(1 / Math.random());
    	charisma = (int)(1 / Math.random());
    	stamina = (int)(1 / Math.random());
	}
    
	//stats for boss: so strong
	public static void bossEnemy()
	{
    	System.out.println("You come upon an extremely threatening enemy!");
    	//random number between 17 and 20
    	strength = (int)(Math.random() * 4 + 3);
    	agility = (int)(1 / Math.random());
    	intelligence = (int)(1 / Math.random());
    	charisma = (int)(1 / Math.random());
    	stamina = (int)(1 / Math.random());
	}
    
	//do a thing for the +40 or whatever
	public static void addToStats()
	{
    	//int points = 40;
    	//int pointsToAdd = 0;
   	 
    	while(points > 0)
    	{
        	System.out.println("\nYou have " + points + " points to spend as you wish.");
        	System.out.println("Your attributes: \nStrength: "+ strength + "\nAgility: " + agility + "\nIntelligence: " + intelligence
                    	+ "\nCharisma: " + charisma + "\nStamina: " + stamina);
       	 
        	//pick an attribute and add to it
        	System.out.println("Which attribute would you like to add to?");
        	String attributeToAddTo = scan.nextLine();
        	//int pointsToAdd = 0;
       	 
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
    	System.out.println("\n\n\n\n\n\n\nNow, " + charName + ", aren't you curious about your quest?");
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
        	//totalPoints -= pointsToAdd;
        	String catchThatLine = scan.nextLine();
    	}
    	points = totalPoints;
    	attribute = attributeInt;
	}
    

}
