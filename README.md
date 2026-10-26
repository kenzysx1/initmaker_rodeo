# 🃏 Extensão Iniciativa por Cartas para Owlbear Rodeo 2.0

Esta extensão converte o bot de combate e iniciativa por baralho de cartas do Discord para uma ferramenta nativa do **Owlbear Rodeo 2.0**.

---

## 📌 Recursos Implementados

1. **Baralho Real de 52 Cartas**:
   - 4 Naipes: Copas (♥), Ouros (♦), Espadas (♠), Paus (♣).
   - 13 Valores: Ás (1) a Rei (13).
   - Regra: **Menor valor age primeiro** (Ás = 1 = mais rápido, Rei = 13 = mais lento).
   - Embaralhamento contínuo sem repetição de cartas.
2. **Ações dos Jogadores (PJs)**:
   - **🃏 Puxar 1**: Puxa 1 carta individual.
   - **⚡ Vantagem**: Puxa 2 cartas e fica automaticamente com a de **menor valor** (mais rápida).
   - **🐢 Desvantagem**: Puxa 2 cartas e mantém a de **maior valor** (mais lenta).
   - Bloqueio automático para impedir que um PJ puxe mais de uma vez na mesma rodada.
3. **Controles do Mestre**:
   - **👑 Add PdM / Mestre**: Abre janela para digitar o nome do monstro/mestre (ex: *Chefe Orc*, *Goblin 1*, *Mestre*) e puxa a carta para ele.
   - **🗑️ Remover**: Botão rápido de exclusão em cada carta/linha para retirar um combatente (libera o jogador para puxar de novo).
   - **🔄 Nova Rodada**: Limpa a mesa e reembaralha as 52 cartas.
4. **Quadro Visual em 3 Seções (Idêntico ao bot original)**:
   - 🟢 **PJs Antes do Mestre (Mais Rápidos)**: Jogadores com valor menor que a menor carta do Mestre/PdM.
   - 👑 **Mestre & PdMs**: Cartas do Mestre e de monstros.
   - 🔴 **PJs Depois do Mestre (Mais Lentos)**: Jogadores com valor igual ou maior que o Mestre.
5. **Alternância para Lista Simples**:
   - Aba para ver a ordem sequencial dos turnos (1º, 2º, 3º...) de forma compacta.
6. **Sincronização em Tempo Real na Sala**:
   - Utiliza `OBR.room.setMetadata` para que o quadro de iniciativa fique gravado na sala e visível para todos os jogadores conectados.
   - Notificações na tela da mesa a cada carta puxada.

---

## 🚀 Como Publicar no seu GitHub

1. No seu GitHub, crie um novo repositório público (ex: `iniciativa-cartas`).
2. Envie os 3 arquivos desta pasta:
   * `manifest.json`
   * `index.html`
   * `icon.svg`
3. Se você usar GitHub Pages, lembre-se de configurar a URL completa no seu `manifest.json`:
   ```json
   {
     "name": "Iniciativa por Cartas",
     "version": "1.0.0",
     "manifest_version": 1,
     "description": "Rastreador de Iniciativa por baralho de cartas para Owlbear Rodeo.",
     "icon": "https://kenzysx1.github.io/iniciativa-cartas/icon.svg",
     "action": {
       "title": "Iniciativa por Cartas",
       "icon": "https://kenzysx1.github.io/iniciativa-cartas/icon.svg",
       "popover": "https://kenzysx1.github.io/iniciativa-cartas/index.html",
       "width": 520,
       "height": 720
     }
   }
   ```
4. Ative o **Pages** em *Settings > Pages* (Branch `main`).
5. No Owlbear Rodeo, adicione a extensão colando a URL do seu `manifest.json`.
