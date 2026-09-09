# All-In-One
Where you find every service you need
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#111111">
<title>ALL IN ONE</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

body {
  background: #f5f5f5;
  color: #171717;
}

.app {
  max-width: 600px;
  margin: auto;
  min-height: 100vh;
  background: white;
  padding-bottom: 80px;
}

/* HEADER */
header {
  background: #111;
  color: white;
  padding: 25px 20px 28px;
  border-radius: 0 0 25px 25px;
}

.logo {
  font-size: 27px;
  font-weight: 900;
  letter-spacing: 1px;
}

.logo span {
  color: #e50914;
}

.tagline {
  margin-top: 6px;
  color: #ccc;
  font-size: 14px;
}

/* SEARCH */
.search-box {
  margin-top: 20px;
  background: white;
  border-radius: 14px;
  display: flex;
  align-items: center;
  padding: 4px 12px;
}

.search-box input {
  border: none;
  outline: none;
  flex: 1;
  padding: 13px 8px;
  font-size: 15px;
}

.search-icon {
  font-size: 20px;
}

/* CONTENT */
.content {
  padding: 20px;
}

.section-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 13px;
}

.section-title h2 {
  font-size: 19px;
}

.section-title small {
  color: #e50914;
}

/* CATEGORIES */
.categories {
  display: flex;
  gap: 10px;
  overflow-x: auto;
  padding-bottom: 10px;
}

.categories::-webkit-scrollbar {
  display: none;
}

.category {
  min-width: 95px;
  padding: 15px 8px;
  background: #f2f2f2;
  border-radius: 14px;
  text-align: center;
  cursor: pointer;
  border: 2px solid transparent;
}

.category.active {
  background: #111;
  color: white;
}

.category-icon {
  font-size: 25px;
  margin-bottom: 7px;
}

.category-name {
  font-size: 12px;
  font-weight: bold;
}

/* LOCATION */
.location {
  margin: 10px 0 22px;
  padding: 14px;
  background: #fff5f5;
  border-radius: 13px;
  color: #333;
  font-size: 14px;
}

/* BUSINESS CARDS */
.business-card {
  border: 1px solid #e6e6e6;
  border-radius: 18px;
  padding: 15px;
  margin-bottom: 15px;
  background: white;
  box-shadow: 0 4px 15px rgba(0,0,0,.05);
}

.business-top {
  display: flex;
  gap: 13px;
}

.business-logo {
  width: 58px;
  height: 58px;
  border-radius: 15px;
  background: #111;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  flex-shrink: 0;
}

.business-info {
  flex: 1;
}

.business-info h3 {
  font-size: 16px;
  margin-bottom: 4px;
}

.category-label {
  color: #777;
  font-size: 12px;
}

.rating {
  margin-top: 5px;
  font-size: 13px;
}

.verified {
  color: #1683ff;
  font-weight: bold;
}

.description {
  font-size: 13px;
  color: #666;
  margin: 13px 0;
  line-height: 1.4;
}

.buttons {
  display: flex;
  gap: 8px;
}

.btn {
  flex: 1;
  padding: 11px 7px;
  border-radius: 10px;
  border: none;
  font-weight: bold;
  cursor: pointer;
  font-size: 12px;
}

.btn-profile {
  background: #111;
  color: white;
}

.btn-whatsapp {
  background: #25d366;
  color: white;
}

.btn-call {
  background: #eee;
  color: #111;
}

/* FEATURED */
.featured {
  background: linear-gradient(135deg,#111,#292929);
  color: white;
  border-radius: 18px;
  padding: 18px;
  margin-bottom: 20px;
}

.featured p {
  color: #ccc;
  font-size: 13px;
  margin: 7px 0 13px;
}

.featured button {
  border: none;
  background: #e50914;
  color: white;
  padding: 11px 16px;
  border-radius: 10px;
  font-weight: bold;
}

/* EMPTY */
.no-results {
  text-align: center;
  padding: 35px 10px;
  color: #777;
}

/* BOTTOM NAV */
.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  max-width: 600px;
  height: 68px;
  background: white;
  border-top: 1px solid #ddd;
  display: flex;
  justify-content: space-around;
  align-items: center;
  z-index: 20;
}

.nav-item {
  text-align: center;
  font-size: 11px;
  color: #777;
  cursor: pointer;
}

.nav-item.active {
  color: #e50914;
  font-weight: bold;
}

.nav-icon {
  font-size: 21px;
  display: block;
  margin-bottom: 3px;
}

/* MODAL */
.modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,.65);
  z-index: 50;
  align-items: flex-end;
  justify-content: center;
}

.modal-content {
  background: white;
  width: 100%;
  max-width: 600px;
  border-radius: 25px 25px 0 0;
  padding: 25px;
  max-height: 85vh;
  overflow-y: auto;
}

.close {
  float: right;
  font-size: 25px;
  cursor: pointer;
}

.modal-content h2 {
  margin-bottom: 8px;
}

.modal-content p {
  color: #666;
  line-height: 1.5;
  margin-bottom: 15px;
}

.detail-button {
  width: 100%;
  padding: 14px;
  margin-top: 8px;
  border: none;
  border-radius: 12px;
  font-weight: bold;
  cursor: pointer;
}

.red {
  background: #e50914;
  color: white;
}

.dark {
  background: #111;
  color: white;
}

.green {
  background: #25d366;
  color: white;
}

/* DESKTOP */
@media (min-width: 601px) {
  body {
    background: #ddd;
  }

  .app {
    box-shadow: 0 0 30px rgba(0,0,0,.1);
  }
}
</style>
</head>

<body>

<div class="app">

<header>
  <div class="logo">ALL <span>IN ONE</span></div>
  <div class="tagline">Everything you need. All in one place.</div>

  <div class="search-box">
    <span class="search-icon">🔍</span>
    <input
      type="text"
      id="searchInput"
      placeholder="What service do you need?"
      oninput="searchBusinesses()"
    >
  </div>
</header>

<div class="content">

  <div class="location">
    📍 <strong>Your area</strong><br>
    Find trusted businesses and services near you.
  </div>

  <div class="featured">
    <strong>🚀 Grow your business with ALL IN ONE</strong>
    <p>Get discovered by customers looking for your services.</p>
    <button onclick="addBusiness()">+ Add Your Business</button>
  </div>

  <div class="section-title">
    <h2>Categories</h2>
    <small>View all</small>
  </div>

  <div class="categories">

    <div class="category active" onclick="filterCategory('All',this)">
      <div class="category-icon">✨</div>
      <div class="category-name">All</div>
    </div>

    <div class="category" onclick="filterCategory('Plumbing',this)">
      <div class="category-icon">🔧</div>
      <div class="category-name">Plumbing</div>
    </div>

    <div class="category" onclick="filterCategory('Electrical',this)">
      <div class="category-icon">⚡</div>
      <div class="category-name">Electrical</div>
    </div>

    <div class="category" onclick="filterCategory('Beauty',this)">
      <div class="category-icon">💇</div>
      <div class="category-name">Beauty</div>
    </div>

    <div class="category" onclick="filterCategory('Catering',this)">
      <div class="category-icon">🍽️</div>
      <div class="category-name">Catering</div>
    </div>

    <div class="category" onclick="filterCategory('Events',this)">
      <div class="category-icon">🎉</div>
      <div class="category-name">Events</div>
    </div>

    <div class="category" onclick="filterCategory('Cleaning',this)">
      <div class="category-icon">🧹</div>
      <div class="category-name">Cleaning</div>
    </div>

  </div>

  <br>

  <div class="section-title">
    <h2>Popular Services</h2>
    <small id="resultCount"></small>
  </div>

  <div id="businessList"></div>

</div>

</div>

<!-- BOTTOM NAV -->

<div class="bottom-nav">

  <div class="nav-item active" onclick="home()">
    <span class="nav-icon">🏠</span>
    Home
  </div>

  <div class="nav-item" onclick="focusSearch()">
    <span class="nav-icon">🔎</span>
    Search
  </div>

  <div class="nav-item" onclick="saved()">
    <span class="nav-icon">♡</span>
    Saved
  </div>

  <div class="nav-item" onclick="account()">
    <span class="nav-icon">👤</span>
    Account
  </div>

</div>


<!-- PROFILE MODAL -->

<div class="modal" id="profileModal">

  <div class="modal-content">

    <span class="close" onclick="closeModal()">×</span>

    <div id="profileContent"></div>

  </div>

</div>


<script>

const businesses = [

  {
    name: "Cape Fix Plumbing",
    category: "Plumbing",
    area: "Khayelitsha",
    rating: "4.9",
    icon: "🔧",
    verified: true,
    description: "Reliable household plumbing and emergency repairs.",
    phone: "0000000000"
  },

  {
    name: "BrightSpark Electrical",
    category: "Electrical",
    area: "Cape Town",
    rating: "4.8",
    icon: "⚡",
    verified: true,
    description: "Residential electrical installations and repairs.",
    phone: "0000000000"
  },

  {
    name: "Glow Beauty Studio",
    category: "Beauty",
    area: "Khayelitsha",
    rating: "4.7",
    icon: "💇",
    verified: false,
    description: "Hair, nails and beauty services.",
    phone: "0000000000"
  },

  {
    name: "Ubuntu Catering",
    category: "Catering",
    area: "Cape Town",
    rating: "4.9",
    icon: "🍽️",
    verified: true,
    description: "Catering for parties, weddings and ceremonies.",
    phone: "0000000000"
  },

  {
    name: "Perfect Day Events",
    category: "Events",
    area: "Gugulethu",
    rating: "4.8",
    icon: "🎉",
    verified: true,
    description: "Tents, chairs and event equipment for your special occasion.",
    phone: "0000000000"
  },

  {
    name: "FreshHome Cleaning",
    category: "Cleaning",
    area: "Cape Town",
    rating: "4.6",
    icon: "🧹",
    verified: false,
    description: "Professional home and office cleaning services.",
    phone: "0000000000"
  }

];

let currentCategory = "All";


function displayBusinesses(list) {

  const container = document.getElementById("businessList");

  container.innerHTML = "";

  document.getElementById("resultCount").innerText =
    list.length + " found";

  if (list.length === 0) {

    container.innerHTML = `
      <div class="no-results">
        <div style="font-size:40px">🔎</div>
        <h3>No businesses found</h3>
        <p>Try another service or search.</p>
      </div>
    `;

    return;
  }

  list.forEach((business,index) => {

    const card = document.createElement("div");

    card.className = "business-card";

    card.innerHTML = `

      <div class="business-top">

        <div class="business-logo">
          ${business.icon}
        </div>

        <div class="business-info">

          <h3>
            ${business.name}
            ${business.verified
              ? '<span class="verified"> ✓</span>'
              : ''}
          </h3>

          <div class="category-label">
            ${business.category} • ${business.area}
          </div>

          <div class="rating">
            ⭐ ${business.rating}
          </div>

        </div>

      </div>

      <div class="description">
        ${business.description}
      </div>

      <div class="buttons">

        <button
          class="btn btn-profile"
          onclick="viewProfile(${index})">
          View
        </button>

        <button
          class="btn btn-whatsapp"
          onclick="whatsapp('${business.name}')">
          WhatsApp
        </button>

        <button
          class="btn btn-call"
          onclick="callBusiness('${business.name}')">
          Call
        </button>

      </div>

    `;

    container.appendChild(card);

  });

}


function filterCategory(category,element) {

  currentCategory = category;

  document.querySelectorAll(".category")
    .forEach(c => c.classList.remove("active"));

  element.classList.add("active");

  searchBusinesses();

}


function searchBusinesses() {

  const search =
    document.getElementById("searchInput")
      .value
      .toLowerCase();

  let results = businesses.filter(business => {

    const matchesCategory =
      currentCategory === "All" ||
      business.category === currentCategory;

    const matchesSearch =
      business.name.toLowerCase().includes(search) ||
      business.category.toLowerCase().includes(search) ||
      business.area.toLowerCase().includes(search) ||
      business.description.toLowerCase().includes(search);

    return matchesCategory && matchesSearch;

  });

  displayBusinesses(results);

}


function viewProfile(index) {

  const business = businesses[index];

  document.getElementById("profileContent").innerHTML = `

    <div style="font-size:55px;margin-bottom:10px">
      ${business.icon}
    </div>

    <h2>${business.name}</h2>

    <p>
      ${business.verified
        ? "✓ Verified Business"
        : "Business listing"}
    </p>

    <p>
      📍 ${business.area}<br>
      🛠️ ${business.category}<br>
      ⭐ ${business.rating} rating
    </p>

    <p>${business.description}</p>

    <button
      class="detail-button green"
      onclick="whatsapp('${business.name}')">
      💬 WhatsApp Business
    </button>

    <button
      class="detail-button dark"
      onclick="callBusiness('${business.name}')">
      📞 Call Business
    </button>

    <button
      class="detail-button red"
      onclick="closeModal()">
      Close
    </button>

  `;

  document.getElementById("profileModal").style.display = "flex";

}


function closeModal() {

  document.getElementById("profileModal").style.display = "none";

}


function whatsapp(name) {

  alert(
    "WhatsApp demo activated for " +
    name +
    ".\n\nLater we will connect this to the real business WhatsApp number."
  );

}


function callBusiness(name) {

  alert(
    "Call demo activated for " +
    name +
    ".\n\nLater we will connect this to the real business phone number."
  );

}


function addBusiness() {

  document.getElementById("profileContent").innerHTML = `

    <h2>🚀 Add Your Business</h2>

    <p>
      Get your business discovered by customers using ALL IN ONE.
    </p>

    <input
      placeholder="Business name"
      style="width:100%;padding:14px;margin:7px 0;border:1px solid #ddd;border-radius:10px;"
    >

    <input
      placeholder="Service category"
      style="width:100%;padding:14px;margin:7px 0;border:1px solid #ddd;border-radius:10px;"
    >

    <input
      placeholder="Your area"
      style="width:100%;padding:14px;margin:7px 0;border:1px solid #ddd;border-radius:10px;"
    >

    <input
      placeholder="WhatsApp number"
      style="width:100%;padding:14px;margin:7px 0;border:1px solid #ddd;border-radius:10px;"
    >

    <button
      class="detail-button red"
      onclick="alert('Business registration demo submitted!')">
      Submit Business
    </button>

    <button
      class="detail-button dark"
      onclick="closeModal()">
      Cancel
    </button>

  `;

  document.getElementById("profileModal").style.display = "flex";

}


function focusSearch() {

  document.getElementById("searchInput").focus();

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

}


function saved() {

  alert(
    "Saved businesses will appear here.\n\nThis feature will be connected to user accounts in the next stage."
  );

}


function account() {

  document.getElementById("profileContent").innerHTML = `

    <h2>👤 My Account</h2>

    <p>
      Sign in to save businesses, leave reviews and manage your profile.
    </p>

    <button
      class="detail-button red"
      onclick="alert('Account system coming next!')">
      Create Account
    </button>

    <button
      class="detail-button dark"
      onclick="alert('Login system coming next!')">
      Login
    </button>

  `;

  document.getElementById("profileModal").style.display = "flex";

}


function home() {

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

}


/* START APP */

displayBusinesses(businesses);

</script>

</body>
</html>
