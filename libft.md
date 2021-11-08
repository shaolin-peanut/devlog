todo
# libft
## What it is
- A library of standard [[C]] functions
- [Subject](file:///Users/sbars/Downloads/en.subject.pdf)
## [[todo]]
- [ ] understand purpose and application of each function
  - [ ] create your libft docs
    - [ ] rename this file to 'project/ code libft' and make a new libft page documenting all of it
- [ ] functions
  - [x] libc functions
    1. [x] isalpha
       1. checks if char parameter is alphabetic in the ascii table
    2. [x] isdigit
       1. checks if char paramater is a digit on the ascii table, between 0 and 9
    3. [x] isalnum
       1. checks if char paramater is alphanumeric (isalpha + isdigit)
    4. [x] isascii
       1. checks if char parameter is a character of the ascii table
    5. [x] isprint
       1. checks if char paramter is printable
    6. [x] strlen
       1. counts length of a string, stopping at the first '/0' encountered
    7. [x] toupper
       1. transform every lowercase letter in parameter string to uppercase letter
    8. [x] tolower
       1. transforms every upppercase letter in string parameter to lowercase letter
    9.  [x] memset
        1. > The memset() function writes len bytes of value c (converted to an unsigned char) to the string b.
        2. `void *
     memset(void *b, int c, size_t len);`
    10. [x] bzero
        1.  fills string with zeros
    11. [x] strlcpy
        1.  copies *len* characters from src string to dst string
    12. [x] strlcat
        1.  copies *len* chars from src string to end of dst string
    13. [x] strchr
        1.  `char * strchr(const char *s, int c);`
        2.  locate first occurence of c in s, return pointer to that occurrence
    14. [x] memchr
        1.  `void *memchr(const void *s, int c, size_t n);`
        2.  locate first occurence of byte c in n bytes of string s
        3.  returns pointer to byte located or NULL
    15. [x] memcpy
        1.  [ ] `void *memcpy(void *restrict dst, const void *restrict src, size_t n);`
        2.  copies n bytes of src to dst, returns original value of dst
    16. [x] memmove
        1.  same as memcpy but handles overlap
    17. [x] memcmp
        1.  compares two strings. Assumed to be n bytes long. 
        2.  Returns diff between first 2 differing bytes
        3.  zero length strings are always identical
    18. [x] strrchr
        1.  like strchr, but locating last char
    19. [x] strncmp
    20. [x] strnstr
    21. [x] atoi
    22. [x] calloc
        1.  almost done, just one error left to fix
    23. [x] strdup
  - Additional functions
    1. [x] ft_substr
      - Uses malloc
      - I can use len for malloc. To get the actual len I need to do s size - start index
    2. [x] ft_strjoin
       1. [x] allocate space with malloc for concatenate thing
    3. [x] ft_strtrim
       1. remove chars in set array from s1 string
       2. How could I do this?
          1. What could go wrong?
             1. ft_trim(empty, not_empty)
             2. ft_trim(s1, empty)
          2. implementation braindump
             1. create ft_isset function
                1. will check if char c is an occurence of string
                2. already exists!! memchr or strchr
             2. find malloc length
                1. beginning
                   1. while (strchr(set, s1[i]))
                2. end
             3. allocate malloc
             4. while loop to trim set chars at beginning
             5. while loop to trim set chars from end
          3. What I did. (gets only bus errors)
             1. same as above, using memchr to increment counters of start & end, then using those counters for malloc and to fill a string starting from/up to the counters
          4. fucking malloc error
             1. was incrementing the output pointer, and returning that, so returning a string starting with \0 was obv not gonna work
    4. [x] ft_split
       1. let's try to get this one done asap
       2. `char **ft_split(char const *s, char c);`
       3. [x] Ok first I need to correctly get the number of strings to divide
          1. This is important for the first malloc allocation, which is creating the array of strings. Later there'll be another malloc, so I need this one to work well and be ready when I'll have strings to put in it.
       4. Ok let's think about what's left to do
          1. [x] find number of strings to create array
          2. [x] create array
          3. [ ] split strings
             1. [ ] iterate thru s1 and find index of substring in s1
             2. [ ] allocate space with malloc
             3. [ ] create substring into tab[i] with ft_substr
    5. [x] ft_itoa
       1. Ok let's try to understand this. First off, what is itoa?
          1. lololol had to hit delete, I started problem-solving while confusing atoi's functionality with itoa's
          2. I get an int, I must output a string. How do I do so? I don't have any string parsing to do, that's great. Can just output something made with strlcpy
          3. So the int, if superior to 9, must be divided by 10
             1. so recursive is annoying because of differing parameter/return data types
             2. I don't know how to do it
          4. What needs to be done
             1. find the length of the string to be created
             2. allocate enough space in the string
             3. 
    6. [x] ft_strmapi
    7. [x] ft_striteri
    8. [x] ft_putchar_fd
    9.  [x] ft_putstr_fd
    10. [x] ft_putendl_fd
    11. [x] ft_putnbr_fd
- [ ] [[makefile]]
  - [x] learn about makefiles
    - Starting to understand these, now I have to understand how to construct a proper makefile. A makefile contains building instructions. But what am I trying to build, and how should I do it?
      - [tutorial](attachments/ar_tuto.pdf)
        - A library. But what is a library? It's not a program. What I understood from a website talking about how to create a library, is that you should compile 
  - [x] write one
  - [ ] upgrade to match requirements
    - rules
      - $(NAME)
      - all
      - clean
      - fclean
      - re
- [x] [[header files]]
  - [ ] Learn about it
    - In a library, the header file should contain the prototype of every function, to be included everytime the library is included.
- [ ] functions to debug or rewrite
  - [ ] ft_memchr
  - [ ] ft_strlcat
  - [ ] ft_strrchr
  - [ ] ft_strnstr
  - [ ] ft_striteri
  - additional functions here all have bus errors
    - [ ] ft_strmapi
    - [ ] ft_substr
    - [ ] ft_strjoin
    - [ ] ft_strtrim
    - [ ] ft_split