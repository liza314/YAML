# A basic concept on YAML

**Before starting with YAML here is some concept of serialization**

## **SERIALIZATION**
---------------------
It is a process of translating data structure/object in a format for storage purpose. The storage format later can be used to reconstruct into original object. The bits order in serialization can be used to create semantically identical clone. Marshalling is the process of object serialization. **Deserialization** is extracting a data structure from a series of bytes, opposite of serialization.

## **Uses of Serialization:**


1. Transferring data through wire
2. Storing data
3. Remote procedure calls (ex: SOAP)
4. Detecting changes in time varying data.

***Serialization mainly helps data structure to be architecture-independent format for storing, transferring or other uses among different programming languages. It also helps in byte-ordering, memory layout and provides simple different ways of representing data.***

## **Limitations:**

It breaks opacity of the abstract data types by exposing implementation details. Other way, it violates encapsulation.

## **Formats of serialization:**

1.  XML & SGML-------> In the late 1990s XML, and SGML subset, was used to produce a human  readable text-based encoding. XML was often used for asynchronous transfer of structured data between client and server in Ajax web applications. XML is an open format.


2.  JSON------> A lighter plain-text alternative to XML based on JavaScript syntax, is also used for client-server communication in web applications.

3.  YAML-----> a strict JSON superset, YAML is an open format. (details are given below)

4.  Property lists -----> p-list for short, doesn't refer to a single serialization format but instead several different variants, some human-readable and one binary. It is used for serialization by NeXTSTEP, GNUstep, macos and IOS frameworks. you can learn more Property lists here. 😀 😁

## **Supported programming languages:**

1.  C/C++-------> Boost framework and MFC framework (microsoft)

2.  CFML-----> WDDX
3.  GO -----> JSON & XML

4.  Haskell -------> type classes. 

And many other program languages java, JavaScript, julia, python, Ruby etc.

YEYY!!! you completed the most important part of the topic 🥳🥳.

HERE COMES YAML!!!

#YAML

YAML recursive acronym stands for “YAML Ain't Markup Language”. Firstly, it’s not markup language. It is a human friendly data serialization language and most importantly works perfectly with other programming languages. It is often used to write configuration files.

## **Features of YAML:**  

1. YAML is a data-oriented language that has features derived from Perl, C, HTML, and other languages.

2. YAML is a superset of JSON that comes with multiple built-in advantages such as including comments, self-referencing, and support for complex datatypes.

3. YAML data is portable between programming languages

4. Supports one-direction processing

5. Matches native data structures of agile methodology

6. Supports non-hierarchical data models

7. YAML specification identifies an instance document as a "Presentation" or "character stream.

8. Purely a data-representation language and thus has no executable commands



Multiple software packages have implemented YAML to create powerful configuration management tools such as Red Hat’s Ansible

## **YAML Syntax:**

***yaml datatypes:***
Values in YAML's key-value pairs are scalar. They act like the scalar types in languages like Perl, Javascript, and Python.
The following data types are supported by YAML:

***Types	Description***
String	Strings are enclosed with or without double or single quotes
number	It can be integers or floating values
Boolean	Accepts true or false
sequence	Supports array or list
Set	Set stores the elements with unordered without duplicates
Map	maps stores key with value as like hash map
binary	support binary data of octal strings - images,files
timestamp	Supports date, datetime


***Rules for Creating YAML file:***

basic rules: 
1. YAML is case sensitive
2. The files should have .yaml as the extension
3. YAML does not allow the use of tabs while creating YAML files; spaces are allowed instead


***How YAML Works:***

1. Scalars, or variables, are defined using a colon and a space.

```
integer: 25 
string: "25" 
float: 25.0 
boolean: Yes
```
numeric types

　```
---
 foo: 12345
 bar: 0x12d4
 plop: 023332
 ```

strings are Unicode

```
---
　
foo: "this is not a normal string\n"
bar: this is not a normal string\n
```

nulls with a tilde or the unquoted null string literal

```
---
foo: ~
bar: null
```

boolean values

```
---
foo: True
bar: False
light: On
TV: Off
```

arrays


```
---
items: [ 1, 2, 3, 4, 5 ]
names: [ "one", "two", "three", "four" ]
```


dictionaries


```
---
foo: { thing1: huey, thing2: louie, thing3: dewey }
```


2. Associative arrays and lists can be defined using a conventional block format or an inline format that is similar to JSON.


```
--- # Shopping List in Block Format
 - milk - eggs – juice
 --- # Shopping List in Inline Format
 [milk, eggs, juice]
```


3. Strings do not require quotation mark. Strings can be denoted with a | character, which preserves newlines, or a > character, which folds newlines.


```
data: |
 Each of these
 Newlines Will 
 be broken up 
 ```

```
data: > 
This text is
wrapped and will
be formed into 
a single paragraph

```
4. block format uses hyphen (-) and space to begin a new item in a specified list

```
--- # Favorite movies
 - Casablanca
 - North by Northwest
 - The Man Who Wasn't There
```

5. Comments begin with a pound sign

___
 This is a full line comment
foo: bar # this is a comment, too

Synopsis of YAML Basic Elements:
-	The synopsis of YAML basic elements is given here: Comments in YAML begins with the (#) character.
-	Comments must be separated from other tokens by whitespaces.
-	Indentation of whitespace is used to denote structure.
-	Tabs are not included as indentation for YAML files.
-	List members are denoted by a leading hyphen (-).
-	List members are enclosed in square brackets and separated by commas.
-	Associative arrays are represented using colon ( : ) in the format of key value pair. They are enclosed in curly braces {}.
-	Multiple documents with single streams are separated with 3 hyphens (---).
-	Repeated nodes in each file are initially denoted by an ampersand (&) and by an asterisk (*) mark later.
-	YAML always requires colons and commas used as list separators followed by space with scalar values.
-	Nodes should be labelled with an exclamation mark (!) or double exclamation mark (!!), followed by string which can be expanded into an URI or URL.

Advanced component:

 YAML has the strip chomp and preserve chomp operators. To save the last character, add a plus to the fold or block operators.
 

bar: >+
  this is not a normal string it
  spans more than
  one line
  see?
 

if the value ends with whitespace, like a newline, YAML will preserve it. To strip the character, use the strip operator.







