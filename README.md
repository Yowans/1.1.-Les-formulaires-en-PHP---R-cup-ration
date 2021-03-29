# 1.1.-Les-formulaires-en-PHP---R-cup-ration

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <form  action="thanks.php"  method="post">
        <label  for="nom">Nom :</label>
        <input  type="text"  id="nom"  name="user_lastname">
        <label  for="prénom">Prénom :</label>
        <input  type="text"  id="prénom"  name="user_name">
        <label  for="courriel">E-mail :</label>
        <input  type="email"  id="courriel"  name="user_email">
        <label for="telephone">Téléphone :</label>
        <input type="tel" id="telephone" name="user_telephone">
        <div class="subject">
        <label for="subject">Sujet</label>
        <select name="subject" id="subject">
            <option>Demande d'information</option>
            <option>Recrutement</option>
            <option>Reclamation</option>
            <option>Autres</option>
        </select>
        <label  for="message">Message :</label>
        <textarea  id="message"  name="user_message"></textarea>
        <div  class="button">
        <button  type="submit">Envoyer votre message</button>
    </form>
</body>
</html>


<?php

echo "Merci " . $_POST['user_name'] . " " . $_POST['user_lastname'] . 
" de nous avoir contacté à propos de " . $_POST['subject'] . ".";
echo "<br>";
echo "<br>";
echo "Un de nos conseiller vous contactera soit à l'adresse " . $_POST['user_email'] . 
" ou par téléphone au " . $_POST['user_telephone'] . " dans les plus brefs délais pour traiter votre demande :";
echo "<br>";
echo "<br>";
echo $_POST['user_message'];
