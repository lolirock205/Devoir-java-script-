<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Exercices HTML en Script</title>
</head>
<body>

  <!-- Exercice 1 -->
  <h2>Exercice 1</h2>
  <div id="divTP1"></div>

  <!-- Exercice 2 -->
  <h2>Exercice 2</h2>
  <div id="divTP2"></div>

  <!-- Exercice 3 -->
  <h2>Exercice 3</h2>
  <div id="divTP4"></div>

  <script>
    // Exercice 1
    document.getElementById("divTP1").innerHTML =
      'Le <strong>World Wide Web Consortium</strong>, abrégé par le sigle <strong>W3C</strong>, est un <a href="http://fr.wikipedia.org/wiki/Organisme_de_normalisation" title="Organisme de normalisation">organisme de standardisation</a> à but non-lucratif chargé de promouvoir la compatibilité des technologies du <a href="http://fr.wikipedia.org/wiki/World_Wide_Web" title="World Wide Web">World Wide Web</a>.';

    // Exercice 2
    let langages = ["JavaScript", "JScript", "ActionScript", "EX4"];
    let contenu = "<p>Langages basés sur ECMAScript :</p><ul>";
    for (let i = 0; i < langages.length; i++) {
      contenu += "<li>" + langages[i] + "</li>";
    }
    contenu += "</ul>";
    document.getElementById("divTP2").innerHTML = contenu;

    // Exercice 3
    document.getElementById("divTP4").innerHTML = `
      <form enctype="multipart/form-data" method="post" action="upload.php">
        <fieldset>
          <legend>Uploader une image</legend>
          <div style="text-align: center">
            <label for="inputUpload">Image à uploader :</label>
            <input type="file" name="inputUpload" id="inputUpload" /><br /><br />
            <input type="submit" value="Envoyer" />
          </div>
        </fieldset>
      </form>
    `;
  </script>

</body>
</html>
