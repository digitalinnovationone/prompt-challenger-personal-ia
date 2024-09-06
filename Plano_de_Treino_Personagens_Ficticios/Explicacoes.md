
Fiz algumas modificações no projeto original:
* Inserção de 10 Personagens Ficticios  (5 masculino e 5 feminino)
* Inserção de Altura e Peso aos personagens
* Inserção de treinos mais detalhados do que a descrição disponivel
* Inserção da possibilidade de manter treinos mais intensos para alcançar o objetivo (perda ou ganho de peso) e não tão intensos afim apenas de manter a forma.

## Assistente de Treino Ideal com IA e Engenharia de Prompt
Aqui está um exemplo prático de como seria a implementação de um assistente de personal trainer automatizado usando IA e Engenharia de Prompt para gerar rotinas de treino personalizadas para personagens fictícios.

Como foi possivel de percerber ao observar os arquivos, o assistente foi além do Prompt, gerando uma rotina de treinos bem mais completa e complexa do que o material disponibilizado pela DIO no repositorio apresentava, este é o poder da IA em conjunto com um bom Prompt.

Automação com IA e Engenharia de Prompt
O assistente de treino ideal usaria prompts como este para adaptar e gerar automaticamente as rotinas de treino de acordo com os dados fornecidos pelo usuário. Seguindo as regras de negócio:

## Métrica de Cálculo usada para determinar a necessidade de cada personagem

A determinação de se os personagens precisavam ganhar ou perder peso foi baseada em um conceito comum de avaliação de saúde: o Índice de Massa Corporal (IMC) e o peso considerado saudável em relação à altura de cada personagem.

1. Cálculo do IMC:

O IMC é uma fórmula simples para avaliar se uma pessoa está em um peso saudável, abaixo do peso, ou acima do peso com base em sua altura e peso.

Fórmula:
IMC = Peso(Kg) / Altura(m)²

IMC < 18,5: Abaixo do peso

IMC entre 18,5 e 24,9: Peso normal

IMC entre 25 e 29,9: Sobrepeso

IMC > 30: Obesidade

2. Faixa de Peso Saudável:
Com base na altura de cada personagem, podemos determinar a faixa de peso considerada saudável de acordo com o IMC normal (18,5 a 24,9). Para isso, eu fiz uma estimativa do peso ideal para cada personagem:

Peso ideal mínimo: IMC 18,5

Peso mín. = 18,5 * (Altura²)

Peso ideal máximo: 24,9

Peso ideal máx. = 24,9 * (Altura²)

3. Comparação do Peso Atual com a Faixa Saudável:
Com os valores de peso mínimo e máximo calculados para cada altura, eu comparei o peso atual do personagem para determinar se:

Estava abaixo da faixa saudável (necessita ganhar peso).
Estava acima da faixa saudável (necessita perder peso).
Estava dentro da faixa saudável (manutenção do peso).

Exemplo de Cálculo para Salete:
Altura de Salete: 1,45m
Peso atual: 37 kg

Cálculo do IMC:

IMC = 37 / 1,45² = 17,6

Com um IMC de 17,6, Salete está abaixo do peso. O peso saudável para ela seria:

Peso mínimo (IMC 18,5):

Peso min. = 18,5 * 1,45² = 38,9 kg

Peso máx. = 24,9 * 1,45 = 52,4 kg

Portanto, Salete, com 37 kg, precisaria ganhar peso até atingir pelo menos 39 kg para estar em uma faixa de peso saudável.

## Execução da Regras

* **Seleção do personagem:** IA seleciona os dados e características de um dos personagens (como Alberto ou Ana).
* **Identificação do biotipo corporal:** Usando as informações do prompt, a IA determina o biotipo de cada personagem.
* **Dias disponíveis para treino e preferências:** Com base no tempo disponível para treino e no tipo de exercício preferido, o assistente cria uma rotina personalizada.
* **Geração do plano de treino:** A IA usa o biotipo, dias de treino e o tipo de exercício para gerar o plano mais adequado, como treinos ABC ou Full Body.

Essa abordagem não apenas otimiza o tempo de treino de cada personagem, mas também ajusta o foco de cada rotina, seja em perda de peso, ganho de massa ou manutenção.

Caso fosse desejo do usuário o assistente poderia implementar  lógica em um código para gerar automaticamente os planos de treino para mais personagens ou personalizar com mais detalhes!

## Questões biologicas como gênero influenciaram na escolha dos treinos?

As questões de gênero não influenciaram diretamente na escolha do tipo de treino para os personagens fictícios, mas fatores biológicos como diferenças hormonais e de composição corporal entre homens e mulheres podem ter impacto na forma como os treinos são estruturados. Homens, em média, tendem a ter uma maior massa muscular e níveis mais altos de testosterona, o que facilita o ganho de massa muscular e a recuperação após treinos intensos. Mulheres, por outro lado, geralmente possuem uma porcentagem maior de gordura corporal e menor massa muscular, o que pode influenciar a abordagem dos treinos, com ênfase em exercícios de resistência muscular e fortalecimento de áreas como glúteos e pernas, mais comuns em objetivos estéticos femininos.

Apesar dessas diferenças biológicas, o treino deve ser sempre ajustado de acordo com os objetivos individuais e não simplesmente com base no gênero. Por exemplo, tanto homens quanto mulheres podem se beneficiar de treinos de hipertrofia, funcional ou cardiovascular, dependendo de suas metas, como ganho de massa, perda de peso ou melhora na resistência. A personalização do treino deve considerar fatores como composição corporal, nível de condicionamento físico e preferências pessoais, ao invés de ser moldada exclusivamente pelas características biológicas.

Dessa forma, a variação no tipo de treino não foi baseada no gênero dos personagens, mas em suas características individuais, como biotipo corporal, metas de peso e preferência por exercícios. A ideia é que o treino seja eficiente e saudável, independentemente de questões de gênero, adaptando-se às necessidades físicas de cada pessoa.


Eu James da Fonseca e Silva, aluno da DIO desde janeiro de 2024, implementei este projeto por meio do ChatGPT-4o no dia 05/09/2024. 

