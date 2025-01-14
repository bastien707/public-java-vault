- **Why exceptions ?**
	- Separate the normal control flow from error handling
- **Checked**
	- Need to be handles by `try catch` or `throws`
	- `IOException`, `FileNotFoundException`
	- Not programmer's fault
	- No checked exceptions in **Kotlin**
	- **Why checked exists ?**
		- *“You can’t accidentally say, ‘I don’t care.’ You have to explicitly say, ‘I don’t care.'”* — James Gosling (the creator of Java)
- **Unchecked**
	- Does not need to be handled
	- From programmer's fault
	- `NumberFormatException`
- **Do you create exceptions ?**
	-  checked exceptions = forcer les utilisateurs de mon code a gérer cette exception.
	- Dans notre cas on utilise genéralement une runtime exception pour renvoyer l'erreur au client.

***

https://reflectoring.io/do-not-use-checked-exceptions/