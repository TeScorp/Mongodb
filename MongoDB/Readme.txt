Commandes utilisées:


1. Use contact

	Création de la base de données 'contact'
------------------------------------------------------------------------------

2. contact> db.createCollection("contactlist")
	
	Création d'une collection 'contactlist' dans la base de contact

------------------------------------------------------------------------------

3. contact> db.contactlist.insertMany()

	Insertion de plusieurs contact (5)
		- Fares Ben Lahmer
		- Seif Kefi
		- Sarra Fatnassi
		- Rym Ben Yahia
		- Sami Cherif
------------------------------------------------------------------------------

4. contact> db.contactlist.find()

	Affichage de tous les contacts créés.

------------------------------------------------------------------------------

5. contact> db.contactlist.findOne()

	contact> db.contactlist.findOne({ _id: ObjectId("<contact_id>") })
		Afficher un contact avec un id précis

------------------------------------------------------------------------------

6. contact db.contactlist.find({ age: { $gt: 18 } })

	Affichage des contacts ayant un age supérieur à 18.
		- Fares Ben Lahmer
		- Sarra Fatnassi

------------------------------------------------------------------------------

7. contact> db.contactlist.find({ age: { $gt: 18 } , "Last Name": {$regex: /ah/i} })

	Affichage des contacts ayant un age supérieur à 18 , dont le nom comporte "ah".
		- Fares Ben Lahmer

------------------------------------------------------------------------------

8. contact> db.contactlist.updateOne()
	
	Modification d'un prénom ou nom d'un des contact.

------------------------------------------------------------------------------

9. contact> db.contactlist.deleteMany()
	
	contact> db.contactlist.deleteMany({ age: {$lt: 5 } })
		Suppression des contacts dont les ages sont inférieurs à 5.
		- Rym Ben Yahia
		- Sami Cherif

------------------------------------------------------------------------------

10. contact> db.contactlist.find()

	Affichage de tous les contacts restant après une suppression de certains d'entre eux .
		- Fares Ben Lahmer
		- Seif Kefi
		- Sarra Fatnassi
