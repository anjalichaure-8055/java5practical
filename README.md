# java5practical
class Practical{
    static int fact = 1;

    
    static int getFactorial1(int number) {
        int fact = 1;
        for (int i = 1; i <= number; i++) {
            fact = fact * i;
        }
        return fact;
    }

    
    static int getFactorial2(int number){
        int fact = 1;
        while (number != 0) {
            fact = fact * number;
            number--;
        }
        return fact;
    }

    
    static void calcFact(int no) {
        if (no > 1) {
            fact = fact * no;
            calcFact(no - 1);
        }
    }

    
    static int getSum(int n) {
        int sum = 0;
        while (n != 0) {
            sum = sum + n % 10;
            n = n / 10;
        }
        return sum;
    }

    
    static int sum(int[] arr, int n) {
        if (n <= 0) {
            return 0;
        }
        return sum(arr, n - 1) + arr[n - 1];
    }

    public static void main(String[] args) {
        
        int number = 5;
        System.out.println("Factorial of " + number + " using getFactorial1: " + getFactorial1(number));
        System.out.println("Factorial of " + number + " using getFactorial2: " + getFactorial2(number));

        
        int n = 87;
        System.out.println("Sum of digits of " + n + ": " + getSum(n));

        
        int[] arr = {12, 3, 4, 15};
        int arraySum = sum(arr, arr.length);
        System.out.println("Sum of array elements: " + arraySum);

        
        int no = 5;
        fact = 1;
        calcFact(no);
        System.out.println("Factorial of " + no + " using recursive calcFact: " + fact);
    }
}
