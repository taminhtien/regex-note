# regex-note
```
abc…	      Letters
123…	      Digits
\d	        Any Digit
\D	        Any Non-digit character
.	        Any Character
\.	        Period
[abc]	    Only a, b, or c
[^abc]	    Not a, b, nor c
[a-z]	    Characters a to z
[0-9]	    Numbers 0 to 9
\w	        Any Alphanumeric character
\W	        Any Non-alphanumeric character
{m}	        m Repetitions
{m,n}	    m to n Repetitions
*	        Zero or more repetitions
+	        One or more repetitions
?	        Optional character
\s	        Any Whitespace
\S	        Any Non-whitespace character
^…$	      Starts and ends
(…)	      Capture Group
(a(bc))	    Capture Sub-group
(.*)	    Capture all
(abc|def)	Matches abc or def
```
- Matching Phone Numbers

```
Task	  Text	            Capture   Groups	 
Capture	  415-555-1234	    415	      Success
Capture	  650-555-2345	    650	      Success
Capture	  (416)555-3456	    416	      Success
Capture	  202 555 4567	    202	      Success
Capture	  4035555678	    403	      Success
Capture	  1 416 555 9292	416	      Success

1?[\s]?\(?(\d{3})\)?[-\s]?\d{3}[-\s]?\d{4}
```
- Matching Numbers

```
Task	  Text	 
Match	  3.14529	    Success
Match	  -255.34	    Success
Match	  128	        Success
Match	  1.9e10	    Success
Match	  123,340.00	Success
Skip	  720p	        Success

^-?\d+(,\d+)*(\.\d+(e\d+)?)?$
```
- Matching Emails
```
Task	    Text	                            Capture     Groups	 
Capture	    tom@hogwarts.com	                tom	        Success
Capture	    tom.riddle@hogwarts.com	            tom.riddle	Success
Capture	    tom.riddle+regexone@hogwarts.com	tom.riddle	Success
Capture	    tom@hogwarts.eu.com	                tom	        Success
Capture	    potter@hogwarts.com	                potter	    Success
Capture	    harry@hogwarts.com	                harry	    Success
Capture	    hermione+regexone@hogwarts.com	    hermione	Success

^([\w.]*)

```
