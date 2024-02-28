# Lab Report 3: Bugs and Commands

# Part 1: Bugs
-A failure-inducing input using the reversed method.
```
 @Test
  public void testReversedFailure() {
    int[] input = { 1, 2, 3, 4, 5 };
    int[] expected = { 5, 4, 3, 2, 1};
    int[] result = ArrayExamples.reversed(input);
    assertArrayEquals(expected, result);
  }
```

-An input that doesn't induce a failure.
```
 @Test
  public void testReversedNoFailure() {
    int[] input = { 1, 2, 3, 4, 5 };
    int[] expected = { 1, 2, 3, 4, 5};
    int[] result = ArrayExamples.reversed(input);
    assertArrayEquals(expected, result);
  }
```

-The symptom, as the output of running tests.

<img width="785" alt="lab3" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/308f574a-16b0-4538-9a94-e7a8cc45667c">





-The bug,before and after.
# Before:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
```

# After:
    
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

_ The bug here was that the method `reversed` does not assign the values from the `arr` array in the correct array. So instead we put the values into the `newArray` with the elements of the `arr` array in reversed order. 

# Part 2: Researching Commands

# `find` command

# -OPTION #1 `-name`:

# Source:
https://tecadmin.net/linux-find-command-with-examples/

# EXAMPLE 1:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical -name "911report" 
./technical/911report
adey@Adeys-MacBook-Pro docsearch % 
```


# EXAMPLE 2:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical -type f  -name "chapter-1.txt"
./technical/911report/chapter-1.txt
adey@Adeys-MacBook-Pro docsearch % 
```


# -OPTION #2 `-type`:

# Source:
https://tecadmin.net/linux-find-command-with-examples/

# EXAMPLE 1:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical -type d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```

# EXAMPLE 2:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical/plos -type f
./technical/plos/pmed.0020273.txt
./technical/plos/journal.pbio.0030032.txt
./technical/plos/pmed.0020065.txt
./technical/plos/pmed.0020071.txt
./technical/plos/pmed.0020059.txt
./technical/plos/pmed.0010039.txt
./technical/plos/journal.pbio.0020354.txt
./technical/plos/pmed.0010010.txt
./technical/plos/journal.pbio.0020156.txt
./technical/plos/pmed.0020104.txt
./technical/plos/pmed.0020272.txt
./technical/plos/pmed.0020258.txt
./technical/plos/pmed.0020099.txt
./technical/plos/journal.pbio.0020140.txt
./technical/plos/journal.pbio.0020183.txt
./technical/plos/journal.pbio.0020430.txt
./technical/plos/journal.pbio.0020394.txt
./technical/plos/journal.pbio.0020431.txt
./technical/plos/journal.pbio.0020419.txt

```
-The output was longer but I cut it short for the report.

# -OPTION #3 '-size`:

# Source:
https://tecadmin.net/linux-find-command-with-examples/

# -EXAMPLE 1:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical -size +100k
./technical/government/About_LSC/commission_report.txt
./technical/government/About_LSC/State_Planning_Report.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/ctm4-10.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Gen_Account_Office/d0269g.txt
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
./technical/government/Gen_Account_Office/d01376g.txt
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/pe1019.txt
./technical/government/Gen_Account_Office/gg96118.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/government/Gen_Account_Office/im814.txt
./technical/government/Gen_Account_Office/ai9868.txt
./technical/government/Gen_Account_Office/May1998_ai98068.txt
./technical/government/Gen_Account_Office/d02701.txt
./technical/biomed/1471-2105-3-2.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-12.txt
adey@Adeys-MacBook-Pro docsearch % 
```


# -EXAMPLE 2:

```
adey@Adeys-MacBook-Pro docsearch % find ./technical/biomed  -size +100k
./technical/biomed/1471-2105-3-2.txt
adey@Adeys-MacBook-Pro docsearch %
```

# -OPTION #4 '-regex`:

Source:
https://tecadmin.net/linux-find-command-with-examples/

-EXAMPLE 1:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical/biomed -regex ".*/1476[^/]*$"
./technical/biomed/1476-069X-2-4.txt
./technical/biomed/1476-4598-2-22.txt
./technical/biomed/1476-4598-1-8.txt
./technical/biomed/1476-0711-2-7.txt
./technical/biomed/1476-069X-2-7.txt
./technical/biomed/1476-4598-2-20.txt
./technical/biomed/1476-069X-2-2.txt
./technical/biomed/1476-4598-2-25.txt
./technical/biomed/1476-4598-2-24.txt
./technical/biomed/1476-0711-2-3.txt
./technical/biomed/1476-072X-2-4.txt
./technical/biomed/1476-069X-1-3.txt
./technical/biomed/1476-072X-2-3.txt
./technical/biomed/1476-4598-2-3.txt
./technical/biomed/1476-4598-2-2.txt
./technical/biomed/1476-511X-1-2.txt
./technical/biomed/1476-5918-1-2.txt
./technical/biomed/1476-4598-2-1.txt
./technical/biomed/1476-4598-1-3.txt
./technical/biomed/1476-511X-2-3.txt
./technical/biomed/1476-4598-2-28.txt
./technical/biomed/1476-511X-2-2.txt
./technical/biomed/1476-4598-1-5.txt
./technical/biomed/1476-9433-1-2.txt
./technical/biomed/1476-069X-2-9.txt
./technical/biomed/1476-9433-1-3.txt
./technical/biomed/1476-4598-1-6.txt
adey@Adeys-MacBook-Pro docsearch %
```



-EXAMPLE 2:
```
adey@Adeys-MacBook-Pro docsearch % find ./technical -type d -regex ".*/g[^/]*"
./technical/government
adey@Adeys-MacBook-Pro docsearch %
```
