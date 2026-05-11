# Resultados Experimentais — Métodos Exatos para o APPP em Redes Wi-Fi 6/6E

Este repositório contém os resultados experimentais completos do artigo:

> **Métodos Exatos para o Problema de Posicionamento de Pontos de Acesso em Redes Wi-Fi 6/6E**
> *Artigo submetido ao Simpósio Brasileiro de Pesquisa Operacional (SBPO) 2026.*

## Descrição

O artigo propõe dois modelos de Programação Linear Inteira Mista (PLIM) para o Problema de Posicionamento de Pontos de Acesso (APPP) com suporte a Wi-Fi 6/6E, incorporando suporte tri-banda (2,4 GHz / 5 GHz / 6 GHz), alocação de canais com restrições de interferência e conectividade redundante. Os modelos foram avaliados em 148 plantas-baixas reais do conjunto de dados CVC-FP, resolvidos com IBM CPLEX 22.1.1 com limite de 600 s por instância.

## Arquivo de resultados

**`resultados_completos.csv`** — resultados para todas as 148 instâncias testadas.

| Coluna | Descrição |
|--------|-----------|
| `instancia` | Nome da instância (planta-baixa do dataset CVC-FP) |
| `aps_regioes` | Número de APs obtido pela formulação por regiões |
| `aps_pontos` | Número de APs obtido pela formulação por pontos |
| `tempo_regioes_s` | Tempo de execução da formulação por regiões (segundos) |
| `tempo_pontos_s` | Tempo de execução da formulação por pontos (segundos ou `timeout`) |
| `pontos_alta_demanda` | Número de pontos de alta demanda na instância |
| `pontos_livres` | Número de pontos após discretização (candidatos a AP e unidades de demanda) |
| `pontos_obstaculos` | Número de pontos de obstáculos (paredes e colunas) |

O valor `timeout` indica que a execução atingiu o limite de 600 s; nesse caso, a solução reportada é a melhor solução viável encontrada até o momento da interrupção.

## Dataset CVC-FP

As instâncias são derivadas do conjunto de dados público CVC-FP:

> Fernandez-Moral, E., Martins, R., Wolf, D., & Rives, P. (2016).
> *A new metric for evaluating semantic segmentation: leveraging global and contour accuracy.*
> Proceedings of the IEEE Intelligent Vehicles Symposium.
> Disponível em: https://dag.cvc.uab.es/dataset/cvc-fp-database-for-structural-floor-plan-analysis/

## Licença

Os dados deste repositório estão disponibilizados sob a licença
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

Você pode usar, compartilhar e adaptar este material para qualquer finalidade, inclusive comercial, desde que atribua crédito ao trabalho original.
