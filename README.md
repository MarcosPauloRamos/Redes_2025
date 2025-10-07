Explicação do projeto:



Criação de uma rede de fio com três pontos:

servidor

roteador intermediario

roteador final que distribui a rede sem fio para usuarios de 1 a 50 usuarios

O projeto roda em 6 opções:

Conexão TCP apenas com usuarios moveis ou fixos (2 arquivos diferentes)

Conexão UDP apenas com usuarios moveis ou fixos (2 arquivos diferentes)

Conexão TCP+UDP apenas com usuarios moveis ou fixos (2 arquivos diferentes)



comandos para rodar o codigo:

ir para a pasta de execução dos arquivos: cd ~/ns-allinone-3.41/ns-3.41

mude para onde está seu arquivo

🟦 1️⃣ UDP — Clientes fixos
./waf --run "scratch/projeto_redes_misto --trafego=UDP --moveis=false --nClients=10"

🟦 2️⃣ UDP — Clientes móveis
./waf --run "scratch/projeto_redes_misto --trafego=UDP --moveis=true --nClients=10"

🟥 3️⃣ TCP — Clientes fixos
./waf --run "scratch/projeto_redes_misto --trafego=TCP --moveis=false --nClients=10"

🟥 4️⃣ TCP — Clientes móveis
./waf --run "scratch/projeto_redes_misto --trafego=TCP --moveis=true --nClients=10"

🟩 5️⃣ MISTO (UDP + TCP) — Clientes fixos
./waf --run "scratch/projeto_redes_misto --trafego=MISTO --moveis=false --nClients=10"

🟩 6️⃣ MISTO (UDP + TCP) — Clientes móveis
./waf --run "scratch/projeto_redes_misto --trafego=MISTO --moveis=true --nClients=10"

📂 Resultado esperado após cada simulação

Depois de cada comando, o programa gera dois arquivos de saída (um .xml e um .csv), dentro da pasta raiz do ns-3, com nomes como:

saida_UDP_fixos_10.xml

saida_UDP_fixos_10.csv

saida_TCP_moveis_10.xml

saida_MISTO_fixos_10.csv

...


🔸 O número final (10 neste exemplo) vem do parâmetro --nClients=10.

🔸 Você pode trocar o valor (ex.: --nClients=50) sem mudar mais nada.

🔸 Se quiser rodar por mais tempo, adicione --simTime=30 no final.
