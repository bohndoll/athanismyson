---
author: Bohn
title: Form untuk OB
date: 2021-10-06T03:15:28.548Z
description: Stack yang digunakan adalah Survey.js dan Google Sheets.
categories:
  - Tutorial
tags:
  - Works
image: screenshot-2021-10-05-at-10-50-00-dashboard-mtc-›-laporan-ob.png
license: Free
---
### Buat Laporan Baru

<!--StartFragment-->

<head>

    <!-- Required meta tags -->

    <meta charset="utf-8">

    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">



    <!-- Bootstrap CSS -->

    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    <link href="https://unpkg.com/survey-jquery@1.8.70/modern.css" type="text/css" rel="stylesheet" />

    <title>SurveyJS and Google Sheets untuk Form OB</title>

  </head>

  <body>

<!-- Button trigger modal -->



  <main role="main" class="container">



    <div>

      <h1>Form untuk OB</h1>

      <p class="lead">Stack yang digunakan adalah Survey.js dan Google Sheets.</p>

      <p><button type="button" class="btn btn-success" data-toggle="modal" data-target="#exampleModal">

        Buka Form

      </button></p>

      <p><a href="https://docs.google.com/spreadsheets/d/1nANUA6tl4RG-eyzZOaJ85QjgwQmDtXCD_BSiIwupnpw/edit?usp=sharing" class="btn btn-info" target="_blank">

        Lihat Data Laporan

    </a></p>

    </div>

    <br>

    <hr>

    <div class="embed-responsive embed-responsive-4by3">

        <iframe class="embed-responsive-item" width="600" height="450" src="https://datastudio.google.com/embed/reporting/d7f5c55d-16d4-44aa-90d8-c9df58242672/page/p_hjri8ogznc" frameborder="0" style="border:0" allowfullscreen></iframe>

    </div>

  </main><!-- /.container -->

  

  <!-- Modal -->

  <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">

    <div class="modal-dialog modal-lg" role="document">

      <div class="modal-content">

        <div class="modal-header">

          <button type="button" class="close" data-dismiss="modal" aria-label="Close">

            <span aria-hidden="true">&times;</span>

          </button>

        </div>

        <div class="modal-body">

            <div id="surveyContainer"></div>

        </div>

      </div>

    </div>

  </div>

    <!-- Optional JavaScript -->

    <!-- jQuery first, then Popper.js, then Bootstrap JS -->

    <script src="https://code.jquery.com/jquery-3.3.1.min.js" crossorigin="anonymous"></script>

    <script src="https://unpkg.com/survey-jquery@1.8.70/survey.jquery.min.js"></script>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>

    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

    

    <script>

Survey.StylesManager.applyTheme("modern");



var surveyJSON = {"title":"Form Input Laporan OB","description":"Form ini digunakan untuk membantu Staff MTC dalam melakukan monitoring pekerjaan harian.","pages":\[{"name":"Halaman 1","elements":[{"type":"dropdown","name":"Nama Pemeriksa","title":"Nama Pemeriksa","description":"Pilih yang sesuai","isRequired":true,"requiredErrorText":"Nama Pemeriksa tidak boleh Kosong.","choices":[{"value":"Khaidir","text":"Khaidir"},{"value":"Jajat","text":"Jajat"},{"value":"Sri Dewi","text":"Sri Dewi"}],"optionsCaption":"Pilih Salah Satu","showOptionsCaption":false},{"type":"text","name":"Tanggal","title":"Tanggal Pemeriksaan","description":"Pilih tanggal pemeriksaan","isRequired":true,"requiredErrorText":"Tanggal Pemeriksaan tidak boleh kosong","inputType":"date"},{"type":"dropdown","name":"Jenis Pekerjaan","title":"Jenis Pekerjaan","description":"Pilih yang sesuai","isRequired":true,"requiredErrorText":"Jenis Pekerjaan belum diisi","choices":\[{"value":"Pemeriksaan","text":"Pemeriksaan"},{"value":"Pengaturan","text":"Pengaturan"},{"value":"Perbaikan","text":"Perbaikan"}],"optionsCaption":"Pilih Salah Satu","showOptionsCaption":false},{"type":"checkbox","name":"Nama Perangkat","title":"Nama Perangkat","description":"Pilih nama perangkat mana saja yang diperiksa.","isRequired":true,"requiredErrorText":"Nama Perangkat belum dipilih.","choices":\[{"value":"Mesin Absensi","text":"1. Mesin Absensi"},{"value":"Perangkat XL","text":"2. Perangkat Jaringan XL"},{"value":"UPS","text":"3. UPS"},{"value":"Perangkat ICON","text":"4. Perangkat Jaringan ICON"},{"value":"Server Mini Banking","text":"5. Server Mini Banking"},{"value":"Server MTC","text":"6. Server MTC"},{"value":"Mesin Fotokopi","text":"7. Mesin Fotokopi"},{"value":"Perangkat Wifi","text":"7. Perangkat Wifi"}],"hasSelectAll":true,"selectAllText":"Pilih Semua"},{"type":"dropdown","name":"Status","title":"Status Perangkat","description":"Pilih yang sesuai","isRequired":true,"requiredErrorText":"Status Perangkat belum diisi.","choices":\[{"value":"OK","text":"OK"},{"value":"Bermasalah","text":"Bermasalah"}],"optionsCaption":"Pilih Salah Satu","showOptionsCaption":false},{"type":"comment","name":"Keterangan","visibleIf":"{Status} = 'Bermasalah'","title":"Rincian Permasalahan","description":"Apabila status bermasalah, maka harap deskripsikan pada kolom di bawah ini","requiredIf":"{Status} = 'Bermasalah'"},{"type":"html","name":"question1"}],"questionTitleLocation":"top","title":"Halaman 1"}]}



function sendDataToServer(survey, options) {

    //Display information about sending data

    options.showDataSaving();

    $.ajax({

        url: 'https://script.google.com/macros/s/AKfycby-8g-OMTt3k4UA2Y6Hr1w9hu3RakQeNuvQgts6uolSh5DLIejfWWohBcY-1E0GVztD/exec',

        type: 'post',

        data: JSON.stringify(survey.data),

        //We need tell web app that we use plain text.

        headers: {

            "Content-Type": "text/plain"

        },

        processData: false,

        complete: function(res, status) {

            if (status == 'success') {

                //Show that data was send successfully

                options.showDataSavingSuccess();

            }else {

                //Display retry button in case of error

                options.showDataSavingError();

            }

        },

    });

}



var survey = new Survey.Model(surveyJSON);

$("#surveyContainer").Survey({

    model: survey,

    onComplete: sendDataToServer

});

    </script>

  </body>

<!--EndFragment-->

### Lihat Laporan

<iframe width="600" height="450" src="https://datastudio.google.com/embed/reporting/d7f5c55d-16d4-44aa-90d8-c9df58242672/page/p_hjri8ogznc" frameborder="0" style="border:0" allowfullscreen></iframe>