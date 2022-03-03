- 👋 Hi, I’m @Minimalist-dev
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me neury.developer@gmail.com
- !DOCTYPE html>
<html>
<head>
    <title>Notas</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="/index.css">
    <link rel="stylesheet" href="">
<style>

</style>
<body>

<p>Start typing a name in the input field below:</p>
    <p>Suggestions: <span id="txtHint"></span></p>

    <form>
        First name: <input type="text" onkeyup="showHint(this.value)">
    </form>

<script>
    function showHint(str) {
      if (str.length == 0) {
        document.getElementById("txtHint").innerHTML = "";
                return;
            } else {
                const xmlhttp = new XMLHttpRequest();
                xmlhttp.onload = function () {
                    document.getElementById("txtHint").innerHTML = this.responseText;
                }
                xmlhttp.open("GET", "http://localhost/Notas/gethint.php?q=" + str);
                xmlhttp.send();
            }
        }
</script> 
</body>
</html>
