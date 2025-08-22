<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>קפה טאטיס – הזמנה אונליין</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Heebo:wght@400;600;800;900&display=swap" rel="stylesheet">
<style>
:root{--brand:#11b6b8;--brand-700:#0b9395;--bg:#f7f9fc;--card:#ffffff;--ink:#0f172a;--muted:#475569;--border:#e2e8f0;--accent:#eefdfd}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:Heebo,system-ui,Arial,sans-serif;line-height:1.55}
.appbar{position:sticky;top:0;z-index:20;background:var(--card);border-bottom:1px solid var(--border)}
.container{max-width:1200px;margin:0 auto;padding:14px}
.brandline{display:flex;align-items:center;gap:12px}
.logo{width:30px;height:30px;border-radius:8px;background:linear-gradient(135deg,var(--brand),#70e1e8)}
.title{font-weight:900;letter-spacing:.2px;font-size:clamp(20px,3.2vw,28px)}
.subtitle{color:var(--muted);font-size:13px}
.layout{display:grid;grid-template-columns:1fr;gap:16px;padding:10px}
@media(min-width:980px){.layout{grid-template-columns:1.7fr 1fr}}
.section{background:var(--card);border:1px solid var(--border);border-radius:16px;box-shadow:0 10px 20px rgba(2,6,23,.06)}
.section-head{padding:10px 14px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center}
.section-title{margin:0;font-weight:900;font-size:20px}
.section-body{padding:12px}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:8px}
.card{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;display:flex;flex-direction:column;height:100%}
.thumb{width:100%;height:80px;background:#f3f6f9;display:flex;align-items:center;justify-content:center}
.thumb img{width:100%;height:100%;object-fit:cover}
.card-body{padding:8px;display:grid;grid-template-rows:auto 1fr auto;gap:6px;height:100%}
.card h3{margin:0;font-size:13px;line-height:1.2}
.card p{margin:0;color:var(--muted);font-size:11px}
.price{font-weight:800;font-size:13px}
.actions{display:flex;align-items:center;justify-content:space-between;min-height:38px}
.btn{display:inline-flex;align-items:center;justify-content:center;gap:6px;cursor:pointer;border-radius:10px;border:1px solid transparent;padding:7px 10px;font-weight:800;font-size:12px}
.btn.primary{background:var(--brand);color:#fff}.btn.primary:hover{background:var(--brand-700)}
.btn.ghost{background:#fff;border-color:var(--border);color:var(--ink)}
.btn.link{background:transparent;color:var(--brand);border:none}
.cart{position:sticky;top:70px}
.cart-items{max-height:460px;overflow:auto}
.cart-row{display:grid;grid-template-columns:auto 1fr auto;gap:10px;align-items:center;padding:10px 12px;border-bottom:1px dashed var(--border)}
.qty{display:flex;align-items:center;gap:6px}
.qty button{width:28px;height:28px;border-radius:8px;border:1px solid var(--border);background:#fff;font-weight:900;cursor:pointer}
.summary{padding:10px;border-top:1px solid var(--border)}
.line{display:flex;justify-content:space-between;margin:6px 0;font-size:14px}
.total{font-size:18px;font-weight:900}
dialog{border:none;border-radius:18px;padding:0;width:min(900px,96%);box-shadow:0 26px 48px rgba(2,6,23,.28)}
dialog::backdrop{background:rgba(2,6,23,.5)}
.modal-head{padding:12px 14px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center}
.modal-body{padding:12px}
.group{margin:8px 0 14px}
.group h4{margin:0 0 8px;font-size:15px;font-weight:900}
.options{display:grid;grid-template-columns:repeat(2,1fr);gap:8px}
@media(min-width:720px){.options{grid-template-columns:repeat(3,1fr)}}
.opt{border:1px solid var(--border);border-radius:12px;padding:8px;display:flex;gap:8px;align-items:center;cursor:pointer;font-size:13px}
.opt input{margin:0 0 0 6px}
.opt.active{border-color:var(--brand);background:var(--accent);outline:2px solid rgba(14,165,166,.18)}
.helper{font-size:12px;color:var(--muted)}
form .field{display:grid;gap:6px}
input[type=text],input[type=email],input[type=tel],select,textarea{width:100%;padding:10px;border:1px solid var(--border);border-radius:10px;background:#fff;font-size:14px}
.two{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.three{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px}
@media(max-width:640px){.two,.three{grid-template-columns:1fr}}
.hr{height:1px;background:var(--border);margin:8px 0}
.cat-head{font-weight:900;font-size:18px;margin:6px 0 8px}
.card.no-thumb .card-body{padding-top:10px}
.muted{color:var(--muted);font-size:12px}
</style>
</head>
<body>
<header class="appbar">
  <div class="container" style="display:flex;justify-content:space-between;align-items:center">
    <div class="brandline">
      <div class="logo" aria-hidden="true"></div>
      <div>
        <div class="title">קפה טאטיס – הזמנה אונליין</div>
        <div class="subtitle">תפריט מקצועי, ברור וקריא</div>
      </div>
    </div>
    <button class="btn ghost" id="btnCheckoutHeader">לתשלום</button>
  </div>
</header>

<main class="container layout">
  <section class="section">
    <div class="section-head">
      <h2 class="section-title">תפריט</h2>
      <div class="subtitle">הקטגוריות מוצגות אחת מתחת לשנייה</div>
    </div>
    <div class="section-body">
      <div id="cat-salads">
        <div class="cat-head">סלטים</div>
        <div class="grid" id="grid-salads"></div>
      </div>

      <div id="cat-sandwiches" style="margin-top:14px">
        <div class="cat-head">כריכים</div>
        <div class="grid" id="grid-sandwiches"></div>
      </div>

      <div id="cat-desserts" style="margin-top:14px">
        <div class="cat-head">קינוחים</div>
        <div class="grid" id="grid-desserts"></div>
      </div>

      <div id="cat-drinks" style="margin-top:14px">
        <div class="cat-head">שתייה</div>
        <div class="grid" id="grid-drinks"></div>
      </div>
    </div>
  </section>

  <aside class="section cart" aria-label="עגלה">
    <div class="section-head">
      <h2 class="section-title">עגלה</h2>
      <button class="btn link" id="btnClearCart">נקה</button>
    </div>
    <div class="section-body">
      <div id="cartItems" class="cart-items"></div>
      <div class="summary">
        <div class="line"><span>סכום ביניים</span><strong id="subTotal">₪0</strong></div>
        <div class="line"><span>משלוח</span><strong id="deliveryFee">₪0</strong></div>
        <div class="hr"></div>
        <div class="line total"><span>סה"כ</span><strong id="grandTotal">₪0</strong></div>
        <div style="display:flex;gap:8px;margin-top:8px">
          <button class="btn primary" id="btnCheckout">לתשלום</button>
          <button class="btn ghost" id="btnBuildSalad">סלט בהרכבה</button>
        </div>
      </div>
    </div>
  </aside>
</main>

<!-- Salad Builder -->
<dialog id="dlgSalad" aria-label="סלט בהרכבה">
  <div class="modal-head">
    <strong>סלט בהרכבה</strong>
    <button class="btn link" onclick="dlgSalad.close()">סגור ✕</button>
  </div>
  <div class="modal-body">
    <form id="saladForm">
      <div class="group">
        <h4>גודל סלט</h4>
        <div class="options" data-name="size" data-type="radio">
          <label class="opt"><input type="radio" name="size" value="small" data-price="40"> 750 מ"ל – ₪40</label>
          <label class="opt"><input type="radio" name="size" value="large" data-price="46"> 1000 מ"ל – ₪46</label>
        </div>
      </div>
      <div class="group">
        <h4>מרכיבים (בחירה חופשית)</h4>
        <div class="options" data-name="ingredients" data-type="checkbox">
          <label class="opt"><input type="checkbox" value="מלפפון"> מלפפון</label>
          <label class="opt"><input type="checkbox" value="עגבנייה"> עגבנייה</label>
          <label class="opt"><input type="checkbox" value="חסה"> חסה</label>
          <label class="opt"><input type="checkbox" value="בצל ירוק"> בצל ירוק</label>
          <label class="opt"><input type="checkbox" value="כוסברה"> כוסברה</label>
          <label class="opt"><input type="checkbox" value="פטרוזליה"> פטרוזליה</label>
          <label class="opt"><input type="checkbox" value="נענע"> נענע</label>
          <label class="opt"><input type="checkbox" value="בזיליקום"> בזיליקום</label>
          <label class="opt"><input type="checkbox" value="עלי רוקט"> עלי רוקט</label>
          <label class="opt"><input type="checkbox" value="בצל סגול"> בצל סגול</label>
          <label class="opt"><input type="checkbox" value="פלפל ירוק"> פלפל ירוק</label>
          <label class="opt"><input type="checkbox" value="פלפל אדום"> פלפל אדום</label>
          <label class="opt"><input type="checkbox" value="פלפל צהוב"> פלפל צהוב</label>
          <label class="opt"><input type="checkbox" value="כרוב לבן"> כרוב לבן</label>
          <label class="opt"><input type="checkbox" value="גזר"> גזר</label>
          <label class="opt"><input type="checkbox" value="זיתים ירוקים"> זיתים ירוקים</label>
          <label class="opt"><input type="checkbox" value="זיתי קלמטה"> זיתי קלמטה</label>
          <label class="opt"><input type="checkbox" value="תירס"> תירס</label>
          <label class="opt"><input type="checkbox" value="פסטה מסולסלת"> פסטה מסולסלת</label>
          <label class="opt"><input type="checkbox" value="קינואה"> קינואה</label>
          <label class="opt"><input type="checkbox" value="עדשים שחורות"> עדשים שחורות</label>
          <label class="opt"><input type="checkbox" value="גרגירי חומוס"> גרגירי חומוס</label>
          <label class="opt"><input type="checkbox" value="בטטה אפויה בתנור"> בטטה אפויה בתנור</label>
          <label class="opt"><input type="checkbox" value='תפו"א אפוי'> תפו"א אפוי</label>
          <label class="opt"><input type="checkbox" value="סלק אפוי"> סלק אפוי</label>
          <label class="opt"><input type="checkbox" value="חמוציות"> חמוציות</label>
          <label class="opt"><input type="checkbox" value="שברי אגוזי מלך"> שברי אגוזי מלך</label>
          <label class="opt"><input type="checkbox" value="גרעיני חמנייה"> גרעיני חמנייה</label>
          <label class="opt"><input type="checkbox" value="גרעיני דלעת"> גרעיני דלעת</label>
        </div>
      </div>
      <div class="group">
        <h4>תוספות (אחת חינם)</h4>
        <div class="options" data-name="extras" data-type="checkbox">
          <label class="opt"><input type="checkbox" value="ביצה קשה" data-price="3"> ביצה קשה (+₪3)</label>
          <label class="opt"><input type="checkbox" value="טונה" data-price="6"> טונה (+₪6)</label>
          <label class="opt"><input type="checkbox" value="טונה במיונז" data-price="6"> טונה במיונז (+₪6)</label>
          <label class="opt"><input type="checkbox" value="גבינת פטה 5%" data-price="5"> גבינת פטה 5% (+₪5)</label>
          <label class="opt"><input type="checkbox" value="גבינה בולגרית 24%" data-price="6"> גבינה בולגרית 24% (+₪6)</label>
          <label class="opt"><input type="checkbox" value="טופו" data-price="5"> טופו (+₪5)</label>
        </div>
        <div class="helper">הבחירה היקרה מביניהן תחושב חינם.</div>
      </div>
      <div class="group">
        <h4>רטבים (2 כלולים, כל נוסף +₪3)</h4>
        <div class="options" data-name="dressings" data-type="checkbox" data-free="2" data-extra-price="3">
          <label class="opt"><input type="checkbox" value="טחינה"> טחינה</label>
          <label class="opt"><input type="checkbox" value="טחינה גולמית"> טחינה גולמית</label>
          <label class="opt"><input type="checkbox" value="שמן זית ולימון"> שמן זית ולימון</label>
          <label class="opt"><input type="checkbox" value="ויניגרט הדרים"> ויניגרט הדרים</label>
          <label class="opt"><input type="checkbox" value="רוטב שום"> רוטב שום</label>
          <label class="opt"><input type="checkbox" value="רוטב אלף האיים"> רוטב אלף האיים</label>
          <label class="opt"><input type="checkbox" value="לימון טרי"> לימון טרי</label>
        </div>
      </div>
      <div class="group">
        <h4>לחם (+₪4)</h4>
        <div class="options" data-name="bread" data-type="radio">
          <label class="opt"><input type="radio" name="bread" value="לחם כפרי" data-price="4" checked> לחם כפרי (+₪4)</label>
          <label class="opt"><input type="radio" name="bread" value="לחם דגנים" data-price="4"> לחם דגנים (+₪4)</label>
          <label class="opt"><input type="radio" name="bread" value="לחמניה לבנה" data-price="4"> לחמניה לבנה (+₪4)</label>
        </div>
      </div>
      <div class="hr"></div>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:10px">
        <div>מחיר משוער: <strong id="saladPrice">₪0</strong></div>
        <div style="display:flex;gap:8px">
          <button type="button" class="btn ghost" onclick="dlgSalad.close()">ביטול</button>
          <button type="submit" class="btn primary">הוסף לעגלה</button>
        </div>
      </div>
    </form>
  </div>
</dialog>

<!-- Checkout -->
<dialog id="dlgCheckout" aria-label="תשלום ומשלוח">
  <div class="modal-head">
    <strong>תשלום ומשלוח</strong>
    <button class="btn link" onclick="dlgCheckout.close()">סגור ✕</button>
  </div>
  <div class="modal-body">
    <form class="checkout" id="checkoutForm">
      <div class="two">
        <div class="field"><label>שם מלא</label><input required type="text" name="name" placeholder="שם ושם משפחה"></div>
        <div class="field"><label>טלפון</label><input required type="tel" name="phone" placeholder="050-0000000" pattern="0[0-9\\-]{8,10}"></div>
      </div>
      <div class="two">
        <div class="field"><label>אימייל</label><input type="email" name="email" placeholder="name@example.com"></div>
        <div class="field"><label>שיטת אספקה</label>
          <select name="deliveryMethod" id="deliveryMethod">
            <option value="pickup">איסוף עצמי (₪0)</option>
            <option value="mall">משלוח חינם (במתחם הקניון)</option>
            <option value="delivery">משלוח (₪15)</option>
          </select>
        </div>
      </div>
      <div id="addressFields" style="display:none">
        <div class="two">
          <div class="field"><label>עיר</label><input type="text" name="city" placeholder="קריית אונו"></div>
          <div class="field"><label>כתובת</label><input type="text" name="address" placeholder="רחוב ומספר"></div>
        </div>
        <div class="three">
          <div class="field"><label>קומה</label><input type="text" name="floor" placeholder="4"></div>
          <div class="field"><label>משרד / דירה</label><input type="text" name="office" placeholder="9"></div>
          <div class="field"><label>הערות לשליח</label><input type="text" name="notes" placeholder="קוד כניסה וכו'"></div>
        </div>
      </div>
      <div class="hr"></div>
      <div class="two">
        <div class="field"><label>אופן תשלום</label>
          <select name="payment" id="payment">
            <option value="cash">מזומן</option>
            <option value="card">אשראי</option>
          </select>
        </div>
        <div class="field"><label>סכום לתשלום</label><input type="text" id="payAmount" readonly></div>
      </div>
      <div id="cardFields" style="display:none">
        <div class="two">
          <div class="field"><label>מס' כרטיס</label><input type="text" name="cardNumber" inputmode="numeric" placeholder="0000 0000 0000 0000" maxlength="19"></div>
          <div class="field"><label>שם בעל הכרטיס</label><input type="text" name="cardName" placeholder="כפי שמופיע בכרטיס"></div>
        </div>
        <div class="three">
          <div class="field"><label>חודש</label><input type="text" name="expMonth" placeholder="MM" maxlength="2"></div>
          <div class="field"><label>שנה</label><input type="text" name="expYear" placeholder="YY" maxlength="2"></div>
          <div class="field"><label>CVV</label><input type="text" name="cvv" placeholder="000" maxlength="4"></div>
        </div>
      </div>
      <div class="hr"></div>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px">
        <div class="subtitle">ההזמנה תישלח אוטומטית לאחר אישור</div>
        <button type="submit" class="btn primary" id="btnPlaceOrder">בצע הזמנה</button>
      </div>
    </form>
  </div>
</dialog>

<script>
const DELIVERY_PRICE = { pickup: 0, mall: 0, delivery: 15 };
const SHEET_ENDPOINT = 'https://script.google.com/macros/s/AKfycbwCNUiHd-bjsYFmNM1RfjyY6F8eicp-iFO3ILoQrLdysfoJBFe821bmL_DTx8Eq1wFk/exec';

// Placeholder image
const PH = 'data:image/svg+xml;utf8,' + encodeURIComponent(`<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200"><rect width="100%" height="100%" fill="#eaf3f5"/><text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-family="Arial" font-size="18" fill="#0ea5a6">Cafe Tattis</text></svg>`);

// === תמונות לפי מזהה מוצר ===
const IMAGES = {
  greek: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-f9ea5fca.jpg",
  tuna: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-29-37-b867e557.jpg",
  pasta: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-c50de089.jpg",
  vegan: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-23bbe18c.jpg",
  sand_greenomelet: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-acd44cca.jpg",
  sand_omelet: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-0e958e62.jpg",
  sand_sabich: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-15-d7683a31.jpg",
  sand_tunaSalad: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-594ec9b2.jpg",
  sand_cheddar: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-16-491e300c.jpg",
  sand_eggSalad: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-16-44cc8424.jpg",
  sand_levivot: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-16-dee60627.jpg",
  sand_bulgarit_pesto: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-16-8a8ecd46.jpg",
  sand_salmon_smoked: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-16-f350c982.jpg",
  choc_balls_sprinkles: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-d7a551ad.jpg",
  choc_balls_coconut: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-11-17-d7a551ad.jpg",
  macarons: "https://cafetattis.weebly.com/uploads/1/0/3/4/10347808/whatsapp-2025-08-22-13-42-22-b166020b.jpg",
  carrot_cake: "",
  pritzi_cake: "",
  biscuit_cake: ""
};

const CATALOG = [
  {id:'build', name:'סלט בהרכבה', price:null, description:'בחרו גודל, מרכיבים, תוספות ורטבים – ללא שתייה', category:'builder', special:'builder', image:PH},

  // Salads
  {id:'greek', name:'סלט יווני', price:53, description:'עגבנייה, מלפפון, חסה, זיתי קלמטה, בצל סגול, גבינת פטה 5%', category:'salads', image:PH},
  {id:'tuna', name:'סלט טונה', price:57, description:'עגבנייה, מלפפון, חסה, בצל סגול/ירוק, תפו"א אפוי, טונה מיונז, פלפל אדום, ביצה', category:'salads', image:PH},
  {id:'vegan', name:'סלט טבעוני', price:53, description:'רוקט, גזר, כרוב, סלק אפוי, בטטה אפויה, קינואה, עדשים שחורות, טופו', category:'salads', image:PH},

  // Sandwiches
  {id:'sand_greenomelet', name:'חביתת ירק', price:25, description:'חביתת תרד ובצל ירוק, עם גבינת שמנת עשירה, חסה לליק רעננה ומלפפון ירוק קראנצ׳י.', category:'sandwiches', image:PH},
  {id:'sand_omelet', name:'חביתה קלאסית', price:25, description:'חביתה עסיסית עם גבינת שמנת נימוחה, חסה לליק טרייה ומלפפון ירוק פריך.', category:'sandwiches', image:PH},
  {id:'sand_sabich', name:'סביח חלומי', price:25, description:'טחינה עדינה, חציל אפוי בתנור, ביצה קשה ומלפפון חמוץ – שילוב מושלם של טעמים!', category:'sandwiches', image:PH},
  {id:'sand_tunaSalad', name:'סלט טונה קצוץ', price:25, description:'טונה במיונז איכותי, גמבה קצוצה ומלפפון חמוץ, חסה לליק רעננה ומקלוני גזר מתפצפצים.', category:'sandwiches', image:PH},
  {id:'sand_eggSalad', name:'סלט ביצים ביתי', price:25, description:'ביצים, בצל וקישוא מטוגנים קלות במיונז, על מצע של חסה לליק ובצל ירוק רענן.', category:'sandwiches', image:PH},
  {id:'sand_levivot', name:'לביבות ירק', price:35, description:'לביבות ירק מטוגנות קלות, עם טחינה עדינה, חסה לליק ומלפפון ירוק רענן.', category:'sandwiches', image:PH},
  {id:'sand_bulgarit_pesto', name:'בולגרית עם פסטו', price:35, description:'גבינה בולגרית 24% משובחת, ממרח פסטו עשיר, חסה לליק רעננה, עגבנייה טרייה ועלי בזיליקום.', category:'sandwiches', image:PH},
  {id:'sand_salmon_smoked', name:'כריך סלמון מעושן', price:35, description:'סלמון מעושן עם גבינת שמנת נימוחה, חסה לליק טרייה ומלפפון ירוק פריך.', category:'sandwiches', image:PH},

  // Desserts
  {id:'choc_balls_sprinkles', name:'מארז 3 כדורי שוקולד – ציפוי סוכריות', price:15, description:'כדורי שוקולד בציפוי סוכריות', category:'desserts', image:PH},
  {id:'choc_balls_coconut', name:'מארז 3 כדורי שוקולד – ציפוי קוקוס', price:15, description:'כדורי שוקולד בציפוי קוקוס', category:'desserts', image:PH},
  {id:'macarons', name:'מארז עוגיות מקרון', price:29, description:'מבחר טעמים', category:'desserts', image:PH},
  {id:'carrot_cake', name:'עוגת גזר', price:38, description:'עוגת פס שלמה', category:'desserts', image:PH},
  {id:'pritzi_cake', name:'עוגת פריצי', price:38, description:'עוגת פס שלמה', category:'desserts', image:PH},
  {id:'biscuit_cake', name:'עוגת ביסקוויטים', price:42, description:'עוגת פס שלמה', category:'desserts', image:PH},

  // Drinks – no images
  {id:'drink_xl', name:'XL', price:10, description:'פחית', category:'drinks', noImage:true},
  {id:'drink_grape_can', name:'פחית מיץ ענבים', price:10, description:'פחית', category:'drinks', noImage:true},
  {id:'drink_peach_can', name:'פחית מיץ אפרסק', price:10, description:'פחית', category:'drinks', noImage:true},
  {id:'drink_cola_bottle', name:'קוקה קולה 0.5 ל׳ בקבוק', price:12, description:'בקבוק 500 מ״ל', category:'drinks', noImage:true},
  {id:'drink_cola_zero_bottle', name:'קוקה קולה זירו 0.5 ל׳ בקבוק', price:12, description:'בקבוק 500 מ״ל', category:'drinks', noImage:true},
  {id:'drink_cola_can', name:'פחית קוקה קולה', price:10, description:'330 מ״ל', category:'drinks', noImage:true},
  {id:'drink_cola_zero_can', name:'פחית קוקה קולה זירו', price:10, description:'330 מ״ל', category:'drinks', noImage:true},
  {id:'drink_sprite_can', name:'פחית ספרייט', price:10, description:'330 מ״ל', category:'drinks', noImage:true},
  {id:'drink_sprite_zero_can', name:'פחית ספרייט זירו', price:10, description:'330 מ״ל', category:'drinks', noImage:true},
  {id:'drink_soda', name:'סודה', price:9, description:'בקבוק', category:'drinks', noImage:true},
  {id:'drink_flavored_peach', name:'מים בטעם אפרסק', price:10, description:'בקבוק', category:'drinks', noImage:true},
  {id:'drink_flavored_apple', name:'מים בטעם תפוח', price:10, description:'בקבוק', category:'drinks', noImage:true},
  {id:'drink_flavored_grape', name:'מים בטעם ענבים', price:10, description:'בקבוק', category:'drinks', noImage:true},
  {id:'drink_prigat_grapefruit', name:'מיץ אשכוליות פריגת', price:10, description:'בקבוק/פחית', category:'drinks', noImage:true},
  {id:'drink_nestea_500', name:'נסטי 0.5 ל׳', price:10, description:'בקבוק 500 מ״ל', category:'drinks', noImage:true},
  {id:'drink_mey_eden', name:'מי עדן', price:10, description:'בקבוק', category:'drinks', noImage:true},
  {id:'drink_neviot', name:'מי נביעות', price:10, description:'בקבוק', category:'drinks', noImage:true},
  {id:'fresh_orange', name:'סחוט טרי תפוז 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
  {id:'fresh_pomegranate', name:'סחוט טרי רימון 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
  {id:'fresh_matcha_spirulina', name:'סחוט טרי מאצ׳ה ספירולינה 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
  {id:'fresh_carrot', name:'סחוט טרי גזר 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
  {id:'fresh_apple', name:'סחוט טרי תפוח 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
  {id:'fresh_lemonade', name:'סחוט טרי לימונדה 250 מ״ל', price:16, description:'מיץ סחוט טרי', category:'drinks', noImage:true},
];

const state = { cart: [], deliveryMethod:'pickup' };
const el = (s)=>document.querySelector(s);
const elCartItems = el('#cartItems');
const elSubTotal = el('#subTotal');
const elDeliveryFee = el('#deliveryFee');
const elGrandTotal = el('#grandTotal');
const ils = (n)=>'₪'+(n.toFixed(0));
const save = ()=> localStorage.setItem('tattis_cart', JSON.stringify(state));
const load = ()=> { try{ Object.assign(state, JSON.parse(localStorage.getItem('tattis_cart'))||{});}catch{} renderCart(); };
const sameMeta = (a,b)=> JSON.stringify(a||{})===JSON.stringify(b||{});

function addToCart(item){
  const i = state.cart.findIndex(x=> x.id===item.id && sameMeta(x.meta,item.meta));
  if(i>-1) state.cart[i].qty += item.qty||1; else state.cart.push({...item, qty:item.qty||1});
  renderCart(); save();
}
function removeFromCart(idx){ state.cart.splice(idx,1); renderCart(); save(); }
function changeQty(idx,delta){ const it=state.cart[idx]; if(!it) return; it.qty=Math.max(1,it.qty+delta); renderCart(); save(); }
function totals(){
  const sub = state.cart.reduce((s,it)=>s+it.price*it.qty,0);
  const delivery = state.deliveryMethod==='delivery' ? 15 : 0;
  const total = Math.max(0, sub+delivery);
  return {sub,delivery,total};
}
function metaText(m){
  if(!m) return '';
  const p=[];
  if(m.size) p.push(`גודל: ${m.size==='small'?'750 מ"ל':'1000 מ"ל'}`);
  if(m.ingredients?.length) p.push(`מרכיבים: ${m.ingredients.join(', ')}`);
  if(m.extras?.length) p.push(`תוספות: ${m.extras.join(', ')}`);
  if(m.dressings?.length) p.push(`רטבים: ${m.dressings.join(', ')}`);
  if(m.bread) p.push(`לחם: ${m.bread}`);
  return p.join(' | ');
}
function renderCart(){
  elCartItems.innerHTML='';
  if(state.cart.length===0){ elCartItems.innerHTML = '<div class="subtitle" style="padding:8px 2px">העגלה ריקה. הוסיפו פריטים מהתפריט →</div>'; }
  state.cart.forEach((it,i)=>{
    const row=document.createElement('div'); row.className='cart-row';
    row.innerHTML = `
      <div class="qty">
        <button aria-label="הפחת" onclick="changeQty(${i},-1)">–</button>
        <div>${it.qty}</div>
        <button aria-label="הוסף" onclick="changeQty(${i},+1)">+</button>
      </div>
      <div>
        <div style="font-weight:800">${it.name}</div>
        ${it.meta?`<div class="subtitle" style="font-size:12px">${metaText(it.meta)}</div>`:''}
      </div>
      <div style="text-align:end">
        <div>${ils(it.price*it.qty)}</div>
        <button class="btn link" onclick="removeFromCart(${i})">הסר</button>
      </div>`;
    elCartItems.appendChild(row);
  });
  const t=totals();
  elSubTotal.textContent = ils(t.sub);
  elDeliveryFee.textContent = ils(t.delivery);
  elGrandTotal.textContent = ils(t.total);
  document.getElementById('payAmount')?.value && (document.getElementById('payAmount').value = ils(t.total));
}

function makeCard(p){
  const wrap = document.createElement('div');
  wrap.className='card' + (p.noImage ? ' no-thumb' : '');
  const isBuilder = p.special==='builder';
  const imgSrc = p.noImage ? '' : (IMAGES[p.id] || p.image || PH);
  wrap.innerHTML = `
    ${p.noImage ? '' : `<div class="thumb"><img alt="${p.name}" src="${imgSrc}"></div>`}
    <div class="card-body">
      <h3>${p.name}</h3>
      <p>${p.description||''}</p>
      <div class="actions">
        <div class="price">${p.price? ils(p.price) : ''}</div>
        <button class="btn ${isBuilder ? 'ghost' : 'primary'}" ${isBuilder ? 'data-builder="1"' : `data-id="${p.id}"`}>
          ${isBuilder ? 'פתח אפשרויות' : 'הוסף'}
        </button>
      </div>
    </div>`;
  return wrap;
}
function renderCategories(){
  const saladsGrid = document.getElementById('grid-salads');
  const sandwichesGrid = document.getElementById('grid-sandwiches');
  const dessertsGrid = document.getElementById('grid-desserts');
  const drinksGrid = document.getElementById('grid-drinks');
  saladsGrid.innerHTML=''; sandwichesGrid.innerHTML=''; dessertsGrid.innerHTML=''; drinksGrid.innerHTML='';
  saladsGrid.appendChild(makeCard(CATALOG.find(x=>x.special==='builder')));
  CATALOG.filter(x=>x.category==='salads').forEach(p=> saladsGrid.appendChild(makeCard(p)));
  CATALOG.filter(x=>x.category==='sandwiches').forEach(p=> sandwichesGrid.appendChild(makeCard(p)));
  CATALOG.filter(x=>x.category==='desserts').forEach(p=> dessertsGrid.appendChild(makeCard(p)));
  CATALOG.filter(x=>x.category==='drinks').forEach(p=> drinksGrid.appendChild(makeCard(p)));
  document.querySelectorAll('[data-builder]').forEach(btn=> btn.addEventListener('click', ()=> dlgSalad.showModal()));
  document.querySelectorAll('button[data-id]').forEach(btn=>{
    btn.addEventListener('click', ()=>{
      const it = CATALOG.find(x=>x.id===btn.dataset.id);
      addToCart({id:it.id, name:it.name, price:it.price});
    });
  });
}

// Builder pricing
const dlgSalad = document.getElementById('dlgSalad');
const saladForm = document.getElementById('saladForm');
const saladPriceEl = document.getElementById('saladPrice');
function calcSaladPrice(){
  let price=0;
  const sizeEl = saladForm.querySelector('input[name="size"]:checked');
  if(sizeEl) price += Number(sizeEl.dataset.price||0);
  const extrasWrap = saladForm.querySelector('[data-name="extras"]');
  if(extrasWrap){
    const chosen=[...extrasWrap.querySelectorAll('input:checked')];
    if(chosen.length){
      const vals = chosen.map(i=>Number(i.dataset.price||0));
      const sum = vals.reduce((a,b)=>a+b,0);
      const max = Math.max(...vals);
      price += (sum - max);
    }
  }
  const dWrap = saladForm.querySelector('[data-name="dressings"]');
  const free = Number(dWrap?.dataset.free||2), add = Number(dWrap?.dataset.extraPrice||3);
  const count = saladForm.querySelectorAll('[data-name="dressings"] input:checked').length;
  price += Math.max(0, count - free) * add;
  const breadEl = saladForm.querySelector('input[name="bread"]:checked');
  if(breadEl){ price += Number(breadEl.dataset.price||0); }
  saladPriceEl.textContent = ils(price);
  return price;
}
function collectSalad(){
  const meta={
    size:(saladForm.querySelector('input[name="size"]:checked')||{}).value,
    ingredients:[...saladForm.querySelectorAll('[data-name="ingredients"] input:checked')].map(x=>x.value),
    extras:[...saladForm.querySelectorAll('[data-name="extras"] input:checked')].map(x=>x.value),
    dressings:[...saladForm.querySelectorAll('[data-name="dressings"] input:checked')].map(x=>x.value),
    bread:(saladForm.querySelector('input[name="bread"]:checked')||{}).value,
  };
  const price=calcSaladPrice();
  return { id:'custom-'+JSON.stringify(meta), name:'סלט בהרכבה', price, meta };
}
document.querySelectorAll('.options').forEach(g=>{
  g.addEventListener('change',()=>{
    g.querySelectorAll('.opt').forEach(o=>{
      const i=o.querySelector('input');
      o.classList.toggle('active', i.type==='radio'? i.checked : i.checked);
    });
    calcSaladPrice();
  })
});
saladForm.addEventListener('submit',e=>{
  e.preventDefault();
  if(!saladForm.querySelector('input[name="size"]:checked')){ alert('בחרו גודל סלט'); return; }
  addToCart(collectSalad()); saladForm.reset();
  document.querySelectorAll('.opt').forEach(o=>o.classList.remove('active'));
  saladPriceEl.textContent='₪0'; dlgSalad.close();
});

// Checkout
const dlgCheckout = document.getElementById('dlgCheckout');
const checkoutForm = document.getElementById('checkoutForm');
const deliveryEl = document.getElementById('deliveryMethod');
const addressFields = document.getElementById('addressFields');
const paymentEl = document.getElementById('payment');
const cardFields = document.getElementById('cardFields');
function openCheckout(){ if(state.cart.length===0){ alert('העגלה ריקה'); return;} document.getElementById('payAmount').value = ils(totals().total); dlgCheckout.showModal(); }
document.getElementById('btnCheckout').addEventListener('click', openCheckout);
document.getElementById('btnCheckoutHeader').addEventListener('click', openCheckout);
document.getElementById('btnBuildSalad').addEventListener('click', ()=> dlgSalad.showModal());
document.getElementById('btnClearCart').addEventListener('click', ()=>{ if(confirm('לנקות את העגלה?')){ state.cart=[]; renderCart(); save(); }});
deliveryEl.addEventListener('change', ()=>{
  state.deliveryMethod = deliveryEl.value;
  addressFields.style.display = (state.deliveryMethod==='mall' || state.deliveryMethod==='delivery')? '' : 'none';
  const t=totals();
  document.getElementById('payAmount').value = ils(t.total);
  document.getElementById('deliveryFee').textContent = ils(t.delivery);
  document.getElementById('grandTotal').textContent = ils(t.total);
});
paymentEl.addEventListener('change', ()=>{ cardFields.style.display = paymentEl.value==='card' ? '' : 'none'; });
checkoutForm.addEventListener('submit', async (e)=>{
  e.preventDefault();
  const data = Object.fromEntries(new FormData(checkoutForm).entries());
  const t = totals();
  const payload = {
    meta:{ ts:new Date().toISOString(), source:'web-cart-pro-v8-images-final' },
    customer:data,
    deliveryMethod: state.deliveryMethod,
    items: state.cart.map(it=>({id:it.id,name:it.name,qty:it.qty,price:it.price,meta:it.meta||null})),
    totals:{ sub: t.sub, delivery: t.delivery, total: t.total },
  };
  const btn = document.getElementById('btnPlaceOrder'); btn.disabled=true; btn.textContent='שולח...';
  try{
    const res = await fetch(SHEET_ENDPOINT,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify(payload)});
    if(!res.ok) throw new Error('שגיאה בשליחה');
    alert('הזמנה התקבלה! תודה');
    state.cart=[]; renderCart(); save();
    checkoutForm.reset(); cardFields.style.display='none'; addressFields.style.display='none'; dlgCheckout.close();
  }catch(err){ alert('לא ניתן לשלוח כרגע. בדקו חיבור/סקריפט.'); }
  finally{ btn.disabled=false; btn.textContent='בצע הזמנה'; }
});

(function init(){
  renderCategories();
  load();
})();
</script>
</body>
</html>
