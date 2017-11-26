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

```
public static string CreatePhoneNumber(int[] numbers)
{
    return $@"({numbers[0]}{numbers[1]}{numbers[2]}) {numbers[3]}{numbers[4]}{numbers[5]}-{numbers[6]}{numbers[7]}{numbers[8]}                  {numbers[9]}";
}

public static string CreatePhoneNumber(int[] numbers) =>
    new Regex("(...)(...)(....)").Replace(String.Concat(numbers), "($1) $2-$3");

public static string CreatePhoneNumber(int[] numbers)
   => String.Format("({0}) {1}-{2}",
     numbers.Take(3).Select(n => n.ToString()).Aggregate((a, b) => a + b),
     numbers.Skip(3).Take(3).Select(n => n.ToString()).Aggregate((a, b) => a + b),
     numbers.Skip(6).Take(4).Select(n => n.ToString()).Aggregate((a, b) => a + b));
```

```
public static string Rgb(int r, int g, int b)
{
    r = Math.Max(0, Math.Min(255, r));
    g = Math.Max(0, Math.Min(255, g));
    b = Math.Max(0, Math.Min(255, b));

    return r.ToString("X2") + g.ToString("X2") + b.ToString("X2");
}
```
