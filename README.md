Kokeile tehdä käyttöliittymä puhelinluetteloon.
Tässä vaiheessa tehdään ensin vain taulukko henkilöistä.
Luo itsellesi oma tyylimäärittely taulukkoon, jonka otat käyttöön tässä harjoituksessa luomaasi html -sivuun. 
Luo html sivu Visual Studio Codessa. Voit lisätä esim. live-server laajennoksen jolla pystyt suorittamaan html sivua.
 Sisällytä script tag html sivuun ja lisää koodin runko tämän esim. mukaisesti (lisää ao. script elementti body -elementin sisälle):
 <script> 
                $(document).ready(function () { 
                    // FETCHING DATA FROM JSON FILE 
                    $.getJSON("http://a41d.k.time4vps.cloud:3001/henkilot",  
                      function (data) { 
  TÄSSÄ MUODOSTA TAULUKKO DATASTA

    }); 

 </script>
Lisää myös sivun alkuun (head elementin sisälle) toinen script -elementti jossa otat jqyeryn käyttöön (voit ottaa uudemman version jquery:stä kuin tässä esimerkissä):
<script src="https://code.jquery.com/jquery-3.5.1.js">  
</script> 
 
Eli sivun "pohjakoodi" voisi olla tehty kuten tässä.
Voit myös käyttää tässä harjoituksessa omaa ulkoista tyylitiedostoasi (.css), jos haluat.

Luo lisäksi toiminto eri sivulla jossa voit hakea tekstilaatikkoon syötetyn nimen perusteella ko. henkilön puhelinnumeron esim. toiseen tekstilaatikkoon (tässä voit tosin muotoilla oman tyyppisen käyttöliittymän). Runko haun mahdollistavalle sivulle:
<!DOCTYPE html>
<html>
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

    <script>
      $(document).ready(function () {
        $('[name="submit"]').click(function () {
           
        });
      });
    </script>
  </head>
  <body>
    <form id="form" name="form">
      <th>Syötä nimi:</th>
      <td>
        <input
          name="nimi"
          id="nimi"
          type="text"
          value=""
          maxlength="35"
          size="35"
        />
      </td>
      <td>
        <input
          name="puhelin"
          id="puhelin"
          type="text"
          value=""
          maxlength="35"
          size="35"
        />
      </td>

      <td>
        <input name="submit" type="button" value="Hae puhelinnumero" />
      </td>
    </form>
  </body>
</html>



Lopuksi luo pääsivu (index.html), jossa on linkkeinä valinnat koko puhelinluettelo (ts. kaikki henkilöt) ja haku (nimen perusteella). Haku ja taulukko sivustoilta tulisi päästä takaisin pääsivulle.
