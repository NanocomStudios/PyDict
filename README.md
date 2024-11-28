PyDict Library for VB.NET and C#
================================

Import the "PyDict.dll" into your .Net project to use Python Dictionaries and Lists in your .Net project.

  

[**Download**](data/pydict.zip)

  
  

About the library
-----------------

Basic Introduction
------------------

This library was written using VB.Net 2008 and it can use in VB.Net and in C# in the Visual Studio. There are two main parts in this library.

*   Dictonary
*   List

You can use this to filter data from a python dictionary that is written in a string variable. You also can use this library to work with python lists that also is written in a string variable.

This can use to decode data from web APIs that output data in Python Dictonary.

_**Note :-** This library fully supports nesteding the dictionaries and lists and also combining both of them._

Import into a Project
---------------------

First, goto **"Project"** -> **"Add Reference..."** and in the popup window, click on the **"Browse"** and select the **"PyDict.dll"** file from the location you saved it.

Then in your code, Import it using the following code :

    Imports PyDict.Dict
    Imports PyDict.List

After that, create an object to call the functions in the library :

    Dim dict As New PyDict.Dict
    Dim list As New PyDict.List

Then you can use the new _'dict'_ and _'list'_ objects to use the functions in the library.

PyDict.Dict()
-------------

This class is used to work with Python Dictionaries.

Here are all the functions currently available on this version of the library,

### toArray(input)

**Inputs :**

*   input - The string that contains the dictionary.

**Output :**

*   A 2D string array that contains the keys and values of each entry of the given dictionary.

This function is used to decode a Python dictionary. It takes a dictionary written in a string variable and outputs a two-dimentional string array to use in our program. The key saves in the first dimention and the value saved in the second dimention.

The dictionary must be written using the correct syntax that used in the Python language. You can use " " or ' ' to store keys and valuse, but the function turns all the " " into ' ' inside the function (this only happen to the data inside the function and not in the main code).

### toDict(inp(,))

**Inputs :**

*   inp(,) - The 2D string array that contains the dictionary.

**Output :**

*   A string that contains the given 2D array converted to a dictionary.

This function is used to convert a given 2D array with the keys and valuse as the output array on `toArray()` function, into a Python dictionary and output it into a string variable.

This is the complete opposite opporation of the `toArray()` function.

### getValArr(inp(,) , key)

**Inputs :**

*   inp(,) - The 2D string array that contains the dictionary.
*   key - The key of the entry you need to extract from the dictionary.

**Output :**

*   A string that contains the value for the given key in the given dictionary.

This function is used to extract a value from a dictionary that was already converted into a 2D string array. If the given key is not available in the dictionary, there will be a runtime error and the program will crash. So run this in a `try()...catch()` or first verify that the key is available by the `isAvailable()` function.

### getVal(input , key)

**Inputs :**

*   input - The string that contains the dictionary.
*   key   - The key of the entry you need to extract from the dictionary.

**Output :**

*   A string that contains the value for the given key in the given dictionary.

This function is basicly the `getVarArr()` function but it takes the string contains the dictionary, and convert it to the 2d array inside the function and use it. So when using this, there's not a need to convert the dictionary in the string to to a 2D array.

### isAvailable(input , key)

**Inputs :**

*   input - The string that contains the dictionary.
*   key   - The key of the entry you need to extract from the dictionary.

**Output :**

*   True if the given key is in the dictionary.
*   False if the given key is not in the dictionary.

This function checks that the given value is available or not in the given dictionary.

PyDict.List()
-------------

This class is used to work with Python Lists.

Here are all the functions currently available on this version of the library,

### toArray(input)

**Inputs :**

*   input - The string that contains the list.

**Output :**

*   A string array that contains the values of the given list.

This function is used to convert a Python list into a regular string array that can use in the main code.

The list must be written using the correct syntax that used in the Python language. You can use " " or ' ' to store valuse, but the function turns all the " " into ' ' inside the function (this only happen to the data inside the function and not in the main code).

### toList(inp())

**Inputs :**

*   inp() - The string array that contains the dictionary.

**Output :**

*   A string that contains the given array converted to a list.

This function is used to convert a given array into a Python list and output it into a string variable.

This is the complete opposite opporation of the `toArray()` function.

### getVal(inp , n)

**Inputs :**

*   inp - The string that contains the list.
*   n - The index of the requesting value in the list.

**Output :**

*   A string that contains the value for the given index in the given list.

This function is used to extract a value from a list and output it in a string variable. This can be used to read values directly from the string contains the list.
