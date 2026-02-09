<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cotações - Câmera Rápida</title>

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
  border-radius:12px;
  box-shadow:0 0 12px rgba(0,0,0,0.15);
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
  padding:12px;
  margin-top:5px;
  border-radius:6px;
  border:1px solid #ccc;
  font-size:15px;
}

.main-btn{
  background:#25D366;
  color:white;
  border:none;
  margin-top:20px;
  font-size:18px;
  cursor:pointer;
}

.camera-btn{
  background:#1976d2;
  color:white;
  border:none;
  margin-top:10px;
  font-size:16px;
  cursor:pointer;
}

.preview{
  margin-top:15px;
  text-align:center;
}

.preview img{
  max-width:100%;
  border-radius:8px;
  border:2px solid #eee;
}

.info{
  margin-top:10px;
  background:#f1f1f1;
  padding:10px;
  border-radius:6px;
  font-size:14px;
}
</style>
</head>

<body>

<div class="container">

<h1>Envio de Cotação</h1>

<label>Nome do Vendedor</label>
<input type="text" id="seller" placeholder="Digite seu nome">

<label>Foto da Cotação</label>

<!-- Input escondido -->
<input type="file" id="photo" accept="image/*" capture="environment" style="display:none;">

<button class="camera-btn" onclick="openCamera()">📷 Tirar Foto</button>

<div class="preview" id="preview"></div>

<label>Observação</label>
<textarea id="note" placeholder="Opcional"></textarea>

<button class="main-btn" id="sendBtn">Enviar</button>

<div class="info">
➡️ Tire a foto, depois clique em Enviar.<br>
➡️ No WhatsApp, anexe a mesma foto.
</div>

</div>

<script>

const btn = document.getElementById("sendBtn");
const photo = document.getElementById("photo");
const seller = document.getElementById("seller");
const note = document.getElementById("note");
const preview = document.getElementById("preview");

const num1 = "5599988592997";
const num2 = "5599981050024";

let message = "";


// Abrir câmera
function openCamera(){
  photo.click();
}


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


// Enviar
btn.addEventListener("click", ()=>{

  if(!seller.value.trim()){
    alert("Informe seu nome.");
    return;
  }

  if(!photo.files[0]){
    alert("Tire a foto primeiro.");
    return;
  }

  message =
`📋 *Nova Cotação*

👤 Vendedor: ${seller.value}

📝 Obs:
${note.value || "Nenhuma"}

📅 ${new Date().toLocaleString()}`;

  showOptions();

});


// Mostrar opções
function showOptions(){

  const escolha = confirm(
"Enviar primeiro para COMPRAS?\n\nOK = Compras\nCancelar = Gerência"
  );

  if(escolha){
    openWhats(num1);
  }else{
    openWhats(num2);
  }

}


// Abrir Whats
function openWhats(number){

  const url = "https://wa.me/" + number + "?text=" + encodeURIComponent(message);

  window.open(url,"_blank");

  alert("No WhatsApp, anexe a foto tirada.");

}

</script>

</body>
</html>
