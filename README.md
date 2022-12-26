# JavaInterview

---

### String - Frequency Map

#### a. Approach 1

```java
String s = "hello";
Map<Character,Integer> sMap = new HashMap<>();
for(char ch : s.toCharArray()) {
  sMap.put(ch, sMap.getOrDefault(ch, 0) + 1);
}
```

#### b. Approach 2

```java
String s = "hello";
Map<Character,Integer> sMap = s.chars()
                              .mapToObj(c -> (char)c)
                              .collect(Collectors
                              .groupingBy(Function.identity(), Collectors.summingInt(c -> 1)));
```

#### b. Approach 3

```java
String s = "hello";
Map<Character,Long> sMap = s.chars()
                              .mapToObj(c -> (char)c)
                              .collect(Collectors
                              .groupingBy(Function.identity(), Collectors.counting()));
```
