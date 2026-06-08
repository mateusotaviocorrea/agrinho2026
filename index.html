// ==========================================
// CONFIGURAÇÕES INICIAIS DO GRID (TABULEIRO)
// ==========================================
let cols = 8;       // Número de colunas da nossa fazenda digital
let rows = 6;       // Número de linhas da nossa fazenda digital
let gridSize = 60;   // Tamanho em pixels de cada quadrado (talhão de terra)

// MATRIZ BIDIMENSIONAL DO SOLO
let solo = [];

// ==========================================
// VARIÁVEIS GLOBAIS DE CONTROLE DO JOGO
// ==========================================
let aguaReservatorio = 100;     // Quantidade de água restante para irrigar (%)
let pontuacaoSustentavel = 100; // Pontuação de equilíbrio ecológico do jogador (%)
let jogoAtivo = true;           // Controla se o jogo está rodando ou se deu Game Over

function setup() {
  // AJUSTE: Aumentamos o espaço inferior para +110px para caber o painel e a legenda visual
  createCanvas(cols * gridSize, rows * gridSize + 110);
  
  // Inicialização da matriz do solo
  for (let i = 0; i < cols; i++) {
    solo[i] = []; 
    for (let j = 0; j < rows; j++) {
      solo[i][j] = random(60, 100);
    }
  }
}

function draw() {
  background(240); // Fundo cinza claro

  if (!jogoAtivo) {
    telaGameOver();
    return;
  }

  // ==========================================
  // 1. ATUALIZAÇÃO E DESENHO DO SOLO (FAZENDA)
  // ==========================================
  for (let i = 0; i < cols; i++) {
    for (let j = 0; j < rows; j++) {
      
      // O solo seca ligeiramente a cada frame (simulação do clima)
      if (solo[i][j] > 0) {
        solo[i][j] -= 0.05; 
      }

      // Função matemática que gera o degradê visual baseado na umidade
      let r = map(solo[i][j], 0, 100, 255, 34);
      let g = map(solo[i][j], 0, 100, 0, 139);
      let b = map(solo[i][j], 0, 100, 0, 34);
      
      fill(r, g, b); 
      stroke(255);   
      rect(i * gridSize, j * gridSize, gridSize, gridSize); 
    }
  }

  // ==========================================
  // 2. SIMULAÇÃO DO DRONE (MANEJO DE PRECISÃO)
  // ==========================================
  let mouseGridX = floor(mouseX / gridSize);
  let mouseGridY = floor(mouseY / gridSize);

  if (mouseGridX >= 0 && mouseGridX < cols && mouseGridY >= 0 && mouseGridY < rows) {
    
    // Desenha o contorno da mira do drone
    noFill();
    stroke(0, 150, 255); 
    strokeWeight(3);     
    rect(mouseGridX * gridSize, mouseGridY * gridSize, gridSize, gridSize);
    strokeWeight(1);     

    // Mecânica de clique para irrigar
    if (mouseIsPressed && aguaReservatorio > 0) {
      
      // Regra de Lixiviação (Desperdício)
      if (solo[mouseGridX][mouseGridY] > 85) {
        pontuacaoSustentavel -= 0.2; 
      }

      if (solo[mouseGridX][mouseGridY] < 100) {
        solo[mouseGridX][mouseGridY] += 1.5; 
        aguaReservatorio -= 0.3;             
      }
    }
  }

  // ==========================================
  // 3. RENDERIZAÇÃO DO PAINEL E DA EXPLICAÇÃO VISUAL
  // ==========================================
  desenharPainel();
  desenharLegendaCores(15, rows * gridSize + 75); // Posiciona a legenda logo abaixo do HUD

  // ==========================================
  // 4. VERIFICAÇÃO DE STATUS
  // ==========================================
  verificarCondicoes();
}

// FUNÇÃO AUXILIAR: Desenha a HUD (Painel de Status)
function desenharPainel() {
  fill(50); 
  noStroke();
  rect(0, rows * gridSize, width, 55);

  fill(255); 
  textSize(14);
  textAlign(LEFT, CENTER);
  
  text("💧 Água do Reservatório: " + nf(aguaReservatorio, 1, 0) + "%", 15, rows * gridSize + 27);
  text("🌱 Sustentabilidade: " + nf(pontuacaoSustentavel, 1, 0) + "%", width - 180, rows * gridSize + 27);
}

// FUNÇÃO AUXILIAR: Desenha os blocos explicativos para o usuário e avaliadores
function desenharLegendaCores(x, y) {
  textSize(11);
  textAlign(LEFT, CENTER);
  noStroke();

  // Desenha o bloco explicativo VERDE
  fill(34, 139, 34); 
  rect(x, y, 14, 14, 3); 
  fill(60); 
  text("Solo Úmido/Saudável", x + 20, y + 7);

  // Desenha o bloco explicativo AMARELO
  fill(255, 204, 0); 
  rect(x + 155, y, 14, 14, 3); 
  fill(60);
  text("Alerta: Secando", x + 175, y + 7);

  // Desenha o bloco explicativo VERMELHO
  fill(255, 0, 0); 
  rect(x + 285, y, 14, 14, 3); 
  fill(60);
  text("Crítico: Solo Seco", x + 305, y + 7);
}

function verificarCondicoes() {
  if (pontuacaoSustentavel <= 0 || aguaReservatorio <= 0) {
    jogoAtivo = false;
  }
}

function telaGameOver() {
  fill(0, 0, 0, 200); 
  rect(0, 0, width, height);
  
  fill(255);
  textSize(24);
  textAlign(CENTER, CENTER);
  text("Fim de Jogo!", width / 2, height / 2 - 20);
  
  textSize(14);
  text("Pense em estratégias de precisão na próxima!", width / 2, height / 2 + 15);
}
