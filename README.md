# Chatbot

Un « chatbot » est un robot logiciel pouvant dialoguer avec un consommateur par le biais d’un service de conversations automatisées (Messenger par exemple). Un acteur de la grande distribution décide de mettre en place un chatbot pour informer les consommateurs des horaires d'ouverture du magasin le plus proche de chez eux. Les magasins sont présents dans les villes de Paris, Lyon, Toulouse, Nantes et Marseille. 

On considère que le nom d'une ville figure dans un message, à partir du moment où les lettres qui composent le nom apparaissent consécutivement dans le message (en majuscules ou minuscules). Par exemple Paris figure dans parisienne mais Nantes ne figure pas dans maintenant.

* En entrée : un tableau avec les messages du consommateur.
* En sortie : le nom de la première ville présente dans l'ensemble des messages si elle existe, null sinon.

Exemples: 

	[
		"lol g r1 konpri"
	]
	return null

	[
		"slt j'aimerais contraite",
		"l'horaire du magazin de nantes svp"
	]
	return "Nantes"

	[
		"Bonjour",
		"je suis un toulousain à Paris",
		"où sont les chocolatines ?"
	]
	return "Paris"

Rappel des commandes junit :

    javac -cp .:junit-4.12.jar ChatbotTest.java
    java -cp .:junit-4.12.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore ChatbotTest
