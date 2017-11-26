# CodeSinppets

'''
var ints = numbers.Split(' ').Select(int.Parse).ToList();
var unique = ints.GroupBy(n => n % 2).OrderBy(c => c.Count()).First().First();
return ints.FindIndex(c => c == unique) + 1;
