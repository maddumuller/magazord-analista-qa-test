## Cenário 3
### **Análise e Identificação do Problema - Anúncios "Pausado" em vez de "Pausado (sem estoque)"**  


**Simular um envio manual de estoque zero** para um anúncio teste via API do Mercado Livre e verificar se o status muda corretamente para **paused (sem estoque)**.  

**Solicitar ao time técnico logs detalhados da API** para entender se há chamadas de atualização de estoque com quantidade 0.  

**Validar se há configurações no Mercado Livre** que impactam anúncios pausados manualmente.  

**Ajustar a integração se necessário**, garantindo que a atualização de estoque seja feita corretamente em todas as etapas (Magazord → Bling → Mercado Livre).

## Passos para Análise do Problema  

Podemos seguir uma abordagem para investigar a causa do problema com base na documentação da API do Mercado Livre e nas informações fornecidas.  

##### Verificação do Fluxo de Atualização de Estoque  
- Identificar como a atualização de estoque é enviada para o Mercado Livre quando um produto atinge estoque zero.  
- Validar se há um endpoint específico que deve ser chamado quando o estoque chega a zero.  
- Revisar se a integração com o Bling está corretamente enviando as requisições para atualizar a situação do anúncio.  

##### Análise da API do Mercado Livre
- O Mercado Livre define diferentes status para os anúncios, como:  
  - **active** → Anúncio ativo.  
  - **paused** → Anúncio pausado, mas ainda disponível para venda.  
  - **paused (sem estoque)** → Indica que o produto foi pausado automaticamente por falta de estoque.  
  - **closed** → Anúncio encerrado.  
- Na documentação da API do Mercado Livre, o status correto quando o estoque zera deve ser **paused (sem estoque)**.   
- Se um estoque igual a **zero** não for enviado, o status pode permanecer como **paused** e não mudar para **paused (sem estoque)**.  

##### Validação dos Logs e Testes Manuais  
- Revisar o log da integração para verificar se o envio do estoque **igual a zero** foi feito corretamente.  
- Realizar um teste manual na API do Mercado Livre para um anúncio de teste e observar o comportamento.  
- Caso o status do anúncio não mude para **paused (sem estoque)**, pode ser uma regra específica do Mercado Livre que precisa ser ajustada na integração.  




  

  

