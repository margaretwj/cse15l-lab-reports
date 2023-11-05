# **Lab Report 3** <br />
Margaret Jones <br />
Monday 4PM - 6PM <br />

## **PART 1 - ReverseInPlace Bug**
* **Failure inducing input:** the non-empty integer array {3, 4, 5, 6}
* Failure inducing test code:
  ```  @Test
  public void testReverseInPlace2() {
    int[] input2 = {3, 4, 5, 6};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{6, 5, 4, 3}, input2);
  }
  ```
* **Non-failure inducing input:** the non-empty integer array { 3 }
* Non-failure inducing test code:
  ``` 	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
  ```
* **Symptom:**
![Image](symptom_labreport3.png)

* **The bug:**
* Code before fixing the bug:
  ```
    static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) { 
      arr[i] = arr[arr.length - i - 1];
      }
    }
  ```
* Code after fixing the bug:
  ```
    static void reverseInPlace(int[] arr) {
    int num; //new
    for(int i = 0; i < arr.length/2; i += 1) { //arr.length/2 = new
      num = arr[i]; //new
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = num; //new
    }
    }
  ```
  

## **PART 2 - Researching Commands**
