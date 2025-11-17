# restaurant-billing-system
import java.util.*;

class Dish {
    String name;
    double price;

    Dish(String name, double price) {
        this.name = name;
        this.price = price;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter number of dishes:");
        int n = sc.nextInt();
        sc.nextLine();
        Dish[] dishes = new Dish[n];
        double total=0;
        for (int i = 0; i < n; i++) {
            System.out.println("Enter dish name:");
            String name = sc.nextLine();
            System.out.println("Enter dish price:");
            double price = sc.nextDouble();
            sc.nextLine();
            dishes[i] = new Dish(name, price);
            total+=price;
        }

        System.out.println("\n------- Restaurant Menu -------");
        for (int i = 0; i < n; i++) {
            System.out.println((i + 1) + ". " + dishes[i].name + " - Rs."+dishes[i].price);
        }
        System.out.println("total:"+total);
        sc.close();
    }
}
