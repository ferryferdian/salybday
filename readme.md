   
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Padel Party Reservation</title>
  <style>
     /* Responsive for mobile */
    @media (max-width: 600px) {
      .container {
        max-width: 100vw;
        border: none;
        box-shadow: none;
      }
      .main-title {
        font-size: 38px;
        padding: 16px 8px 6px 8px;
      }
      .event-details {
        font-size: 14px;
        padding: 0 8px 10px 8px;
      }
      .images-row img {
        height: 90px;
      }
      .rsvp-section {
        padding: 10px 4px;
        gap: 6px;
      }
      .rsvp-row {
        flex-direction: column !important;
        align-items: stretch !important;
        gap: 4px;
      }
      .rsvp-form-label {
        margin-bottom: 2px;
        font-size: 16px;
      }
      .toggle-wrapper {
        width: 80px;
        height: 30px;
        padding: 0 3px;
        margin-bottom: 8px;
      }
      .toggle-label {
        font-size: 14px;
      }
      .toggle-slider {
        width: 34px;
        height: 22px;
        top: 3px;
        left: 3px;
      }
      #yes:checked ~ .toggle-slider {
        left: 43px;
      }
      .btn-submit {
        width: 100%;
      }
    }
  @import url('https://fonts.googleapis.com/css2?family=Fredericka+the+Great&family=Indie+Flower&family=Roboto:wght@400;700&family=Pacifico&display=swap');

    /* Reset */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Barriecito', Barriecito;
      background-color: #fffbea;
      color: #000;
      line-height: 1.3;
      user-select: none;
    }

    /* Container */
    .container {
      max-width: 480px;
      margin: 0 auto;
      border: 1px solid #0000ff;
      border-top: none;
      border-bottom: none;
      box-shadow: 0 0 0 1px #0000ff inset;
    }

    /* Header */
    header {
      background-color: #bfff33;
      border-bottom: 2px solid #0000ff;
      display: flex;
      align-items: center;
      padding: 10px 15px;
      gap: 10px;
    }

    header .logo {
      width: 24px;
      height: 24px;
      background-color: #000;
      clip-path: polygon(50% 0%, 90% 25%, 90% 75%, 50% 100%, 10% 75%, 10% 25%);
      /* hexagon shape */
    }

    header .title {
      font-weight: 700;
      font-family: 'HK Groteska', cursive;
      font-size: 18px;
      letter-spacing: 0.05em;
    }

    /* Main Title */
    .main-title {
      font-family: 'Barriecito', cursive;
      font-weight: 700;
      font-size: 72px;
      line-height: 1;
      padding: 20px 15px 10px 15px;
      user-select: none;
    }

    /* Event Details */
    .event-details {
      padding: 0 15px 15px 15px;
      font-weight: 700;
      font-size: 16px;
      font-style: italic;
      user-select: none;
    }

    .event-details .location {
      font-weight: 400;
      font-style: normal;
      margin-top: 4px;
      line-height: 1.2;
    }

    /* Images Row */
    .images-row {
      display: flex;
      gap: 2px;
      user-select: none;
    }

    .images-row img {
      width: 100%;
      height: 160px;
      object-fit: fill;
      filter: grayscale(100%);
      display: block;
    }

    /* RSVP Section */
    .rsvp-section {
      background-color: #bfff33;
      color: #222;
      display: flex;
      flex-direction: column;
      gap: 10px;
      padding: 15px;
      font-family: 'Indie Flower', cursive;
      user-select: none;
    }

    .rsvp-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
      gap: 20px;
    }

    .rsvp-left {
      flex: 1;
    }

    .rsvp-left h2 {
      font-family: 'Pacifico', cursive;
      font-weight: 700;
      font-size: 28px;
      margin-bottom: 0;
      user-select: none;
      margin-right: 0;
    }

    .rsvp-left label {
      display: block;
      font-weight: 700;
      font-size: 20px;
      margin-bottom: 6px;
      user-select: none;
    }

    .rsvp-left input[type="text"],
    .rsvp-left input[type="tel"],
    .rsvp-form-fields input[type="text"],
    .rsvp-form-fields input[type="tel"] {
      width: 100%;
      font-family: 'Indie Flower', cursive;
      font-size: 18px;
      padding: 4px 6px;
      border: 2px solid #222;
      border-radius: 4px;
      background: transparent;
      color: #222;
      outline: none;
      user-select: text;
      box-sizing: border-box;
      transition: border 0.2s, box-shadow 0.2s;
    }
    .rsvp-form-fields input[type="text"]:focus,
    .rsvp-form-fields input[type="tel"]:focus {
      border: 2px solid #bfff33;
      box-shadow: 0 0 0 2px #bfff3340;
    }

    /* RSVP Right */
    .rsvp-right {
      text-align: right;
      flex-shrink: 0;
      user-select: none;
    }

    .rsvp-right .join-text {
      font-family: 'Pacifico', cursive;
      font-weight: 700;
      font-size: 28px;
      margin-bottom: 0;
      user-select: none;
      margin-left: 0;
    }

    /* Toggle Buttons */
    .toggle-wrapper {
      position: relative;
      width: 100px;
      height: 36px;
      background-color: #444;
      border-radius: 20px;
      box-shadow: inset 0 0 5px #000;
      user-select: none;
      display: flex;
      align-items: center;
      padding: 0 6px;
      gap: 6px;
    }

    .toggle-wrapper input[type="radio"] {
      display: none;
    }

    .toggle-label {
      flex: 1;
      text-align: center;
      font-family: 'Indie Flower', cursive;
      font-weight: 700;
      font-size: 18px;
      color: #bfff33;
      cursor: pointer;
      user-select: none;
      z-index: 2;
      transition: color 0.3s ease;
    }

    .toggle-slider {
      position: absolute;
      top: 3px;
      left: 3px;
      width: 44px;
      height: 30px;
      background-color: #bfff33;
      border-radius: 20px;
      box-shadow: 0 0 5px #bfff33;
      transition: left 0.3s ease;
      z-index: 1;
    }

    #yes:checked ~ .toggle-slider {
      left: 53px;
    }

    #yes:checked ~ label[for="yes"] {
      color: #222;
    }

    #no:checked ~ label[for="no"] {
      color: #222;
    }

    /* Footer bar */
    footer {
      height: 40px;
      background-color: #c83a8d;
      user-select: none;
    }
     .btn-submit {
      margin-top: 10px;
      background: #bfff33;
      color: #222;
      border: 2px solid #222;
      border-radius: 8px;
      font-family: 'Pacifico', cursive;
      font-size: 20px;
      font-weight: 700;
      padding: 8px 28px;
      cursor: pointer;
      box-shadow: 0 2px 6px #0001;
      transition: background 0.2s, color 0.2s, box-shadow 0.2s;
      letter-spacing: 0.03em;
    }
    .btn-submit:hover, .btn-submit:focus {
      background: #d6ff7f;
      color: #c83a8d;
      box-shadow: 0 4px 12px #bfff3340;
      outline: none;
    }
        /* RSVP Form Desktop Row */
    .rsvp-form-desktop-row {
      display: flex;
      flex-direction: row;
      align-items: flex-end;
      gap: 32px;
      width: 100%;
    }
    .rsvp-form-fields {
      flex: 2;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .rsvp-form-actions {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 10px;
      min-width: 140px;
    }

    @media (max-width: 600px) {
      .rsvp-form-desktop-row {
        flex-direction: column;
        align-items: stretch;
        gap: 0;
      }
      .rsvp-form-actions {
        align-items: stretch;
        min-width: 0;
      }
      .btn-submit {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="container" role="main" aria-label="Padel Party Reservation">
    <header>
      <div class="logo" aria-hidden="true"></div>
      <div class="title">SALY's</div>
    </header>

    <h1 class="main-title" aria-label="Padel Party Title">PADEL<br>PARTY</h1>

    <section class="event-details" aria-label="Event Details">
      <div><em>NOVEMBER 8, 2 PM</em></div>
      <div class="location">HOUSE OF PADEL, AGORA MALL<br>JAKARTA PUSAT</div>
    </section>

    <section class="images-row" aria-label="Padel images">
      <img src="padel.png" alt="Padel player lying on court with balls" />
    </section>

    <section class="rsvp-section" aria-label="RSVP Section">
      <div class="rsvp-row">
        <div class="rsvp-left">
          <h2>RSVP</h2>
        </div>
      
      </div>
      <form id="rsvpForm">
        <div class="rsvp-form-desktop-row">
          <div class="rsvp-form-fields">
            <label for="name" class="rsvp-form-label">Name :</label>
            <input type="text" id="name" name="name" autocomplete="name" required />
            <label for="phone" class="rsvp-form-label">HP Number :</label>
            <input type="tel" id="phone" name="phone" autocomplete="tel" required />
          </div>
          <div class="rsvp-form-actions">
            <label class="rsvp-form-label" style="margin-bottom:4px;">Join Party :</label>
            <div class="toggle-wrapper" role="radiogroup" aria-labelledby="join-label">
              <input type="radio" id="yes" name="join" value="yes" />
              <input type="radio" id="no" name="join" value="no" checked />
              <label for="yes" class="toggle-label">YES</label>
              <label for="no" class="toggle-label">NO</label>
              <span class="toggle-slider"></span>
            </div>
            <button type="submit" class="btn-submit">Submit</button>
          </div>
        </div>
      </form>
  
    </section>
    <!-- Download CSV button removed, now using Google Sheets integration -->
  </div>
  <footer></footer>
  <script>
    // Kirim data ke Google Apps Script Web App
    const form = document.getElementById('rsvpForm');
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const phone = document.getElementById('phone').value.trim();
      const join = document.getElementById('yes').checked ? 'YES' : 'NO';
      if(name && phone) {
        fetch('https://script.google.com/macros/s/AKfycbw9vJOOl0bdTR3kWRjnoa632auksquDNRQ-m2X_sJPNDynBPzAqFywquKzvUXFjOow4/exec', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({ name, phone, join })
        })
        .then(response => response.json())
        .then(data => {
          if(data.result === 'success') {
            alert('RSVP berhasil dikirim!');
            form.reset();
          } else {
            alert('Gagal mengirim RSVP. Coba lagi.');
          }
        })
        .catch(() => {
          alert('Gagal mengirim RSVP. Cek koneksi internet Anda.');
        });
      }
    });
  </script>
</body>
</html>
