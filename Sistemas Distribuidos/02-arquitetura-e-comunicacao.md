# Sistemas Distribuídos

Segundo a [página da IBM sobre sistemas distribuídos](https://www.ibm.com/br-pt/think/topics/distributed-systems), um sistema distribuído é:
> Um sistema distribuído é um conjunto de computadores e dispositivos independentes que trabalham juntos em uma rede de modo que, do lado de fora, pareçam ser um único sistema unificado.

Conceitos básicos:
- comunicação
- arquitetura
- processamento concomitante(concorrente)
- 
# Arquitetura

Os modelos de arquiteturas que se destacam nesse assunto são:  
1) Cliente-Servidor
2) Peer-to-Peer
3) Multicamadas
4) Cluster
5) Computação em Grade
6) Computação em Nuvem
7) Microsserviços

# Comunicação 

A comunicação respeita o modelo TCP/IP
- endereço IP: servidor, cliente, grupo.
- máscara ou classe de rede e domínio
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

