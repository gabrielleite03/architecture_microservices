## Como definir sua estratégia de deployment? ##
### Cada estratégia atende uma necessidade, como entender qual a minha necessidade? ###

- 1: Qual o ambiente tenho hoje?
  - É uma estrutura imutável?
  - Ele é um single point of failure, tenho AutoScaling, tenho Primary/Secondary Cluster, EKS, ECS, Servless...
- 2: Qual o nível de tolerãncia ao downtime que voc/~e terá de fazer um rollback em caso de problemas?
- 3: Quão rápido precisamos ser capazes de fazer rollback em caso de problemas?
- Quais são os SLIs que devemos monitorar?
- Qual frequência de alterações do source code?
- Ter duas versões rodando em paralelo pode gerar inconsistência de saídas?

![img.png](img/img.png)

