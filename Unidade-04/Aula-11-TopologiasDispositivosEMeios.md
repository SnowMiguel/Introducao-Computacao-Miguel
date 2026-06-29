# Aula 11 – Redes de Computadores: Topologias, Dispositivos e Meios

**Estudante:** Miguel M. Neves 
**Disciplina:** Introdução à Computação  

---

## 🎯 Objetivo
Entender a organização física e lógica das redes, identificar os principais dispositivos (Hub, Switch, Roteador) e reconhecer os diferentes meios de transmissão (guiados e não guiados).

---

## 1. Diagramas de Topologias

A topologia define o layout físico e lógico da rede. Os principais modelos são:

* **Estrela (Star):** Todos os hosts conectam-se a um dispositivo central (Switch ou Hub). É o padrão moderno para redes locais (LAN).
* **Barramento (Bus):** Todos os dispositivos compartilham um único cabo central (backbone).
* **Anel (Ring):** Os dispositivos formam um ciclo, onde o dado circula em uma direção até o destino.
* **Malha (Mesh):** Cada nó possui conexões redundantes com múltiplos outros nós, garantindo alta disponibilidade.

---

## 2. Quadro Comparativo de Dispositivos

| Dispositivo | Função Principal | Vantagens / Limitações | Exemplo de Uso |
| :--- | :--- | :--- | :--- |
| **Hub** | Repete o sinal (broadcast) para todas as portas. | **Limitação:** Gera colisões, ineficiente e "barulhento". | Redes legadas/muito antigas. |
| **Switch** | Memoriza endereços MAC e entrega o dado apenas ao destino. | **Vantagem:** Comunicação silenciosa, isolada e rápida. | Redes locais (LAN) modernas. |
| **Roteador** | Interliga redes distintas e determina o melhor caminho (GPS de dados). | **Vantagem:** Inteligente e essencial para conectar à Internet. | Conexão de casa com o Provedor. |

---

## 3. Meios de Transmissão

A comunicação ocorre através de meios que conduzem dados (elétrons ou fótons):

### 🧵 Meios Guiados (Com Fio)
* **Par Trançado (RJ45):** Fios entrelaçados que anulam interferências. É o padrão de custo-benefício para redes LAN.
* **Cabo Coaxial:** Possui blindagem extra contra interferências externas (comum em infraestrutura de TV).
* **Fibra Óptica:** Utiliza pulsos de luz para transmissão de altíssima velocidade e distância.

### 📶 Meios Não Guiados (Sem Fio)
* **Wi-Fi:** Padrão para rede local sem fio utilizando espectro eletromagnético.
* **Bluetooth:** Focado em conexões de curtíssimo alcance para dispositivos pessoais.
* **Satélite:** Cobertura global, mas com latência (atraso) superior.
* **Infravermelho:** Curto alcance, requer visada direta.

---

## 📝 Reflexão Individual
**Pergunta:** *“Qual topologia seria mais adequada para a rede da sua residência e por quê?”*

A topologia mais adequada para a minha residência é a **Topologia em Estrela (Star)**. Esta escolha fundamenta-se na eficiência operacional, na facilidade de gestão e na robustez que este modelo oferece em ambientes domésticos modernos.

Numa rede residencial baseada na topologia em estrela, todos os dispositivos — como smartphones, smart TVs, computadores e dispositivos IoT — estão conectados a um ponto central, que é o roteador sem fio. As razões para esta escolha são:

1. **Facilidade de Gestão e Manutenção:** Numa topologia em estrela, o impacto de uma falha é isolado. Se um cabo de rede for danificado ou um dispositivo apresentar um erro, a rede permanece operacional para todos os outros equipamentos.
2. **Escalabilidade:** A necessidade de adicionar novos dispositivos a uma casa é constante. A topologia em estrela permite que eu ligue novos equipamentos (via Wi-Fi ou cabo Ethernet) ao roteador central sem qualquer interrupção na comunicação dos dispositivos já existentes.
3. **Desempenho Otimizado:** Diferente de um hub, o roteador moderno atua como um gerenciador de tráfego, encaminhando os pacotes de forma eficiente para o destino correto, reduzindo colisões e otimizando a largura de banda.

Em suma, a topologia em estrela é a arquitetura que melhor equilibra o desempenho, o custo de implementação e a facilidade de manutenção para as exigências de conectividade de uma residência contemporânea.

---

## 📚 Referências
TANENBAUM, A. S.; FEAMSTER, N.; WETHERALL, D. J. **Redes de computadores**. 6. ed. São Paulo: Bookman, 2021. E-book. Disponível em: https://plataforma.bvirtual.com.br. Acesso em: 20 abr 2026.

---
*Documentação gerada para fins acadêmicos - Introdução à Computação.*
