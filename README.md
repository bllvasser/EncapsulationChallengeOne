# EncapsulationChallengeOne
package academy.learnprogrmming;

public class Main {

static class Printer{
    private int tonerLevel = 100;
    private int numberOfPagesPrinted;
    private boolean isDuplexPrinter;

    public Printer(int tonerLevel, int numberOfPagesPrinted, boolean isDuplexPrinter){
        this.isDuplexPrinter = isDuplexPrinter;
        if(isDuplexPrinter == true){
            System.out.println("The printer can print on both sides");
        } else if (isDuplexPrinter != true){
            System.out.println("The printer cannot print on both sides");
        }
        this.numberOfPagesPrinted = numberOfPagesPrinted;
       // this.tonerLevel = 100;
    }

    public void fillUpToner(int tonerAmount){
        if(tonerAmount >= 75 || tonerAmount <= 100){
            this.tonerLevel = tonerAmount;
            System.out.println("Toner levels are at 75% to 100%");
        } else if(tonerAmount <= 74){
            System.out.println("Toner Levels are below 75%");
        }

        else if(tonerAmount <0){
            System.out.println("Add Toner");
        } else if (tonerAmount > 100) {
            System.out.println("Too much Toner");
        }
    }
    public void printingPage(int pages){
        if (pages < 1){
            System.out.println(" Getting ready to print");
            pages ++;
        }
    }



    public int getTonerLevel() {
        return tonerLevel;
    }

    public int getNumberOfPagesPrinted() {
        return numberOfPagesPrinted;
    }

    public boolean isDuplexPrinter() {
        return isDuplexPrinter;
    }
}

    public static void main(String[] args) {

    Printer printer = new Printer(-1,10,true);

    printer.fillUpToner(150);

    printer.printingPage(0);

    }
}

"C:\Program Files\Java\jdk-15.0.1\bin\java.exe" "-javaagent:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\lib\idea_rt.jar=53929:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\bin" -Dfile.encoding=UTF-8 -classpath C:\Users\nadiy\IdeaProjects\EncapsulationChallenge\out\production\EncapsulationChallenge academy.learnprogrmming.Main
The printer can print on both sides
Toner levels are at 75% to 100%
 Getting ready to print

Process finished with exit code 0
