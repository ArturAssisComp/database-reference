<a name="readme-top"></a>

[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/ArturAssisComp/ctest.git">
  </a>

  <h3 align="center">CTEST</h3>

  <p align="center">
    An unit test lib for C.
    <br />
    <a href="#documentation"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/ArturAssisComp/ctest/issues">Report Bug</a>
    ·
    <a href="https://github.com/ArturAssisComp/ctest/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#description">Description</a></li>
    <li><a href="#how-is-a-contribution-made">How to contribute</a></li>
    <li><a href="#requirements">Requirements</a></li>
    <li><a href="#how-to-use-the-makefile">How to use the makefile</a></li>
    <li>
      <a href="#how-to-use-ctest-in-other-projects">Using ctest</a>
      <ul>
        <li><a href="#example-of-usage">Example</a></li>
      </ul>
    </li>
    <li>
      <a href="#documentation">Documentation</a>
      <ul>
	<details>
          <summary>index</summary>
          <li><a href="#overview">Overview</a></li>
	      <li><a href="#types">Types</a></li>
	      <li><a href="#variables">Variables</a></li>
          <li><a href="#constants">Constants</a></li>
          <li><a href="#functions">Functions</a></li>
	      <ul>
              <li><a href="#single-data-types">Single data types</a></li>
	              <ul>
                       <li><a href="#unsigned_integer">unsigned_integer</a></li>
			   <ul>
                               <li><a href="#assert_unsigned_integer_equal">assert_unsigned_integer_equal</a></li>
                               <li><a href="#assert_unsigned_integer_notequal">assert_unsigned_integer_notEqual (implement)</a></li>
                               <li><a href="#assert_unsigned_integer_greater">assert_unsigned_integer_greater (implement)</a></li>
                               <li><a href="#assert_unsigned_integer_greaterequal">assert_unsigned_integer_greaterEqual (implement)</a></li>
                               <li><a href="#assert_unsigned_integer_less">assert_unsigned_integer_less (implement)</a></li>
                               <li><a href="#assert_unsigned_integer_lessequal">assert_unsigned_integer_lessEqual (implement)</a></li>
                               <li><a href="#assert_unsigned_integer_bitmaskequal">assert_unsigned_integer_bitMaskEqual (implement)</a></li>
                           </ul>
                       <li><a href="#integer">integer</a></li>
			   <ul>
                               <li><a href="#assert_integer_equal">assert_integer_equal (implement)</a></li>
                               <li><a href="#assert_integer_notequal">assert_integer_notEqual (implement)</a></li>
                               <li><a href="#assert_integer_greater">assert_integer_greater (implement)</a></li>
                               <li><a href="#assert_integer_greaterequal">assert_integer_greaterEqual (implement)</a></li>
                               <li><a href="#assert_integer_less">assert_integer_less (implement)</a></li>
                               <li><a href="#assert_integer_lessequal">assert_integer_lessEqual (implement)</a></li>
                           </ul>
                       <li><a href="#floating_point">floating_point</a></li>
			   <ul>
                               <li><a href="#assert_floating_point_almostequal">assert_floating_point_almostEqual (implement)</a></li>
                               <li><a href="#assert_floating_point_notalmostequal">assert_floating_point_notAlmostEqual (implement)</a></li>
                               <li><a href="#assert_floating_point_greater">assert_floating_point_greater (implement)</a></li>
                               <li><a href="#assert_floating_point_greaterequal">assert_floating_point_greaterEqual (implement)</a></li>
                               <li><a href="#assert_floating_point_less">assert_floating_point_less (implement)</a></li>
                               <li><a href="#assert_floating_point_lessequal">assert_floating_point_lessEqual (implement)</a></li>
                           </ul>
                       <li><a href="#bool">bool</a></li>
			   <ul>
                               <li><a href="#assert_bool_equal">assert_bool_equal (implement)</a></li>
                               <li><a href="#assert_bool_notequal">assert_bool_notEqual (implement)</a></li>
                               <li><a href="#assert_bool_true">assert_bool_true (implement)</a></li>
                               <li><a href="#assert_bool_false">assert_bool_false (implement)</a></li>
                           </ul>
                       <li><a href="#char">char</a></li>
			   <ul>
                               <li><a href="#assert_char_equal">assert_char_equal (implement)</a></li>
                               <li><a href="#assert_char_notequal">assert_char_notEqual (implement)</a></li>
                               <li><a href="#assert_char_greater">assert_char_greater (implement)</a></li>
                               <li><a href="#assert_char_greaterequal">assert_char_greaterEqual (implement)</a></li>
                               <li><a href="#assert_char_less">assert_char_less (implement)</a></li>
                               <li><a href="#assert_char_lessequal">assert_char_lessEqual (implement)</a></li>
                           </ul>
                       <li><a href="#file">file</a></li>
			   <ul>
                               <li><a href="#assert_files_binarycontentequal">assert_files_binaryContentEqual (implement)</a></li>
                               <li><a href="#assert_files_contentequal">assert_files_contentEqual (implement)</a></li>
                               <li><a href="#assert_file_path_contentequal">assert_file_path_contentEqual (implement)</a></li>
                           </ul>
                       <li><a href="#void-pointer">Void pointer</a></li>
			   <ul>
                               <li><a href="#assert_pointer_isnull">assert_pointer_isNULL (implement)</a></li>
                               <li><a href="#assert_pointer_notisnull">assert_pointer_notIsNULL (implement)</a></li>
                           </ul>
                      </ul>
              <li><a href="#array-data-types">Array data type</a></li>
	              <ul>
                       <li><a href="#unsigned_integerarray">unsigned_integerArray</a></li>
			   <ul>
                               <li><a href="#assert_unsigned_integerarray_equal">assert_unsigned_integerArray_equal (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notequal">assert_unsigned_integerArray_notEqual (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_sorted">assert_unsigned_integerArray_sorted (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notsorted">assert_unsigned_integerArray_notSorted (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_permutation">assert_unsigned_integerArray_permutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notpermutation">assert_unsigned_integerArray_notPermutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_ispartialpermutation">assert_unsigned_integerArray_isPartialPermutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notispartialpermutation">assert_unsigned_integerArray_notIsPartialPermutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_haspartialpermutation">assert_unsigned_integerArray_hasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_nothaspartialpermutation">assert_unsigned_integerArray_notHasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_setequal">assert_unsigned_integerArray_setEqual (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_setin">assert_unsigned_integerArray_setIn (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notsetin">assert_unsigned_integerArray_notSetIn (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_sethas">assert_unsigned_integerArray_setHas (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notsethas">assert_unsigned_integerArray_notSetHas (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_issubarray">assert_unsigned_integerArray_isSubarray (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_notissubarray">assert_unsigned_integerArray_notIsSubarray (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_hassubarray">assert_unsigned_integerArray_hasSubarray (implement)</a></li>
                               <li><a href="#assert_unsigned_integerarray_nothassubarray">assert_unsigned_integerArray_notHasSubarray (implement)</a></li>
                           </ul>
                       <li><a href="#integerarray">integerArray</a></li>
			   <ul>
                               <li><a href="#assert_integerarray_equal">assert_integerArray_equal (implement)</a></li>
                               <li><a href="#assert_integerarray_notequal">assert_integerArray_notEqual (implement)</a></li>
                               <li><a href="#assert_integerarray_sorted">assert_integerArray_sorted (implement)</a></li>
                               <li><a href="#assert_integerarray_notsorted">assert_integerArray_notSorted (implement)</a></li>
                               <li><a href="#assert_integerarray_permutation">assert_integerArray_permutation (implement)</a></li>
                               <li><a href="#assert_integerarray_notpermutation">assert_integerArray_notPermutation (implement)</a></li>
                               <li><a href="#assert_integerarray_ispartialpermutation">assert_integerArray_isPartialPermutation (implement)</a></li>
                               <li><a href="#assert_integerarray_notispartialpermutation">assert_integerArray_notIsPartialPermutation (implement)</a></li>
                               <li><a href="#assert_integerarray_haspartialpermutation">assert_integerArray_hasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_integerarray_nothaspartialpermutation">assert_integerArray_notHasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_integerarray_setequal">assert_integerArray_setEqual (implement)</a></li>
                               <li><a href="#assert_integerarray_setin">assert_integerArray_setIn (implement)</a></li>
                               <li><a href="#assert_integerarray_notsetin">assertd_integerArray_notSetIn (implement)</a></li>
                               <li><a href="#assert_integerarray_sethas">assert_integerArray_setHas (implement)</a></li>
                               <li><a href="#assert_integerarray_notsethas">assert_integerArray_notSetHas (implement)</a></li>
                               <li><a href="#assert_integerarray_issubarray">assert_integerArray_isSubarray (implement)</a></li>
                               <li><a href="#assert_integerarray_notissubarray">assert_integerArray_notIsSubarray (implement)</a></li>
                               <li><a href="#assert_integerarray_hassubarray">assert_integerArray_hasSubarray (implement)</a></li>
                               <li><a href="#assert_integerarray_nothassubarray">assert_integerArray_notHasSubarray (implement)</a></li>
                           </ul>
                       <li><a href="#boolarray">boolArray</a></li>
			   <ul>
                               <li><a href="#assert_boolarray_equal">assert_boolArray_equal (implement)</a></li>
                               <li><a href="#assert_boolarray_alltrue">assert_boolArray_allTrue (implement)</a></li>
                               <li><a href="#assert_boolarray_anyfalse">assert_boolArray_anyFalse (implement)</a></li>
                               <li><a href="#assert_boolarray_allfalse">assert_boolArray_allFalse (implement)</a></li>
                               <li><a href="#assert_boolarray_anytrue">assert_boolArray_anyTrue (implement)</a></li>
                           </ul>
                       <li><a href="#chararray">charArray</a></li>
			   <ul>
                               <li><a href="#assert_chararray_equal">assert_charArray_equal (implement)</a></li>
                               <li><a href="#assert_chararray_notequal">assert_charArray_notEqual (implement)</a></li>
                               <li><a href="#assert_chararray_sorted">assert_charArray_sorted (implement)</a></li>
                               <li><a href="#assert_chararray_notsorted">assert_charArray_notSorted (implement)</a></li>
                               <li><a href="#assert_chararray_permutation">assert_charArray_permutation (implement)</a></li>
                               <li><a href="#assert_chararray_notpermutation">assert_charArray_notPermutation (implement)</a></li>
                               <li><a href="#assert_chararray_ispartialpermutation">assert_charArray_isPartialPermutation (implement)</a></li>
                               <li><a href="#assert_chararray_notispartialpermutation">assert_charArray_notIsPartialPermutation (implement)</a></li>
                               <li><a href="#assert_chararray_haspartialpermutation">assert_charArray_hasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_chararray_nothaspartialpermutation">assert_charArray_notHasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_chararray_setequal">assert_charArray_setEqual (implement)</a></li>
                               <li><a href="#assert_chararray_setin">assert_charArray_setIn (implement)</a></li>
                               <li><a href="#assert_chararray_notsetin">assertd_charArray_notSetIn (implement)</a></li>
                               <li><a href="#assert_chararray_sethas">assert_charArray_setHas (implement)</a></li>
                               <li><a href="#assert_chararray_notsethas">assert_charArray_notSetHas (implement)</a></li>
                               <li><a href="#assert_chararray_issubarray">assert_charArray_isSubarray (implement)</a></li>
                               <li><a href="#assert_chararray_notissubarray">assert_charArray_notIsSubarray (implement)</a></li>
                               <li><a href="#assert_chararray_hassubarray">assert_charArray_hasSubarray (implement)</a></li>
                               <li><a href="#assert_chararray_nothassubarray">assert_charArray_notHasSubarray (implement)</a></li>
                           </ul>
                       <li><a href="#string">string</a></li>
			   <ul>
                               <li><a href="#assert_string_equal">assert_string_equal (implement)</a></li>
                               <li><a href="#assert_string_notequal">assert_string_notEqual (implement)</a></li>
                               <li><a href="#assert_string_greater">assert_string_greater (implement)</a></li>
                               <li><a href="#assert_string_greaterequal">assert_string_greaterEqual (implement)</a></li>
                               <li><a href="#assert_string_less">assert_string_less (implement)</a></li>
                               <li><a href="#assert_string_lessequal">assert_string_lessEqual (implement)</a></li>
                               <li><a href="#assert_string_sizeequal">assert_string_sizeEqual (implement)</a></li>
                               <li><a href="#assert_string_notsizeequal">assert_string_notSizeEqual (implement)</a></li>
                               <li><a href="#assert_string_sizegreater">assert_string_sizeGreater (implement)</a></li>
                               <li><a href="#assert_string_sizegreaterequal">assert_string_sizeGreaterEqual (implement)</a></li>
                               <li><a href="#assert_string_sizeless">assert_string_sizeLess (implement)</a></li>
                               <li><a href="#assert_string_sizelessequal">assert_string_sizeLessEqual (implement)</a></li>
                               <li><a href="#assert_string_samesize">assert_string_sameSize (implement)</a></li>
                               <li><a href="#assert_string_haschar">assert_string_hasChar (implement)</a></li>
                               <li><a href="#assert_string_nothaschar">assert_string_notHasChar (implement)</a></li>
                               <li><a href="#assert_string_sorted">assert_string_sorted (implement)</a></li>
                               <li><a href="#assert_string_notsorted">assert_string_notSorted (implement)</a></li>
                               <li><a href="#assert_string_permutation">assert_string_permutation (implement)</a></li>
                               <li><a href="#assert_string_notpermutation">assert_string_notPermutation (implement)</a></li>
                               <li><a href="#assert_string_ispartialpermutation">assert_string_isPartialPermutation (implement)</a></li>
                               <li><a href="#assert_string_notispartialpermutation">assert_string_notIsPartialPermutation (implement)</a></li>
                               <li><a href="#assert_stringy_haspartialpermutation">assert_string_hasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_string_nothaspartialpermutation">assert_string_notHasPartialPermutation (implement)</a></li>
                               <li><a href="#assert_string_setequal">assert_string_setEqual (implement)</a></li>
                               <li><a href="#assert_string_setin">assert_string_setIn (implement)</a></li>
                               <li><a href="#assert_string_notsetin">assertd_string_notSetIn (implement)</a></li>
                               <li><a href="#assert_string_sethas">assert_string_setHas (implement)</a></li>
                               <li><a href="#assert_string_notsethas">assert_string_notSetHas (implement)</a></li>
                               <li><a href="#assert_string_issubarray">assert_string_isSubarray (implement)</a></li>
                               <li><a href="#assert_string_notissubarray">assert_string_notIsSubarray (implement)</a></li>
                               <li><a href="#assert_string_hassubarray">assert_string_hasSubarray (implement)</a></li>
                               <li><a href="#assert_string_nothassubarray">assert_string_notHasSubarray (implement)</a></li>
                               <li><a href="#assert_string_epmty">assert_string_empty (implement)</a></li>
                               <li><a href="#assert_string_notempty">assert_string_notEmpty (implement)</a></li>
                           </ul>
                  </ul>
          </ul>
          <li><a href="#macros">Macros</a></li>
	</details>
      </ul>
    </li>

  </ol>
</details>



<p align="right">(<a href="#readme-top">back to top</a>)</p>






# Description 

This repository contains a library that can be used to implement unit tests for C code.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# How is a contribution made?

1. Create a branch from an issue;
2. Clone the repository: 
```bash
git clone  https://github.com/ArturAssisComp/ctest.git
```
3. Change to the desired branch: 
```bash
cd ctest
git checkout <branch-name>
```
4. For each meaningful change, make a commit;

-> Fist, add the files that were changed: 
```bash
git add <filename1> <filename2> ... <filenameN>
```
-> Commit the changes: 
```bash
git commit -m "Implemented function foo()"
```
5. Push the changes: 
```bash
git push origin <name-of-the-branch>
```
6. If more changes are necessary, go to 4. Else,
   go to 7;
7. Create a pull request and assign someone to review the changes
   that were made in the branch;

=> Other useful commands:

Check the history of commits
```bash
git log
```
Check the status of the repository
```bash
git status
```
Get changes from remote repository from branch master
```bash
git pull origin <master-branch-name>
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# Requirements

make       4.3

gcc        11.2.0

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# How to use the makefile?

Run the following command in the terminal in the root directory of the ctest project:
```bash
make
```  
The headers, object files, and archive lib object will be saved into ./build/ folder. 
They may be used to implement unit tests using ctest lib in other projects.

To clean ./build/ folder, run:
```bash
make clean
```

In order to run all tests:
```bash
make test
```
or, to print the results to txt files in ./build/test_results/
```bash
make test_to_txt
```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

# How to use ctest in other projects?

Run the command make from the ctest base directory:
```bash
make
```  
then, the headers and the archive ctest.a files will be created and saved 
into the folder ./build/ctest_lib/

The files are organized as follows:

headers --> ./build/ctest_lib/include/

ctest.a --> ./build/ctest_lib/lib/

In order to use the library, the user must copy the content from ctest_lib 
to the desired folder in the target project, import the header ctest.h, and 
compile the file with the unit tests using as input, among others, the 
ctest.a object file.

## Example of usage
Let us suppose that the base directory for ctest is CTEST_BASE_DIR and the 
base directory for the target project, in which the unit tests will be 
implemented, is BASE_DIR. In an actual case, it is necessary to exchange
BASE_DIR and CTEST_BASE_DIR to the respective actual directory name.

1 - Execute the make command from CTEST_BASE_DIR:

```bash
cd CTEST_BASE_DIR
```  

```bash
make
```  

2 - Copy the folder CTEST_BASE_DIR/build/ctest_lib and its contents to the
target project:
```bash
cp -r CTEST_BASE_DIR/build/ctest_lib BASE_DIR/
```  

3 - Create the unit test file with name unit_test.c:
```C
//C file that implements the unit tests
#include "ctest_lib/include/ctest.h"


#define MSG_SIZE 100

int add(int a, int b)
{
    return a + b;
}

int main(void)
{
	char suite_name[] = "Unit test";
	char suite_description[] = "Basic test case.";
	char *functions_tested[] = {
        "add",
		NULL
	};
	char error_msg[MSG_SIZE] = "";
	char msg[MSG_SIZE] = ""; 


	//------------------------------------------------------------------------------
	start_suite(suite_name, suite_description, functions_tested);
		//------------------------------------------------------------------------------
		start_module("EDGE CASES", "Module for testing edge cases.", functions_tested);
            /* 0 + 0 */
            assert_integer_equal(add(0, 0), 0, __LINE__, "add(0, 0) == 0");
            /*------*/
            /* -1 + 0 */
            assert_integer_equal(add(-1, 0), -1, __LINE__, "add(-1, 0) == -1");
            /*------*/
            /* -1 + 1 */
            assert_integer_equal(add(-1, 1), 0, __LINE__, "add(-1, 1) == 0");
            /*------*/
            /* 1 + 1 */
            assert_integer_equal(add(1, 1), 2, __LINE__, "add(1, 1) == 2");
            /*------*/
            /* -1 + 2 */
            assert_integer_equal(add(-1, 2), 1, __LINE__, "add(-1, 2) == 1");
            /*------*/    
		end_module();
		//------------------------------------------------------------------------------
    		//------------------------------------------------------------------------------
		start_module("Domain CASES", "Module for testing domain cases.", functions_tested);
            /* 123 + 44 */
            assert_integer_equal(add(123, 44), 167, __LINE__, "add(123, 44) == 167");
            /*------*/
            /* -14 + 10 */
            assert_integer_equal(add(-14, 10), -4, __LINE__, "add(-14, 10) == -4");
            /*------*/ 
		end_module();
		//------------------------------------------------------------------------------
        
		
	end_suite();
	//------------------------------------------------------------------------------
}
```

4 - Compile the unit test file and execute it:
```bash
cd BASE_DIR
``` 

```bash
gcc -o unit_test unit_test.c ctest_lib/lib/ctest.a
```  

5 - Execute unit_test and check the results:
```bash
unit_test
``` 
<p align="right">(<a href="#readme-top">back to top</a>)</p>


# Documentation

## Overview
- ***About assert functions***: every assert function has the signature in the following format: 

***void assert_\<type\>_\<description\>(..., int line_number, char custom_message[])***. 

\<type\> describes the type of the target that will be used in the assertion process. \<description\> specify the type of assertion that will be made. As an example, \<type\> may be ***integer*** and \<description\> may be ***equal***, resulting in ***assert_integer_equal***. 

***line_number*** and ***custom_message*** are useful for printing meaningful failure messages. It is recommended to use the macro ***\_\_LINE\_\_*** as the input ***line_number***. ***custom_message*** may be NULL if no custom message will be used for failure message. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Types

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Variables

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Constants

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Functions

### Single data types

#### unsigned_integer

##### assert_unsigned_integer_equal
- Signature: 
```C
void assert_unsigned_integer_equal (unsigned_integer target, unsigned_integer reference, int line_number, char custom_message[]);
```
- Description: this function checks if the unsigned_integer ***target*** is equal to the unsigned_integer ***reference***.
<details> 
	<summary>Example</summary> 
<pre><code>#include "ctest_lib/include/ctest.h"
int main(void)
{
    char *functions_tested[] = { "None", NULL };
    start_suite("Unit test", "Basic test case.", functions_tested);
        start_module("Success module", "Basic test case.", functions_tested);
            assert_unsigned_integer_equal(2, 2, __LINE__, NULL); //pass
        end_module();	
        start_module("Fail module", "Basic test case.", functions_tested);
            assert_unsigned_integer_equal(0, 2, __LINE__, NULL); //fail
        end_module();	
    end_suite();
}</code></pre>
</details>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### integer

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### floating_point


<p align="right">(<a href="#readme-top">back to top</a>)</p>


#### bool

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### char

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### file

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### void pointer

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Array data types

#### unsigned_integerArray

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### integerArray

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### boolArray

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### charArray

<p align="right">(<a href="#readme-top">back to top</a>)</p>


#### string

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Macros


<p align="right">(<a href="#readme-top">back to top</a>)</p>



[issues-shield]: https://img.shields.io/github/issues/ArturAssisComp/ctest?logo=github&style=for-the-badge
[issues-url]: https://github.com/ArturAssisComp/ctest/issues

[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/ArturAssisComp/ctest/blob/version1_0/LICENSE
