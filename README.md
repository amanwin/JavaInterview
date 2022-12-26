# JavaInterview

---

### String - Frequency Map

```java
String s = "hello";
Map<Character,Integer> sMap = new HashMap<>();
for(char ch : s.toCharArray()) {
  sMap.put(ch, sMap.getOrDefault(ch, 0) + 1);
}
```
