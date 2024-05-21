# Kode program

```html css
<!DOCTYPE html>

<html>

<head>

    <title>Pesona Indonesia</title>

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>

body {

    margin: 0;

    padding: 0;

}

  

.navbar {

    display: flex;

    position: fixed;

    margin-bottom: 500px;

    background-color: white;

    padding-right: 100%;

    justify-content: center;

    box-shadow: 0px 0px 5px 0px;

    z-index: 99;

}

  

.navbar > img.logo {

    width: auto;

    height: 60px;

    margin-left: 30px;

    margin-right: auto;

    padding-left: 400px;

    padding-top: 10px;

    padding-bottom: 10px;

    width: 115px;

}

  

.navbar p {

    padding: 15px;

    cursor: pointer;

    transition: 0.8s all;

}

  

.navbar p:hover {

    transform: scale(1.3);

}

  

.navbar p:active {

    transform: scale(0.8);

}

  

.navbar img.garis {

    margin-left: auto;

    padding-right: 30px;

    padding-top: 20px;

    padding-bottom: 10px;

    height: 40px;

}

  

@media only screen and (max-width: 768px) {

.navbar {

    padding-right: 20px;

    }

  

.navbar > img.logo {

    padding-left: 20px;

    }

}

  

.background {

    background-image: url(img1.jpeg);

    background-size: cover;

    padding-top: 100px;

    height: 600px;

    text-align: center;

    width:100%;

}

  

.button {

    background-color: blue;

    color: white;

    padding: 10px 20px;

    border-radius: 5px;

    cursor: pointer;

    border: none;

}

  

.button:hover {

    background-color: white;

    color: navy;

}

  

.tex {

    color: white;

    padding-top: 10%;

    padding-bottom: 20px; }

  

.container {

     display: flex;

    flex-wrap: wrap;

    justify-content: center;

}

  

.box {

    border: 1px black;

    border-radius: 10px;

    box-shadow: 2px 2px 2px 2px;

    background-color: white;

    width: 250px;

    height: 450px;

    margin: 20px;

}

  

.gambar {

    margin-top: 20px;

    width: 220px;

    height: 150px;

    padding-left: 15px;

    border-radius: 30px;

}

  

.tombol {

    background-color: blue;

    color: white;

    margin: 20px;

    height: 40px;

    border: none;

    border-radius: 5px;

    cursor: pointer;

}

  

.tombol:hover {

    background-color: navy;

    color: white;

}

  

.end {

    background-color: blue;

    color: white;

    height: 300px;

    display: flex;

    align-items: center;

    text-align: center;

}

  

#border {

    width: 200px;

    height: 200px;

    border-radius: 100px;

    margin: 20px;

    filter: grayscale(100);

}

  

#jd {

    text-align: center;

}

  

.text {

    margin-top: 40px;

    margin-left: 10px;

    display: flex;

    flex-direction: column;

}

  

@media (max-width: 600px) {

.end {

    flex-direction: column;

    height: auto;

}

  

#border {

    margin: 10px auto;

}

  

.text {

    margin-top: 20px;

}

    }

    </style>

</head>

<body>

    <nav class="navbar">

        <img src="logo.png" alt="logo" class="logo">

        <p>Beranda</p>

        <p>Berita</p>

        <p>About</p>

        <img src="garis3.webp" alt="garis 3" class="garis">

    </nav>

  

    <div class="background">

        <div class="tex">

            <h2>Selamat Datang Di Indonesia!</h2>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. <br> Quasi quibusdam blanditiis natus.

                Est voluptatibus eum, <br> officia expedita unde reiciendis maiores,

                magni perspiciatis ipsum <br>quae ipsam, illum beatae eaque omnis nostrum!

            </p>

            <input class="button" type="button" value="klik disini!">

        </div>

    </div>

  

    <h2 align="center">Berita</h2>

    <div class="container">

        <div class="box">

            <img class="gambar" src="img2.jpeg" alt="pantai kuta">

            <h3>Pantai Kuta</h3>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur sequi officia est molestiae

                architecto veniam non. Nesciunt possimus iure perferendis cupiditate sapiente consectetur,

                at eligendi incidunt animi sit. Expedita, aliquid!

            </p>

            <input class="tombol" type="button" value="Baca Selengkapnya >>>">

        </div>

  

        <div class="box">

            <img class="gambar" src="img3.jpeg" alt="pantai kuta">

            <h3>Kebun Tetta</h3>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur sequi officia est molestiae

                architecto veniam non. Nesciunt possimus iure perferendis cupiditate sapiente consectetur,

                at eligendi incidunt animi sit. Expedita, aliquid!

            </p>

            <input class="tombol" type="button" value="Baca Selengkapnya >>>">

        </div>

  

        <div class="box">

            <img class="gambar" src="img4.jpeg" alt="pantai kuta">

            <h3>Gunung Bromo</h3>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur sequi officia est molestiae

                architecto veniam non. Nesciunt possimus iure perferendis cupiditate sapiente consectetur,

                at eligendi incidunt animi sit. Expedita, aliquid!

            </p>

            <input class="tombol" type="button" value="Baca Selengkapnya >>>">

        </div>

  

        <div class="box">

            <img class="gambar" src="img5.jpeg" alt="pantai kuta">

            <h3>Jekadah!</h3>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur sequi officia est molestiae

                architecto veniam non. Nesciunt possimus iure perferendis cupiditate sapiente consectetur,

                at eligendi incidunt animi sit. Expedita, aliquid!

            </p>

            <input class="tombol" type="button" value="Baca Selengkapnya >>>">

        </div>

    </div>    

  

    <div class="end">

        <img id="border" src="img6.jpeg" alt="orang kul">

        <div class="text">

            <h3 id="jd">About</h3>

            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.

                 Est reiciendis nostrum quisquam, quae ea dolorem obcaecati, <br>

                 quia ipsam quam architecto asperiores hic eaque odio numquam optio quo.

                 Sed, dolorum quidem. <br> Lorem ipsum dolor sit amet consectetur adipisicing elit.

                  Libero, minus? Ut rerum suscipit explicabo accusamus fugiat soluta aperiam <br>aliquam doloremque tempora inventore.

                  Adipisci eveniet officia nesciunt amet quo pariatur accusamus.

            </p>

            <p><b>Perhatikan ini gambar di samping, di kasih hitam putihki ini..</b></p>

        </div>

    </div>

</body>

</html>
```


# Hasil

![[Remedial CSS/Aset Remedial/1.png]]
![[Remedial CSS/Aset Remedial/2.png]]
![[Remedial CSS/Aset Remedial/3.png]]
