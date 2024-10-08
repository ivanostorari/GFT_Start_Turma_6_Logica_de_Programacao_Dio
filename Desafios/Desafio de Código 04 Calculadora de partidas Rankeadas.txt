// Função que recebe o número de vitórias e derrotas e calcula o saldo e o nível do jogador
function calcularRank(vitorias, derrotas) {
    // Calcula o saldo de vitórias
    const saldoVitorias = vitorias - derrotas;
    
    // Variável para armazenar o nível do jogador
    let nivel;

    // Estrutura de decisão para definir o nível com base nas vitórias
    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 11 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else if (vitorias >= 101) {
        nivel = "Imortal";
    }

    // Retorna o saldo de vitórias e o nível
    return { saldoVitorias, nivel };
}

// Entrada de dados (substitua essas linhas por gets() na plataforma DIO)
const vitorias = parseInt(gets());  // Exemplo: 55 vitórias
const derrotas = parseInt(gets());  // Exemplo: 30 derrotas

// Chama a função para calcular o saldo e o nível
const resultado = calcularRank(vitorias, derrotas);

// Exibe o resultado
print(`O Herói tem um saldo de ${resultado.saldoVitorias} e está no nível de ${resultado.nivel}`);