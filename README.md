<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Site Unblocker</title>
    <link rel="stylesheet" href="style.css">
  </head>

  <body>
    <h1>SiUn V0.02</h1>
    <input type="text" id="link" value="">
    <button type="button"; onclick = "update()">Update Link</button>
    <br>
    <input type="checkbox" id="proxy">
    <label for = "proxy"> Don't use proxy</label><br>

    <input type="checkbox" id="exploit">
    <label for = "exploit"> Don't use exploit</label><br>
    <br><br><br>
    <a href="#" ID="go">Site Link</a><br>
    <br><br>
  </body>
  <script>
    function update() {
      var link = document.getElementById("link").value;
      var noproxy = document.getElementById("proxy").checked;
      var noexploit = document.getElementById("exploit").checked;

      if (noproxy == false) {
        link = "http://translate.google.com/translate?sl=en&tl=en&u=" + link
      } else if (link.indexOf("https://www.") <= 0) {
        link = "https://www." + link
      }

      if (noexploit == false) {
      link = link + "?gogoten.org";
      }

      document.getElementById("go").href = link;
    }
  </script>
</html>
