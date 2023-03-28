
**Recursive function** or **Recursion** is a function that calls itself inside its body, either directly or not.

## Anatomy of Recursion
A common pattern can be found in the body of many recursive functions. The body begins with a _base case_, a conditional statement that defines the behavior of the function for the inputs that are simplest to process. In the case of sum_digits, the base case is any single-digit argument, and we simply return that argument. Some recursive functions will have multiple base cases.

The base cases are then followed by one or more _recursive calls_. Recursive calls always have a certain character: they simplify the original problem. Recursive functions express computation by simplifying problems incrementally. For example, summing the digits of 7 is simpler than summing the digits of 73, which in turn is simpler than summing the digits of 738. For each subsequent call, there is less work left to be done.

Recursive functions often solve problems in a different way than the iterative approaches that we have used previously. Consider a function fact to compute n factorial, where for example fact(4) computes 4!=4⋅3⋅2⋅1=244!=4⋅3⋅2⋅1=24.

A natural implementation using a while statement accumulates the total by multiplying together each positive integer up to n.

```Python

>>> def fact_iter(n):
        total, k = 1, 1
        while k <= n:
            total, k = total * k, k + 1
        return total

>>> fact_iter(4)
24
```

## Sample Code - Factorial Recursion
```Java
class Main{
	static int fractorial (int n){
		if (n == 0 || n == 1)
			return 1;

		return n * factorial(n-1); //4! = 4*3 *2 *1 = 6
	}

	public static void main(String[] args){
		int ans = factorial(5);

		System.out.println("Factorial of 5 is:" + ans);
	}
}
```