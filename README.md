# tools


query	tag	shell	command	note
show files only, show folders only		cmd	dir /ad   dir/a-d	
output simple display (no datelastmodified, filesize), check subfolders		cmd	dir /b /s	
search using wildcards (^startswith, ? single char, * preceding character 0 or more times)		cmd	dir *.txt	Wildcards may yield unexpected results - see Remarks - https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/dir
search for pattern of text in a file		cmd	findstr  (/v does not match)	https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/findstr
pipe		cmd	command A | command B	use output from command A as input for command B
search current directory using regex		cmd	dir /b *.txt | findstr "regex"	findstr support for regex is limited and nonstandard (alternatives grep, ack, silver searcher, powershells select-string) https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/findstr
search other directory using regex		cmd	dir  c:\temp | findstr "regex"	findstr support for regex is limited and nonstandard (alternatives grep, ack, silver searcher, powershells select-string) https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/findstr
search multiple directories using regex		cmd	dir /b/s  c:\temp;c:\perflogs | findstr "regex"	findstr support for regex is limited and nonstandard (alternatives grep, ack, silver searcher, powershells select-string) https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/findstr
search using multiple search keys		cmd	OR - findstr "regex1 regex2"	https://superuser.com/questions/909127/findstr-dos-commands-multiple-string-argument
			AND -  findstr regex1 | findstr regex2
loop		cmd	TBC for/?	https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/for
display results in a table		cmd		
dump results to file		cmd	> filename	


