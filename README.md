A cibersegurança refere-se a quaisquer tecnologias, práticas e políticas que atuem na prevenção de ataques cibernéticos ou na mitigação do seu impacto. A cibersegurança tem como objetivo proteger sistemas de computador, aplicações, dispositivos, dados, ativos financeiros e pessoas contra ransomwares e outros malwares, golpes de phishing, roubo de dados e outras ameaças cibernéticas. Ela é importante porque os ataques cibernéticos e o crime cibernético têm o poder de interromper, prejudicar ou destruir empresas, comunidades e vidas. Ataques cibernéticos bem-sucedidos levam ao roubo de identidade, extorsão pessoal e corporativa, perdas de informações confidenciais e dados críticos para os negócios, interrupções temporárias nos negócios, perdas de negócios e clientes e, em alguns casos, fechamento de empresas.

Os ataques cibernéticos têm um impacto enorme e crescente nas empresas e na economia. Segundo estimativas, o crime cibernético custará à economia mundial US$ 10,5 trilhões por ano até 2025. O custo dos ataques cibernéticos continua aumentando à medida que os cibercriminosos se tornam mais avançados.

De acordo com o mais recente relatório do custo das violações de dados da IBM:
• O custo médio de uma violação de dados saltou para US$ 4,88 milhões em comparação com US$ 4,45 milhões em 2023, um aumento de 10%. Além de ser o maior aumento desde a
pandemia.
• As perdas de negócios (perda de receita devido ao downtime do sistema, clientes perdidos e danos à reputação), e os custos de resposta pós-violação (custos para criar centrais de atendimento e serviços de monitoramento de crédito para os clientes afetados ou para o pagamento de multas regulatórias) aumentaram quase 11% em relação ao ano anterior.
• O número de organizações que pagam mais de US$ 50.000 em multas regulatórias como resultado de uma violação de dados aumentou 22,7% em relação ao ano anterior, já aqueles
que pagam mais de US$ 100.000 tiveram um aumento de 19,5%. (Fonte: IBM)

Neste trabalho iremos utilizar uma base de dados relacionados a ataques de segurança cibernética. Ela consiste em 25 métricas e 40.000 dados. Mais informações e a base de dados podem ser acessadas no repositório: https://github.com/incribo-inc/cybersecurity_attacks.

a) Faça as análises e alterações necessárias na base de dados para predizer a variável Severity
Level. Verifique se a base de dados possui valores faltantes ou outliers. Caso existam, explique
as considerações e mudanças propostas.
b) Faça um HeatMap correlacionando o número de ataques em cada dia da semana e a cada
ano. Explique os resultados obtidos.
c) Divida aleatoriamente a base de dados em duas partes: treino, com 70% das amostras, e teste,
com 30%. Faça a classificação dos dados utilizando uma Rede Neural. Você deverá testar 3
topologias diferentes (números de camadas, neurônios, dropout, etc.) e explicar o porquê da
escolha de cada uma.
d) Compare os resultados obtidos. O que você pode concluir?
