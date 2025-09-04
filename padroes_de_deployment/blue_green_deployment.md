## Blue green Deployment
### Use para ambiente alternados para minimizar downtime e simplificar roolbacks em suas implantações.


Como funciona: Mantém duas versões do ambiente (Blue = atual, Green = nova). O tráfego é roteado para uma ou outra.
Vantagens: Rollback rápido (basta voltar para o ambiente antigo). Sem downtime.
Desvantagens: Requer o dobro de infraestrutura (custo maior).
Uso típico: Sistemas que não podem ter interrupção e precisam de rollback imediato.
![img_11.png](img/img_11.png)

![img_12.png](img/img_12.png)