🔹 1. Recreate Deployment (Recriar)

Como funciona: Derruba a versão antiga e sobe a nova imediatamente.

Vantagens: Simples, direto, fácil de configurar.

Desvantagens: Tempo de indisponibilidade durante o deploy.

Uso típico: Ambientes de desenvolvimento ou testes, onde downtime não é crítico.

🔹 2. Rolling Update (Atualização gradual)

Como funciona: Substitui instâncias antigas pela nova versão gradualmente.

Vantagens: Evita downtime, mais seguro que recriar tudo de uma vez.

Desvantagens: Se houver bug, parte dos usuários pode ser impactada.

Uso típico: Deploy padrão em Kubernetes.

🔹 3. Blue-Green Deployment

Como funciona: Mantém duas versões do ambiente (Blue = atual, Green = nova). O tráfego é roteado para uma ou outra.

Vantagens: Rollback rápido (basta voltar para o ambiente antigo). Sem downtime.

Desvantagens: Requer o dobro de infraestrutura (custo maior).

Uso típico: Sistemas que não podem ter interrupção e precisam de rollback imediato.

🔹 4. Canary Release

Como funciona: A nova versão é liberada apenas para uma pequena porcentagem de usuários, aumentando gradualmente.

Vantagens: Reduz risco, fácil de medir impacto. Rollback rápido.

Desvantagens: Maior complexidade de roteamento/monitoramento.

Uso típico: Serviços críticos onde é necessário validar métricas de negócio e performance antes da liberação total.

🔹 5. Shadow Deployment

Como funciona: A nova versão recebe uma cópia do tráfego real (em paralelo), mas não afeta os usuários.

Vantagens: Permite validar performance e comportamento em produção sem risco.

Desvantagens: Mais custo, pode ser difícil lidar com volume de tráfego duplicado.

Uso típico: Testes de performance, migração de bancos de dados, experimentação.

🔹 6. A/B Testing Deployment

Como funciona: Diferentes versões do serviço são oferecidas a grupos distintos de usuários, comparando métricas de uso.

Vantagens: Excelente para validar hipóteses de negócio ou experiência de usuário.

Desvantagens: Mais foco em produto do que em infraestrutura, exige coleta de métricas detalhadas.

Uso típico: Experimentos de funcionalidades em empresas orientadas a dados (Google, Facebook, etc).


| Padrão     | Downtime | Custo Infra | Risco                 | Facilidade de Rollback |
| ---------- | -------- | ----------- | --------------------- | ---------------------- |
| Recreate   | Alto     | Baixo       | Alto                  | Médio                  |
| Rolling    | Baixo    | Médio       | Médio                 | Médio                  |
| Blue-Green | Nenhum   | Alto        | Baixo                 | Muito fácil            |
| Canary     | Nenhum   | Médio       | Muito baixo           | Fácil                  |
| Shadow     | Nenhum   | Alto        | Nenhum (para usuário) | Fácil                  |
| A/B        | Nenhum   | Médio       | Baixo                 | Médio                  |


# Table of Contents
1. [Como definir sua estratégia](/padroes_de_deployment/estrategia_de_deployment)
2. [In-Place vs Immutable](/padroes_de_deployment/in-place_deployment_immutable_deployment)
3. [Esteira de deploy](/padroes_de_deployment/CICD)
4. [Full deployment](/padroes_de_deployment/full_deployment)
5. [Third Example](#third-example)
4. [`Padrões de Deployment`](/padroes_de_deployment/estrategia_de_deployment)
    5. koto