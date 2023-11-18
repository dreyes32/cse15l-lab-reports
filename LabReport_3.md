## Part 1 : Bug Questions 
Choice of Bug : Array
```
 @Test
  public void testRevArr(){
    int[] arr = {1,0,1,0,-1,-1,-1,-1};
    ArrayExamples.reverseInPlace(arr);
    assertArrayEquals(new int[] {-1,-1,-1,-1,0,1,0,1}, arr);
  }
```
```
  @Test
  public void testRevArr2(){
    int[] arr = {1};
    ArrayExamples.reverseInPlace(arr);
    assertArrayEquals(new int[] {1}, arr);
  }
```
-  Passed Test ![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/23be0834-3396-427e-bdf1-3e5f44424f6a)
   Failed Test ![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/3a5bbc85-6460-4de6-be80-a8865dd53e45)
   #### Before 
   ```
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
   }
    ```

#### After
```
      static void reverseInPlaceChange(int[] arr) {
        int tempVal = 0;
        for(int i = 0; i < arr.length/2; i += 1) {
          tempVal = arr[i];
          arr[i] = arr[arr.length - i - 1]; 
          arr[arr.length - i - 1] = tempVal;
        }
      }
```
## Part 2 : Researching Commands
Choice of command : Find 
4 Interesting Command Line Options :

- You can use find + -exec, when wanting to delete all files of a certain "." type:
```
  find /path/to/search -name "*.tmp" -exec rm {} \;
```
The output would just be the deletion of all specified files.
-  You can find files that have been modified wihtin a specified time (days) :
```
find /path/to/search -type f -mtime -7
```
The output would consists of all files that have been modified within specified time 
-  You can find file names that have a number attached to them :
```
find /path/to/search -type f -regex '.*file[0-9]+$'
```
The output would consists of all file names with specified range of numbers
-  You can find directories or other objects aside from files that are within a folder :
```
find /path/to/search -type d
```
The output would consists of all object types that were specified

-name + find examples : 
```
find ./technical -type f -name "biomed.txt"
```
**Explanation : This would find all biomed files that is within the techincal directory, useful in finding specfic files of a category or topic**
**Output : \
./technical/biomed.txt**
```
 find . -type f -name "*.py"
```
**Explanation : This command would find all python script files within the current directory, useful when needing to obtain files of a different language, as it isnt just python that works**\
**Output : if there does exists a file\
./folder1/example.py**
```
find /var/www -type d -name "images"
```
**Explanation : This command would find all directories that hold images, useful when trying to find a specific image catergorized**
**Output : if there exists a directory with that name\
/var/www/example/images**
```
find ./technical -type d -name "*backup*"
```
**Explanation : This command would find all backup directories, useful when needing to retrieve a backup incase the main directory gets messy or error filled**\
**Output : if there exists a directory with that name\
./technical/backup**

-  ## Citing Sources
-  ChatGpt: Prompt: What are some command line options for find & How to use -name + find of a \technical directory






