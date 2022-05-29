# Lab Report 4 - Week 8
# Two markdown-parser


[Our markdown-parser](https://github.com/TerryYan26/markdown-parser.git)

[Reviewed markdown-parse](https://github.com/rmccrystal/markdown-parser.git)

# Snippet 1

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

Here is the  the CommonMark demo site produce:
![snippet1](Lab4/3.1.PNG)
The markdown-parse should be output:

``` 
[`google.com, google.com, ucsd.edu] 
```
We have to set up a test in Junit:

### Our test: 


Setting up a variable:

```
 private Path fileName5;
 private String content5;
 private ArrayList<String> links5;
 
 ```
 
Writting a structures for the test in `public void setUp() throws IOException:`

```
fileName5 = Path.of("Snippet1.md");
content5 = Files.readString(fileName5);
links5 = new ArrayList<String>();

```

Setting up a test:

```

  @Test
    public void testTestFile5() {
        links5.add("`google.com");
        links5.add("google.com");
        links5.add("ucsd.edu");
       
        assertEquals(links5, MarkdownParse.getLinks(content5));
        
  ```
  
  
Test result: Failures

![snippet1](Lab4/3.2.PNG)

### Reviewed test:
  
  
 Adding a test:
 ```
  @Test
    public void testfile9(){
        assertMarkdown(Path.of("Snippet1.md"), List.of("`google.com", "google.com", "ucsd.edu"));
    }
    
 ```
 Test result: Failures
 
 ![snippet1.1](Lab4/3.3.PNG)
 
### Question response Snippet 1 :
 
Yes, It can be a small (<10 lines) code change.We may use if statement to check when the first character is equal to the open backticks. It will print out that. Otherwise, it will not print.


# Snippet 2

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)

```

Here is the  the CommonMark demo site produce:
![snippet2](Lab4/3.4.PNG)
The markdown-parse should be output:
``` 
[a.com, a.com(()), example.com]
```
We have to set up a test in Junit:

## Our test: 

1. Setting up a variable:
```
 private Path fileName6;
 private String content6;
 private ArrayList<String> links6;
 ```
 2. Writting a structures for the test in `public void setUp() throws IOException:`
```
fileName6 = Path.of("Snippet2.md");
content6 = Files.readString(fileName6);
links6 = new ArrayList<String>();
```
3. Setting up a test:

```

  @Test
    public void testTestFile6() {
        links6.add("a.com");
        links6.add("a.com(())");
        links6.add("example.com");
       
        assertEquals(links6, MarkdownParse.getLinks(content6));
        
  ```
4. Test result: Failures
![snippet1](Lab4/3.5.PNG)

  ## Reviewed test:
  
  
  1. adding a test:
 ```
  @Test
    public void testfile10(){
        assertMarkdown(Path.of("Snippet2.md"), List.of("`google.com", "google.com", "ucsd.edu"));
    }
    
 ```
 2. Test result: Failures
 ![snippet1](Lab4/3.6.PNG)
 
 ### Question response Snippet2
 
 It seems like bigger than 10 lines. If we want to solve snippet2, we may use stack and create the stack structure. we have to trace the '(' and pop the data after ')'. It may fix that bug.
