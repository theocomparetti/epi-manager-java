# epi-manager-java
Sistema de Gestão de EPIs desenvolvido em Java e Spring Boot para otimização de fluxos de Saúde Ocupacional em empresas de logística urbana. Focado em transformação digital e integridade de dados (Projeto de Extensão Universitária).
♻️ EPI Manager - Sistema de Gestão de Saúde Ocupacional
📌 Sobre o Projeto
O EPI Manager é um projeto de extensão universitária desenvolvido para o curso de Gestão da Tecnologia da Informação. Ele nasceu da necessidade real de otimizar o setor de saúde ocupacional de uma empresa de coleta de resíduos urbanos (nome confidencial).
O sistema substitui o controle manual (feito em pranchetas e planilhas descentralizadas) por uma aplicação web ágil e segura. O foco é gerenciar a entrega de Equipamentos de Proteção Individual (EPIs) para os coletores de rua, garantindo rastreabilidade, segurança da informação e agilidade no atendimento do ambulatório.
🎯 O Problema vs. A Solução
 * O Problema: A equipe de enfermagem do trabalho perdia muito tempo gerenciando papéis, o que dificultava o controle de validade dos EPIs e aumentava o risco de exposição dos coletores nas ruas.
 * A Solução: Uma aplicação em Java com Spring Boot baseada na arquitetura MVC (Model-View-Controller). O sistema permite o registro instantâneo da entrega de equipamentos, salvando os dados em um banco de dados relacional e exibindo o histórico em uma interface web simples e intuitiva.
💻 Telas do Sistema
(<img width="1112" height="698" alt="Image" src="https://github.com/user-attachments/assets/c804ebb5-984d-4fd8-95f7-cd50930a5af0" />)
> <img width="1095" height="567" alt="Image" src="https://github.com/user-attachments/assets/2e76ace8-91be-4d53-91e6-b538d0e42b73" />
> 
🧠 Desafios e Aprendizados (O processo de Desenvolvimento)
Durante a construção deste projeto "do zero", enfrentei e resolvi diversos desafios reais de desenvolvimento e infraestrutura, aprimorando minhas habilidades em troubleshooting (resolução de problemas):
 * Comunicação Front-end e Back-end (Erro 405 Method Not Allowed):
   * O que aprendi: Entendi na prática a diferença entre os métodos HTTP. O erro ocorria porque o formulário HTML tentava enviar dados via GET, mas o Java aguardava um @PostMapping. O alinhamento das rotas (/salvar) com a anotação correta no Controller e no Thymeleaf resolveu a falha.
 * Arquitetura de Pastas no Java (O Efeito "Boneca Russa"):
   * O que aprendi: O Java é extremamente rigoroso com a declaração de pacotes (package). Enfrentei erros de compilação porque a estrutura física das pastas não batia com o código. Aprendi a organizar perfeitamente o padrão MVC separando os arquivos nas camadas corretas: model, repository e controller.
 * Injeção de Dependências e Imports:
   * O que aprendi: Entendi como as classes conversam entre si. Um erro clássico de "método não encontrado" (como o save ou findAll) foi resolvido entendendo que o Controller precisa ter o caminho exato (import) de onde estão o Model e o Repository.
 * Banco de Dados em Memória (H2 Console):
   * O que aprendi: Configurei o application.properties para rodar o H2 Database. Aprendi a acessar o console via navegador (localhost:8080/h2-console) para validar se as informações inseridas na interface web estavam realmente sendo persistidas no banco com os comandos SQL.
🚀 Como executar este projeto na sua máquina
 * Certifique-se de ter o Java 17+ e uma IDE (como VS Code, IntelliJ ou Eclipse) instalados.
 * Faça o clone deste repositório:
   git clone https://github.com/SEU_USUARIO/epi-manager.git

 * Abra o projeto na sua IDE e execute o arquivo principal EpiManagerApplication.java.
 * O servidor iniciará automaticamente. Abra o navegador e acesse:
   http://localhost:8080
