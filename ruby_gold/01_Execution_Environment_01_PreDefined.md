### Ruby Predefine Variables
Ruby contains a wide range of predefined variables. Every predefined variable has its own specification. You can use predefine variables to perform a specific task like when dealing with interpreter parameters or regular expressions. The list of predefined variables in Ruby as shown below:

| Variables | Description |
|-----------|-------------|
| $! | It holds the exception information message set by the last ‘raise’. Alias of $ERROR_INFO. |
| $@ | It holds an array of the backtrace of the last exception raised. Alias of $ERROR_POSITION. |
| $/ | The input record separator, by default newline. If it is set to nil then the whole file will be read at once. Alias of $INPUT_RECORD_SEPARATOR. |
| $\ | The output separator for the print and IO#write, nil by default. Alias of $OUTPUT_RECORD_SEPARATOR. |
| $, | The output field separator for the print and default separator for Array#join. Alias of $OUTPUT_FIELD_SEPARATOR. |
| $; | It is the default separator for String#split. Alias of $FIELD_SEPARATOR. |
| $. | It holds the current input line number read from the last file. Alias of $INPUT_LINE_NUMBER.|
| $< | An object that gives access to the concatenation of the content of all the files given as a command line argument or $stdin. Alias of $DEFAULT_INPUT. |
| $> | It is the destination of output for kernel.print and kernel.printf, the default value is $stdout. Alias of $DEFAULT_OUTPUT. |
| $& | The string matched by the last pattern match. Alias of $MATCH. |
| $` | The string to the left of the last pattern match. Alias of $PREMATCH. |
| $’ | The string to the right of the last pattern match. Alias of $POSTMATCH. |
| $+ | The string correlated to the last matched group in the last successful pattern matched. Alias of $LAST_PAREN_MATCH. |
| $1-$9 | The string matched in the nth group of the last successful pattern matched. |
| $_ | The last input line read by get or readline in the current scope. It is a local variable. Alias of $LAST_READ_LINE. |
| $~ | It holds the information about the last match in the current scope. It is a local variables. Alias of $LAST_MATCH_INFO. |
| $-p | It is true if option -p is set (loop mode is on). It is read-only variable. |
| $-l | It is true if option -l is set (line-ending process is on). It is read-only variable. |
| $-i | This variable hold the extension if in-place-edit mode is set otherwise nil. |
| $-a | It is true if option -a is set (autosplit mode is one). It is read-only variable. |
| $-d | The level of -d is switch. Alias of $DEBUG. |
| $-v | The verbose flag. It is set by the -v switch. Alias of $VERBOSE. |
| $-K | The character encoding of the source code. Alias of $KCODE. |
| $0 | It contains the name of the script being executed. |
| $$ | The process number of the current Ruby program being executed. Alias of $PROCESS_ID. |
| $? | The status of the last child process terminated. Alias of $CHILD_STATUS. |
| $: | Load paths for programs and binary module by load or required. Alias of $LOAD_PATH. |
| $FILENAME | The name of current input file reads from $<. Same as $<.filename. |
| $stderr | Current standard error output. |
| $stdin | Current standard input. |
| $stdout | Current standard output. |
| $= | Flag for case-sensitive, nil by default.Alias of $IGNORECASE. |
| $* | Command line argument given for the program, also known as ARGV.Alias of ARGV. |
| $” | Array contains the module name loaded by require.Alias of $LOAD_FEATURES. |

##### Example:
```
# Ruby program to illustrate the use of pre-defined Variables 
  
# Using '$0' To know about the script name  
puts "Script_name: ",$0; # => Script_name: /var/www/service/usercode/969513068/source.rb
  
# Using ' #{$$}' to know about the total number of process in the script 
puts "Total number of process in this script: #{$$}" # => 
  
# Using $; as default separator for String#split. 
a = "1,2,3,4,5,6,7"
$; = ","
p a.split # => ["1", "2", "3", "4", "5", "6", "7"]
  
# Pattern matching 
"Welcome to Ruby World!" =~ /Ruby/
  
# use to print the string to the left of the last pattern match 
p $` # => "Welcome to "
  
# use to print the string matched by the last pattern match 
p $& # => "Ruby"
  
# use to print the string to the right of the last pattern match 
p $' # => " World!"
```

### Ruby Predefine Variables

| Constant Name | Description |
|---------------|-------------|
| TRUE | Equivalent to true. |
| FALSE | Equivalent to false. |
| NIL | Equivalent to nil. |
| STDIN | Standard input and default value of $stdin. |
| STDOUT | Standard output and default value of $stdout. |
| STDERR | Standard output error and default value of $stderr. |
| RUBY_VERSION | A string shows the version of Ruby interpreter. |
| RUBY_PLATFORM | A string shows the platform of Ruby interpreter. |
| RUBY_RELEASE_DATE| A string shows the release date of Ruby interpreter. |
| DATA | The file object of the program, pointing just after the END. And not defined if END is not present in the program. |
| ARGV | An array holds the command-line arguments passed to the program. Alias of $. |
| ARGF | An object that gives the access to the virtual concatenation of files passed as command-line arguments. Alias of $<. |
| ENV | It is a hash-like object, contains current environment variables. |

Note: It is recommended to use true, false, and nil because TRUE, FALSE, and NIL are backward-compatible.

##### Example:
```
# Ruby program to illustrate pre-defined Constants 

# To know about Ruby Version 
a = RUBY_VERSION
puts "Current Version: #{a}" # => Current Version: 3.1.0

# To Know about Ruby Platform 
b = RUBY_PLATFORM
puts "Platform of Ruby: #{b}" # => Platform of Ruby: x86_64-linux-gnu

# To know about Ruby Release Date 
c = RUBY_RELEASE_DATE
puts "Release date of Ruby: #{c}" # => Release date of Ruby: 2021-12-25
```
