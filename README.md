# amigo-secreto
Amigo secreto e o jogo simples para sorteia nome para um amigo segredo ou para diferentes sorteios maneira simples e facil de uso.


let amig = [];

function adicionarAmigo(){
    let input =  document.getElementById("amigo");
    let amigo = input.value.trim();


    if (amigo === "" ) {
        alert('Por favor, digite um nome');


    }
    amig.push(amigo);

    
    let lista = document.getElementById("listaAmigos");
    let item = document.createElement("li");
    item.textContent = amigo;
    lista.appendChild(item);

    input.value = "";
    input.focus();                  
}
function sortearAmigo() {
    if (amig.length === 0) {
        alert("por favor, adicione nomes para fazer o sorteio.");
        return;
    }

    let sorteado = amig[Math.floor(Math.random() * amig.length)];
    document.getElementById("resultado").textContent = "O amigo sorteado foi: " + sorteado;
}
