<!DOCTYPE html>
<html>
    <head>
    <!--webpage name-->
        <title>Property Management</title>
    </head>
    <body>
    <!--heading to show when webpage opens-->
     <h1 style="font-family: 'Arial black'; font-size: 50px; color: black; text-align: center;">PROPERTY MANAGEMENT SYSTEM</h1> 
     <br>

<!-- LOGIN PAGE - this will show first -->
    <div id="loginPage" style="text-align: center; margin-top: 100px; background: #ccc; padding: 30px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto;">
        <h2>Login</h2>
        <input id="username" type="text" placeholder="Enter username" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
        <input id="password" type="password" placeholder="Enter password" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
        <button onclick="login()" style="background: gold; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 10px; cursor: pointer; font-weight: bold; width: 95%;">LOGIN</button>
        <p id="error" style="color: red;"></p>
    </div>

    
    <!--main system - hidden at first-->

     <div id="mainSystem" style="display: none; justify-content: center; align-items: center; margin-top: 130px">
     <button onclick="openMenu()"style="background-color: gold; color: black; padding: 10px 20px; border-radius: 8px; border: none; cursor: pointer; font-size: 40px; margin-left: 350px">
  <b> Our Services </b>
</button>
</div>

  <!--hidden menu style-->
   <div id="myMenu" style="display: none; text-align: center; margin-top: 20px; background: #f5f5f5; padding: 20px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto;">
    <p style="font-size: 20px; font-weight: bold;">We Offer:</p>
    
   <!--hidden menu-->
        <p><button onclick="openPropertyForm()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Add property</button></p> 
        
        <p><button onclick="viewProperties()"style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: margin-top: 10px; cursor: pointer;">View properties</button></p>

        <p><button onclick="openLandlordForm()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Add landlord</button></p>
        
        <p><button onclick="openTenantForm()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Add tenant</button></p>
        
        <p><button onclick="openAssign()"  style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Assign tenant to property</button></p>

        <p><button onclick="openRentForm()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Record rent payment</button></p>
        
        <p><button onclick="viewPayments()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">View rent payment</button></p>
        
        <p><button onclick="openSearch()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Search property</button></p>
        
        <p><button onclick="openReport()" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid red; cursor: pointer;">Generate report</button></p>
        
        <button onclick="closeMenu()" style="background: red; color: white; padding: 8px 15px; border: none; border-radius: 5px; margin-top: 15px; cursor: pointer;">Close</button>
    <button onclick="logout()" style="background: red; color: white; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 20px; cursor: pointer; font-weight: bold; width: 100%;">LOGOUT</button>
    </div>

<!-- Add Property Form - hidden until clicked -->

<div id="propertyForm" style="display: none; text-align: center; margin-top: 20px; background: white; padding: 20px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto; border: 2px solid gold;">

    <h3>Add New Property</h3>

    <input id="propId" type="text" placeholder="Property ID" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <input id="propAddress" type="text" placeholder="Property Address" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <input id="propType" type="text" placeholder="Property Type" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <input id="propBed" type="number" placeholder="no. of bedrooms" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <input id="propRent" type="number" placeholder="Monthly rent(Naira)" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <input id="propStatus" type="text" placeholder="Availability status" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>

    <button onclick="saveProperty()" style="background: gold; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 10px; cursor: pointer; font-weight: bold;">Save Property</button><br>

    <button onclick="closePropertyForm()" style="background: red; color: white; padding: 8px 15px; border: none; border-radius: 5px; margin-top: 10px; cursor: pointer;">Close</button> </div>

     <!--property form has now been added-->   
   
        <!--to make properties to appear when view properties is clicked-->
        
    <div id="viewPropertiesDiv" style="display: none; text-align: center; margin-top: 20px; background: #f5f5f5; padding: 20px; border-radius: 10px; width: 350px; margin-left: auto; margin-right: auto;">   

    <h3>Saved Properties</h3>

    <div id="propertiesList"></div>
    <button onclick="closePropertiesView()" style="background:red; color:white; padding:8px 15px; border:none; border-radius:5px; margin-top:15px; cursor:pointer;">Close</button>
    </div> 
    
  <!--add landlord form - hidden until clicked-->
      
    
    <div id="landlordForm" style="display: none; text-align: center; margin-top: 20px; background: white; padding: 20px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto; border: 2px solid gold;">
    
    <h3>Add New landlord</h3>
    
    <input id="lordId" type="text" placeholder="Landlord ID" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="lordName" type="text" placeholder="Full name" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="lordNumber" type="text" placeholder="Phone no." style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="lordMail" type="text" placeholder="Email address" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="lordProp" type="number" placeholder="property owned(ID)" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    
    <button onclick="saveLandlord()" style="background: gold; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 10px; cursor: pointer; font-weight: bold;">Save Landlord</button><br>
    
    <button onclick="closeLandlordForm()" style="background: red; color: white; padding: 8px 15px; border: none; border-radius: 5px; margin-top: 10px; cursor: pointer;">Close</button> </div>

  <!--add tenant form - hidden until clicked-->
      
    
    <div id="tenantForm" style="display: none; text-align: center; margin-top: 20px; background: white; padding: 20px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto; border: 2px solid gold;">
    
    <h3>Add new tenant</h3>
    
    <input id="tenantId" type="text" placeholder="Tenant ID" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="tenantName" type="text" placeholder="Full name" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="tenantNumber" type="text" placeholder="Phone no." style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="tenantMail" type="text" placeholder="Email address" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="tenantProp" type="number" placeholder="property occupied(ID)" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    
    <button onclick="saveTenant()" style="background: gold; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 10px; cursor: pointer; font-weight: bold;">Save Tenant</button><br>
    
    <button onclick="closeTenantForm()" style="background: red; color: white; padding: 8px 15px; border: none; border-radius: 5px; margin-top: 10px; cursor: pointer;">Close</button> </div>

<!-- ASSIGN TENANT TO PROPERTY - with filter -->

<div id="assignDiv" style="display:none; text-align:center; margin-top:20px; background:white; padding:20px; border-radius:10px; width:350px; margin:auto; border:2px solid gold;">

  <h3>Assign Tenant to Property</h3>

  <input id="assignTenantId" type="text" placeholder="Enter Tenant ID" style="width:90%; padding:10px; margin:5px; border-radius:5px; border:1px solid #ccc;"><br>

  <input id="assignPrice" type="number" placeholder="Max Price in Naira(e.g 200000)" style="width:90%; padding:10px; margin:5px; border-radius:5px; border:1px solid #ccc;"><br>

  <input id="assignBed" type="number" placeholder="No. of Bedrooms required" style="width:90%; padding:10px; margin:5px; border-radius:5px; border:1px solid #ccc;"><br>

  
  <button onclick="filterAssign()" style="background:gold; border:none; padding:10px 20px; border-radius:5px; margin-top:10px; cursor:pointer; font-weight:bold;">Search Houses</button><br>

  <div id="assignResult" style="margin-top:15px; text-align:left;"></div>

  <button onclick="closeAssign()" style="background:red; color:white; padding:8px 15px; border:none; border-radius:5px; margin-top:10px; cursor:pointer;">Close</button>
</div>

  <!--rent record form - hidden until clicked-->
      
    
    <div id="rentForm" style="display: none; text-align: center; margin-top: 20px; background: white; padding: 20px; border-radius: 10px; width: 300px; margin-left: auto; margin-right: auto; border: 2px solid gold;">
    
    <h3>Record rent payment</h3>
    
    <input id="tId" type="text" placeholder="Tenant ID" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="pId" type="text" placeholder="Property ID" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="amount" type="text" placeholder="Amount paid (Naira)" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="paymentDate" type="text" placeholder="Payment date" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    <input id="paymentStatus" type="number" placeholder="status" style="width: 90%; padding: 10px; margin: 5px; border-radius: 5px; border: 1px solid #ccc;"><br>
    
    
    <button onclick="recordRent()" style="background: gold; border: none; padding: 10px 20px; border-radius: 5px; margin-top: 10px; cursor: pointer; font-weight: bold;">Record payment</button><br>
    
    <button onclick="closeRentForm()" style="background: red; color: white; padding: 8px 15px; border: none; border-radius: 5px; margin-top: 10px; cursor: pointer;">Close</button> </div>

<!--to make payments to appear when view rent payments is clicked-->
        
    <div id="viewPaymentsDiv" style="display: none; text-align: center; margin-top: 20px; background: #f5f5f5; padding: 20px; border-radius: 10px; width: 350px; margin-left: auto; margin-right: auto;">   

    <h3>Rent payment history</h3>

    <div id="paymentHistory"></div>
    <button onclick="closePaymentsView()" style="background:red; color:white; padding:8px 15px; border:none; border-radius:5px; margin-top:15px; cursor:pointer;">Close</button>
    </div> 
    

              <!-- search code -->

<div id="searchDiv" style="display:none; text-align:center; margin-top:20px; background:white; padding:20px; border-radius:10px; width:300px; margin:auto; border:2px solid gold;">

  <h3>Search Property</h3>

  <input id="searchInput" type="text" placeholder="Enter ID or Address" style="width:90%; padding:10px; margin:5px; border-radius:5px; border:1px solid #ccc;"><br>

  <button onclick="searchProperty()" style="background:gold; border:none; padding:10px 20px; border-radius:5px; margin-top:10px; cursor:pointer; font-weight:bold;">Search</button><br>

  <div id="searchResult" style="margin-top:15px; text-align:left;"></div>
  <button onclick="closeSearch()" style="background:red; color:white; padding:8px 15px; border:none; border-radius:5px; margin-top:10px; cursor:pointer;">Close</button>
</div>

       <!-- REPORT Generation code -->

<div id="reportDiv" style="display:none; text-align:center; margin-top:20px; background:white; padding:20px; border-radius:10px; width:350px; margin:auto; border:2px solid gold;">

  <h3>PROPERTY REPORT</h3>

  <div id="reportResult" style="text-align:left; background:#f5f5f5; padding:15px; border-radius:5px;"></div>

  <button onclick="closeReport()" style="background:red; color:white; padding:8px 15px; border:none; border-radius:5px; margin-top:15px; cursor:pointer;">Close</button>
</div>

<script>
// SET YOUR OWN USERNAME AND PASSWORD HERE
        let correctName = "admin";
        let correctPassword = "1234";

        function login() {
            let name = document.getElementById("username").value;
            let pass = document.getElementById("password").value;

            if (name == correctName && pass == correctPassword) {
                // if correct, hide login and show main system
                document.getElementById("loginPage").style.display = "none";
                document.getElementById("mainSystem").style.display = "block";
            } else {
                document.getElementById("error").innerHTML = "Wrong name or password! Try again";
            }
        }

function openMenu() { document.getElementById("myMenu").style.display = "block";
}

function closeMenu() { document.getElementById("myMenu").style.display = "none";
}

function logout() { document.getElementById("loginPage").style.display = "block";
    document.getElementById("mainSystem").style.display = "none";

document.getElementById("myMenu").style.display = "none";
}

function openPropertyForm() { document.getElementById("propertyForm").style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closePropertyForm() { document.getElementById("propertyForm").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

// This array will hold all properties
let properties = JSON.parse(localStorage.getItem("myProperties")) || [];
// means new properties added will be stored in local storage(browser storage).
function saveProperty() {
    let newProp = {
        id: document.getElementById("propId").value,
        address: document.getElementById("propAddress").value,
        type: document.getElementById("propType").value,
        bed: document.getElementById("propBed").value,
        rent: document.getElementById("propRent").value,
        status: document.getElementById("propStatus").value
    };
// if user does not input property ID and address,  dont save.
    if(newProp.id == "" || newProp.address == ""){
        alert("please input Property ID and Address");
        return;
    }

    properties.push(newProp);
    localStorage.setItem("myProperties", JSON.stringify(properties));
    
    alert("Property Saved! ");
    
    // after saving,clear form for another input
    document.getElementById("propId").value = "";
    document.getElementById("propAddress").value = "";
    document.getElementById("propType").value = "";
    document.getElementById("propBed").value = "";
    document.getElementById("propRent").value = "";
    document.getElementById("propStatus").value = "";

    closePropertyForm();
}

function viewProperties() {
    let display = document.getElementById("viewPropertiesDiv");
    let list = document.getElementById("propertiesList");
    
    list.innerHTML=""// clear old ones first.
    
    // if no properties have been saved yet,
    if(properties.length == 0){
        list.innerHTML += "<p>No property saved yet</p>";
    } else {
        properties.forEach((p, index) => {
    // how to display saved properties       
 list.innerHTML += `
                <div style="border:1px solid gold; margin:10px; padding:10px; border-radius:5px; background:white; text-align:left;">
                    <b>ID:</b> ${p.id} <br>
                    <b>Address:</b> ${p.address} <br>
                    <b>Type:</b> ${p.type}<br>
                               <b>Rooms:</b> ${p.bed} bedrooms<br>
                    <b>Rent:</b> ${p.rent} Naira <br>
                    <b>Status:</b> ${p.status}
                </div>
            `;
        });
    }
    display.style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closePropertiesView(){
    document.getElementById("viewPropertiesDiv").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

function openLandlordForm() { document.getElementById("landlordForm").style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closeLandlordForm() { document.getElementById("landlordForm").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

//to allow for saving of landlords

// This array will hold all properties
let landlords= JSON.parse(localStorage.getItem("myLandlords")) || [];
// means new properties added will be stored in local storage(browser storage).

function saveLandlord() {
    let newLord = {
        id: document.getElementById("lordId").value,
        Name: document.getElementById("lordName").value,
        Tel: document.getElementById("lordNumber").value,
        Email: document.getElementById("lordMail").value,
        Properties: document.getElementById("lordProp").value,
    };
// if user does not input landlord id and name,  dont save.
    if(newLord.id == "" || newLord.Name == ""){
        alert("please input Landlord ID and name");
        return;
    }

    landlords.push(newLord);
    localStorage.setItem("myLandlords", JSON.stringify(landlords));
    
    alert("Landlord Saved! ");
    
    // after saving,clear form for another input
    document.getElementById("lordId").value = "";
    document.getElementById("lordName").value = "";
    document.getElementById("lordNumber").value = "";
    document.getElementById("lordMail").value = "";
    document.getElementById("lordProp").value = "";

    closeLandlordForm();
}

function openTenantForm() { document.getElementById("tenantForm").style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closeTenantForm() { document.getElementById("tenantForm").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

//to allow for saving of tenants

// This array will hold all properties
let tenants= JSON.parse(localStorage.getItem("myTenants")) || [];
// means new properties added will be stored in local storage(browser storage).

function saveTenant() {
    let newTenant = {
        id: document.getElementById("tenantId").value,
        Name: document.getElementById("tenantName").value,
        Tel: document.getElementById("tenantNumber").value,
        Email: document.getElementById("tenantMail").value,
        Property: document.getElementById("tenantProp").value,
    };
// if user does not input tenant id and name,  dont save.
    if(newTenant.id == "" || newTenant.Name == ""){
        alert("please input Tenant ID and name");
        return;
    }

    tenants.push(newTenant);
    localStorage.setItem("myTenants", JSON.stringify(tenants));
    
    alert("Tenant Saved! ");
    
    // after saving,clear form for another input
    document.getElementById("tenantId").value = "";
    document.getElementById("tenantName").value = "";
    document.getElementById("tenantNumber").value = "";
    document.getElementById("tenantMail").value = "";
    document.getElementById("tenantProp").value = "";

    closeTenantForm();
}

//assigning tenant to property:functions 

function openAssign(){
  document.getElementById("assignDiv").style.display = "block";
  document.getElementById("myMenu").style.display = "none";
}
function closeAssign(){
  document.getElementById("assignDiv").style.display = "none";
  document.getElementById("myMenu").style.display = "block";
  document.getElementById("assignResult").innerHTML = "";
}

function filterAssign(){
  let tenantId = document.getElementById("assignTenantId").value.trim();
  let maxPrice = document.getElementById("assignPrice").value;
  let bed = document.getElementById("assignBed").value;
  
  let resultDiv = document.getElementById("assignResult");

  if(tenantId == ""){
    alert("Please enter Tenant ID first");
    return;
  }

  let tenant = tenants.find(t => t.id == tenantId);
  if(!tenant){
    alert("Tenant not found! Check ID");
    return;
  }

  let filtered = properties.filter(p => {
    let priceMatch = maxPrice ? Number(p.rent) <= Number(maxPrice) : true;
    let bedMatch = bed ? p.bed == bed : true;
    let available = p.status.toLowerCase().includes("avail");
    return priceMatch && bedMatch && available;
  });

  if(filtered.length == 0){
    resultDiv.innerHTML = "<p style='color:red;'>No available house match that price/bed</p>";
    return;
  }

  resultDiv.innerHTML = "";
  filtered.forEach(p => {
    resultDiv.innerHTML += `
      <div style="border:1px solid gold; margin:10px 0; padding:10px; border-radius:5px; background:#ccc;">
        <b>Property Address: ${p.address}</b><br>
        Type: ${p.type} - ${p.bed} Bedrooms <br>
Rent: ${p.rent} Naira<br>
        <button onclick="doAssign('${p.id}', '${tenantId}')" style="background:green; color:white; border:none; padding:5px 10px; border-radius:3px; margin-top:5px; cursor:pointer;">Assign ${tenant.Name} here</button>
      </div>
    `;
  });
}

function doAssign(propId, tenId){
  let propIndex = properties.findIndex(p => p.id == propId);
  let tenIndex = tenants.findIndex(t => t.id == tenId);

  properties[propIndex].status = "occupied";
  tenants[tenIndex].Property = propId;

  localStorage.setItem("myProperties", JSON.stringify(properties));
  localStorage.setItem("myTenants", JSON.stringify(tenants));

  alert(`Success! ${tenants[tenIndex].Name} has been allocated to ${properties[propIndex].address}`);
  closeAssign();
  viewProperties(); // to see updated status
}

function openRentForm() { document.getElementById("rentForm").style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closeRentForm() { document.getElementById("rentForm").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

//to allow for recording of rent payments 

// This array will hold all properties
let payments= JSON.parse(localStorage.getItem("myPayments")) || [];
// means new properties added will be stored in local storage(browser storage).

function recordRent() {
    let newRecord = {
        TenantId: document.getElementById("tId").value,
        PropertyId: document.getElementById("pId").value,
        Amount: document.getElementById("amount").value,
        Date: document.getElementById("paymentDate").value,
        Status: document.getElementById("paymentStatus").value,
    };
// if user does not input tenant id and property id,  dont save.
    if(newRecord.TenantId == "" || newRecord.PropertyId == "" || newRecord.Amount == ""){
        alert("please input Tenant ID, Property ID and amount");
        return;
    }

    payments.push(newRecord);
    localStorage.setItem("myPayments", JSON.stringify(payments));
    
    alert("Payment recorded! ");
    
    // after saving,clear form for another input
    document.getElementById("pId").value = "";
    document.getElementById("tId").value = "";
    document.getElementById("amount").value = "";
    document.getElementById("paymentDate").value = "";
    document.getElementById("paymentStatus").value = "";

    closeRentForm();
}

function viewPayments() {
    let display = document.getElementById("viewPaymentsDiv");
    let list = document.getElementById("paymentHistory");
    
    list.innerHTML=""// clear old ones first.
    
    // if no payments have been recorded yet,
    if(payments.length == 0){
        list.innerHTML += "<p>No payments recorded yet</p>";
    } else {
        payments.forEach((pa, index) => {
    // how to display saved properties       
 list.innerHTML += `
                <div style="border:1px solid gold; margin:10px; padding:10px; border-radius:5px; background:white; text-align:left;">
                    <b>TenantID:</b> ${pa.TenantId} <br>
                    <b>PropertyID:</b> ${pa.PropertyId} <br>
                    <b>Amount:</b> ${pa.Amount} Naira<br>
                               <b>Date:</b> ${pa.Date}<br>
                    <b>Status:</b> ${pa.Status}
                </div>
            `;
        });
    }
    display.style.display = "block";
    document.getElementById("myMenu").style.display = "none";
}

function closePaymentsView(){
    document.getElementById("viewPaymentsDiv").style.display = "none";
    document.getElementById("myMenu").style.display = "block";
}

function openSearch(){
  document.getElementById("searchDiv").style.display = "block";
  document.getElementById("myMenu").style.display = "none";
}

function closeSearch(){
  document.getElementById("searchDiv").style.display = "none";
  document.getElementById("myMenu").style.display = "block";
  document.getElementById("searchInput").value = "";
  document.getElementById("searchResult").innerHTML = "";
}

function searchProperty(){
  let keyword = document.getElementById("searchInput").value.toLowerCase().trim();
  let resultDiv = document.getElementById("searchResult");
  
  if(keyword == ""){
    alert("Type something to search");
    return;
  }

  // Na here the main search dey happen
  let found = properties.filter(p => 
    p.id.toLowerCase().includes(keyword) || 
    p.address.toLowerCase().includes(keyword) ||
    p.type.toLowerCase().includes(keyword)
  );

  if(found.length == 0){
    resultDiv.innerHTML = "<p style='color:red;'>No property found for '" + keyword + "'</p>";
  } else {
    resultDiv.innerHTML = "";
    found.forEach(p => {
      resultDiv.innerHTML += `
        <div style="border:1px solid gold; margin:10px 0; padding:10px; border-radius:5px; background:#f9f9f9;">
          <b>ID:</b> ${p.id}<br>
          <b>Address:</b> ${p.address}<br>
          <b>Type:</b> ${p.type}<br>
          <b>Rooms:</b> ${p.bed} bedrooms<br>
          <b>Rent:</b> ${p.rent} Naira<br>
          <b>Status:</b> ${p.status}
        </div>
      `;
    });
  }
}

function openReport(){
  document.getElementById("myMenu").style.display = "none";
  document.getElementById("reportDiv").style.display = "block";
  generateReport();
}

function closeReport(){
  document.getElementById("reportDiv").style.display = "none";
  document.getElementById("myMenu").style.display = "block";
}

function generateReport(){
  // Total properties
  let totalProps = properties.length;
  
  // Available vs Occupied 
  let available = properties.filter(p => p.status.toLowerCase().includes("avail")).length;
  let occupied = totalProps - available;

  let totalLandlords = landlords.length;
  let totalTenants = tenants.length;

  // Total rent collected
  let totalRent = 0;
  payments.forEach(pa => {
    totalRent += Number(pa.Amount) || 0;
  });

  let resultDiv = document.getElementById("reportResult");
  resultDiv.innerHTML = `
    <b> PROPERTY REPORT </b><br>
    Total Properties: ${totalProps}<br>
    Available Properties: ${available}<br>
    Occupied Properties: ${occupied}<br>
    Total Landlords: ${totalLandlords}<br>
    Total Tenants: ${totalTenants}<br>
    Total Rent Collected: ${totalRent.toLocaleString()} Naira<br>
    
  `;
}

    </script>
    
    </body>
</html>
