todo
# libft
## What it is
- A library of standard [[C]] functions
- [Subject](file:///Users/sbars/Downloads/en.subject.pdf)
## [[todo]]
- [ ] functions
  - [ ] libc functions
    1. [x] isalpha
    2. [x] isdigit
    3. [x] isalnum
    4. [x] isascii
    5. [x] isprint
    6. [x] strlen
    7. [x] toupper
    8. [x] tolower
    9. [x] memset
    10. [x] bzero
    11. [ ] strlcpy
        - [ ] handle errors
        1.  [ ] your strlcpy does works whe size < strlen(src)
        2.  [ ] your strlcpy copies while destsize is zero, or does not return the size of the string it tried to create
    12. [ ] strlcat
        1. [fail]: your strlcat does not work with basic input
        2. [fail]: your strlcat does not work with over length size
        3. [ ] [crash]: your strlcat does not work with a size of 0
        - [ ] [fail]: your strcat does not work with empty string as second parameter
        - [ ] [fail]: your strlcat does not set a \0 to the end
        - [ ] [crash]: your strlcat crash because it read too many bytes or attempt to write on buff !
        - [ ] [fail]: your strlcat return value is false
    13. [x] strchr
    14. [x] memchr
    15. [x] memcpy
    16. [ ] memmove
    17. [x] memcmp
    18. [x] strrchr
        1.  [ ] only error left to fix (crash because reads too much data)
    19. [x] strncmp
    20. [x] strnstr
    21. [ ] atoi
    22. [ ] calloc
        1.  almost done, just one error left to fix
    23. [x] strdup
  - Additional functions
    1. [ ] ft_substr
      - Uses malloc
      - I can use len for malloc. To get the actual len I need to do s size - start index
    2. [x] ft_strjoin
       1. [x] allocate space with malloc for concatenate thing
    3. [ ] ft_strtrim
    4. [ ] ft_split
    5. [ ] ft_itoa
    6. [ ] ft_strmapi
    7. [ ] ft_striteri
    8. [ ] ft_putchar_fd
    9.  [ ] ft_putstr_fd
    10. [ ] ft_putendl_fd
    11. [ ] ft_putnbr_fd
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