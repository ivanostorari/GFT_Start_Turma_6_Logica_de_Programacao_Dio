const readline = require("readline")

const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});


rl.question("Nome do Heroi: ", (nome) => {
    rl.question('Informe o valor total do XP para verificar o nivel: ', (XP) => {
        if (XP <= 1000) {
            console.log("O Herói de nome " + nome +" está no nível de Ferro")
        }else if(XP <= 2000) {
            console.log("O Herói de nome " + nome +" está no nível de Bronze")
        }else if(XP <= 5000) {
            console.log("O Herói de nome " + nome +" está no nível de Prata")
        }else if(XP <= 7000) {
            console.log("O Herói de nome " + nome +" está no nível de Ouro")
        }else if(XP <= 8000) {
            console.log("O Herói de nome " + nome +" está no nível de Platina")
        }else if(XP <= 9000) {
            console.log("O Herói de nome " + nome +" está no nível de Ascendente")
        }else if(XP <= 10000) {
            console.log("O Herói de nome " + nome +" está no nível de Imortal")
        }else{
            console.log("O Herói de nome " + nome +" está no nível de Radiante")
        }
    
    
        rl.close()
    });
});