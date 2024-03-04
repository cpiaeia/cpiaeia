<div  align="center">

Const
</div>

# 1. Const Qualifier
## const int MAXSIZE = 256 
> Usually, constant is defined as a global variable.
* ## Property
  * ### Cannot be modified later on
  ``` c++
  const int a = 10;
  a = 11; // Error
  ```
  * ### Must be initialized when it is defined
  ``` c++
  const int i; 
  // Error
  ```
# 2. Const Reference
## Initialization
* ## const int iVal = 10;
* ## const int &rVal = iVal;
## Property
* ### const reference can be initialized to an rvalue
  ``` c++
  const int &ref = 10; // OK
  const int &ref = iVal+10; // OK
  ```
* ### In contrast nonconst reference cannot be initialized to an rvalue
  ``` c++
  int &ref = 10; // ERROR
   int &ref = iVal+10; // ERROR
  ```
# 3. Particular use: pass struct/class as the function argument
  ``` c++
  int avg_exam(const struct Grades & gr){
  return (gr.midterm+gr.final)/2;
  }
  ```
## Problem
  * ### Pass-by-value can be expensive, particularly for large structures.
    ``` c++
    int avg_exam(struct Grades gr)
    ```
  * ### It allows for the possibility of (mistakenly) changing the contents of the caller’s gr.
    ``` c++
    int avg_exam(struct Grades & gr)
    ```
## Advantage of using const reference as argument
  * ### We don't have the expense of a copy.
  * ### We have the safety guarantee that the function cannot change the caller's state.
  * ### Compared with non-const reference, another advantage is that function call with consts or expressions is OK
    * ### In contrast, for non-const reference, function call with consts or expressions is not OK
  ``` c++
  foo(“Hello world!”)
  void foo(string & str) {...} //wrong
  ```
  ### Versus
  ``` c++
  void foo(const string &str) {...} //correct
  ```
  * ### Why?
  > ### const reference can be initialized to an rvalue, but, nonconst reference cannot be initialized to an rvalue
# 4. Const Pointer
  ## Pointer to const  (const T *p)
  > ### "T" the pointed-to object cannot be changed by pointer p
  * ## Example
  ``` c++
  int a = 53;
  const int *cptr = &a; 
  // OK: A pointer to a const object can be assigned the address of a nonconst object
  *cptr = 42;
  // ERROR: We cannot use a pointer to const to change the underlying object.
  a = 28; // OK
  int b = 39;
  cptr = &b; // OK: the value in the pointer can be changed.
  ```
  ## Const pointer (T *const p)
  > ### "p" (the pointer) cannot be changed
  * ## Example
  ``` c++
  int a = 53;
  int *const cptr = &a; 
  // OK: initialization
  *cptr = 42;
  // OK: We can use a const pointer to change the underlying object.
  int b = 39;
  cptr = &b;
  // ERROR: We cannot change the value of a const pointer.
  ```
  ## const T *const p 
  > ### neither can be changed
# 5. Define Pointers to const using typedef
* ## Typedef: gives an alias to the existing types
  ``` c++
  typedef existing_type alias_name;
  typedef int * intptr_t;
  //Then we can use:
  intptr_t ip;
  ```
  * ### Use typedef to define pointer to const:
    ``` c++
    typedef const T constT_t;
    typedef constT_t * ptr_constT_t;
    //Now ptr_constT_t is an alias for the type of const T * (pointer const)
    ```
* ## How do we use typedef to rename the type of T *const?
  ``` c++
  typedef T * ptrT_t;
  typedef const ptrT_t constptrT_t;
  ```
  ``` c++
  typedef T * const constptrT_t;
  ```
# 6. Pointer to const versus Normal Pointer
* ## Pointers-to-const-T are not the same type as pointers-to-T.
* ## You can use a pointer-to-T anywhere you expect a pointerto-const-T, but NOT vice versa.
``` c++
int const_ptr(const int *ptr)
{
 …
}
int main()
{
 int a = 0;
 int *b = &a;
 const_ptr(b);
}// OK
```
``` c++
int nonconst_ptr(int *ptr)
{
 …
}
int main()
{
 int a = 0;
 const int *b = &a;
 nonconst_ptr(b);
}//Wrong
```
  




