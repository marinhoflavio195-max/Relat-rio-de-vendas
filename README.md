<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cotações - Envio Duplo WhatsApp</title>

<style>
body{
  font-family: Arial, sans-serif;
  background:#f5f5f5;
  margin:0;
  padding:20px;
}

.container{
  max-width:500px;
  background:#fff;
  margin:auto;
  padding:20px;
  border-radius:10px;
  box-shadow:0 0 10px rgba(0,0,0,0.1);
}

h1{
  text-align:center;
  color:#c62828;
}

label{
  font-weight:bold;
  display:block;
  margin-top:15px;
}

input,textarea,button{
  width:100%;
  padding:10px;
  margin-top:5px;
  border-radius:5px;
  border:1px solid #ccc;
  font-size:15px;
}

.main-btn{
  background:#25D366;
  color:white;
  border:none;
  margin-top:20px;
  font-size:17px;
  cursor:pointer;
}

.option{
  background:#1976d2;
  color:white;
  border:none;
  margin-top:10px;
  cursor:pointer;
}

.option2{
  background:#6a1b9a;
  color:white;
  border:none;
  margin-top:10px;
  cursor:pointer;
}

.hidden{
  display:none;
}

.preview{
  margin-top:15px;
  text-align:center;
}

.preview img{
  max-width:100%;
  border-radius:8px;
}
</style>
</head>

<body>

<div class="container">

<h1>Envio de Cotação</h1>

<div id="formArea">

<label>Nome do Vendedor</label>
<input type="text" id="seller">

<label>Foto da Cotação</label>
<input type="file" id="photo" accept="image/*">

<label>Observação</label>
<textarea id="note"></textarea>

<button class="main-btn" id="openOptions">Enviar</button>

<div class="preview" id="preview"></div>

</div>


<div id="optionsArea" class="hidden">

<h3>Enviar para:</h3>

<button class="option" id="send1">📱 Compras</button>

<button class="option2" id="send2">📱 Gerência</button>

<button onclick="backForm()" style="background:#999;color:white;border:none;margin-top:15px;">
Voltar
</button>

</div>

</div>


<script>

const num1 = "5599988592997";
const num2 = "5599981050024";

const form = document.getElementById("formArea");
const options = document.getElementById("optionsArea");

const btnOpen = document.getElementById("openOptions");
const send1 = document.getElementById("send1");
const send2 = document.getElementById("send2");

const seller = document.getElementById("seller");
const photo = document.getElementById("photo");
const note = document.getElementById("note");
const preview = document.getElementById("preview");

let message = "";


// Preview
photo.addEventListener("change", ()=>{

  const file = photo.files[0];
  if(!file) return;

  const reader = new FileReader();

  reader.onload = e =>{
    preview.innerHTML = `<img src="${e.target.result}">`;
  };

  reader.readAsDataURL(file);

});


// Abrir opções
btnOpen.addEventListener("click", ()=>{

  if(!seller.value.trim()){
    alert("Informe o nome do vendedor.");
    return;
  }

  if(!photo.files[0]){
    alert("Selecione a foto.");
    return;
  }

  message =
`📋 *Nova Cotação*

👤 Vendedor: ${seller.value}

📝 Observação:
${note.value || "Nenhuma"}

📅 ${new Date().toLocaleString()}`;

  form.classList.add("hidden");
  options.classList.remove("hidden");

});


// Enviar 1
send1.addEventListener("click", ()=>{

  openWhats(num1);

});


// Enviar 2
send2.addEventListener("click", ()=>{

  openWhats(num2);

});


// Abrir Whats
function openWhats(number){

  const url = "https://wa.me/" + number + "?text=" + encodeURIComponent(message);

  window.open(url,"_blank");

}


// Voltar
function backForm(){

  options.classList.add("hidden");
  form.classList.remove("hidden");

}

</script>

</body>
</html>
