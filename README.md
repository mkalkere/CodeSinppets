# CodeSinppets


```
var ints = numbers.Split(' ').Select(int.Parse).ToList();
var unique = ints.GroupBy(n => n % 2).OrderBy(c => c.Count()).First().First();
return ints.FindIndex(c => c == unique) + 1;
```


```
public static bool IsPrime(int n)
        {
            if (n < 1) return false;
            if (n == 2) return true;
            if (n % 2 == 0) return false;

            int limit =Convert.ToInt32(Math.Floor(Math.Sqrt(n)));

            for (int i = 3; i <= limit; i+=2)
            {
                if (n % i == 0) return false;
            }

            return true;
        }
```
