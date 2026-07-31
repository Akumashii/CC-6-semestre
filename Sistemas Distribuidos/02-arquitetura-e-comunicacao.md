# Sistemas Distribuídos

Segundo a [página da IBM sobre sistemas distribuídos](https://www.ibm.com/br-pt/think/topics/distributed-systems), um sistema distribuído é:
> Um sistema distribuído é um conjunto de computadores e dispositivos independentes que trabalham juntos em uma rede de modo que, do lado de fora, pareçam ser um único sistema unificado.

Conceitos básicos:
- comunicação
- arquitetura
- processamento concomitante(concorrente)

Objetivo:
- compartilhar recurso (processador e memória) -> secção crítica -> sincronizar

Tecnicas para gerenciar sincronismo:
- relógio: lógico(servidor para sincronizar) e físico(cada processador tem um clock diferente)
- recurso: exclusão mútua

Trabalham diretamente com seção crítica

Prioridade:
- escrita > leitura
- leitura = leitura
- escrita e escrita, um bloqueia e outro escreve

SD são fortemente dependentede de sistemas operacional: gestor de processamento; gestor de comunicação, ou um gestor de camadas de serviço
- na essencia comunicação é feita via SOCKET (ip, porta, dominio, objetos read/write) que é BLOQUEANTE

# Arquitetura


Os modelos de arquiteturas que se destacam nesse assunto são:  
1) Cliente-Servidor
2) Peer-to-Peer
3) Multicamadas
4) Cluster
5) Computação em Grade (Grid)
6) Computação em Nuvem
7) Microsserviços

Sistemas distribuídos permitem flexibilidade em:
- tolerancia a falhas - se um ponto cair isso não influência na capacidade dos outros, inclusive podem substituí-lo.
- escabilidade
- segurança
- manutenção

## Cluster

## Grid
pode haver grid de clusters

## Cliente-Servidor
Sempre vai passar para um servidor, centraliza 

objeto:
- servidor
- cliente
- socket
- ..........

tolerencia a falha: 
- 

tipo:
- monolítico, uma sede central
- ...

### RENATO AUGUSTO - youtube - construindo um servidor nao monolitico

## ESCABILIDADE

vertical:
- exige desligar o servidor ou passar à um servidor backup
- 
- ruim a longo prazo

horizontal:
- 

# programação multitarefa - threads
- miniprocesso de um processo
- thread pode ser com memoria compartilhada -> seção crítica -> monitor, semáforo
- thread pode ser sem memoria compartilhada, sem problema de sincronismo 
- programacao concorrente para solução de comunicação bloqueante

# Comunicação 

A comunicação respeita o modelo TCP/IP
- endereço IP: servidor, cliente, grupo.
- máscara ou classe de rede e **domínio**
- socket
- porta lógica

---

Em Rede de Computadores há 3 tipos de destinos quanto a comunicação: 
1) broadcast(um para todos);
2) multicast(um para um grupo);
3) unicast(um para um).

---

Para fluxo de dados temos: 
- Simplex(unidirecional);
- Half-Duplex(bidirecional e não simultâneo);
- Full-Duplex(bidirecional e simultâneo).

Sistemas de fluxo Half-Duplex ficam bloqueados quando um lado esta enviando dados. A solução é uma comunicação concomitante(concorrente) onde ambos lados se comunicam tão rapidamente que parece simultâneo. Para isso utilizaremos THREADS.

