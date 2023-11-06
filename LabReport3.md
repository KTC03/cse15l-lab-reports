# Part I: Bugs
- failure inducing input:
```
@Test
  public void testReverseInPlace() {
    int[] arr = {1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(arr);
    int[] expected = {5, 4, 3, 2, 1};
    assertArrayEquals(expected, arr);
}
```

- input that does not induce failure:
```
@Test
public void testReverseInPlaceNoFailure() {
  int[] arr = {5, 4, 3, 2, 1};
  ArrayExamples.reverseInPlace(arr);
  int[] expected = {5, 4, 3, 2, 1};
  assertArrayEquals(expected, arr);
}
```



