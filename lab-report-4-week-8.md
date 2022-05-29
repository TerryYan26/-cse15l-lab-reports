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
 
 ### Question response Snippet 1:
Yes, It can be a small (<10 lines) code change.We may use if statement to check when the first character is equal to the open backticks.  it will print out that. Otherwise, it will not print.
