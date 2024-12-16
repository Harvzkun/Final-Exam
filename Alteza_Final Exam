import java.util.Stack;

public class Mythical_Creature {
    // Creature class to store name and power level
    static class Creature {
        String name;
        int powerLevel;

        Creature(String name, int powerLevel) {
            this.name = name;
            this.powerLevel = powerLevel;
        }
    }

    public static void main(String[] args) {
        // creatures name and powerlevel
        Creature[] creatures = {
            new Creature("Dragon", 95),
            new Creature("Griffin", 88),
            new Creature("Unicorn", 78),
            new Creature("Phoenix", 92),
            new Creature("Centaur", 85)
        };

        // Bubble Sort in descending order
        bubbleSortDescending(creatures);
        System.out.println("*** Bubble Sort: Descending Order by Power Level ***");
        displayCreatures(creatures);

        // Selection Sort in ascending order
        selectionSortAscending(creatures);
        System.out.println("\n*** Selection Sort: Ascending Order by Power Level ***");
        displayCreatures(creatures);

        // Stack Implementation
        Stack<Creature> stack = new Stack<>();
        for (Creature creature : creatures) {
            stack.push(creature);
        }
        System.out.println("\n*** Stack Implementation: Popping Creatures ***");
        while (!stack.isEmpty()) {
            Creature creature = stack.pop();
            System.out.println("Popped: " + creature.name + " - " + creature.powerLevel);
        }
    }

    // Bubble Sort in descending order
    public static void bubbleSortDescending(Creature[] creatures) {
        int n = creatures.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (creatures[j].powerLevel < creatures[j + 1].powerLevel) {
                    // Swap creatures[j] and creatures[j + 1]
                    Creature temp = creatures[j];
                    creatures[j] = creatures[j + 1];
                    creatures[j + 1] = temp;
                }
            }
        }
    }

    // Selection Sort in ascending order
    public static void selectionSortAscending(Creature[] creatures) {
        int n = creatures.length;
        for (int i = 0; i < n - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (creatures[j].powerLevel < creatures[minIndex].powerLevel) {
                    minIndex = j;
                }
            }
            // Swap creatures[minIndex] and creatures[i]
            Creature temp = creatures[minIndex];
            creatures[minIndex] = creatures[i];
            creatures[i] = temp;
        }
    }

    // Display creatures
    public static void displayCreatures(Creature[] creatures) {
        for (Creature creature : creatures) {
            System.out.println(creature.name + " - " + creature.powerLevel);
        }
    }
}
