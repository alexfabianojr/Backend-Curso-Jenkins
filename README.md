# Backend-Curso-Jenkins

Gerenciamento do codigo no jenkins:
- Ir na aba de gerenciamento de codigo fonte e selecionarmos git
- Adicionar nossas credenciais do git
- Selecionar a branch

Gerar pasta target ao fazer deploy do codigo 
- Adicionar passo no build
- Setar vers�o do maven
- Goals: clean install package

Deploy da aplica��o no tomcat pelo jenkins
- A��es de p�s build
- Deploy war/ear to a container
  - war/ear files: target/algumNome.war
  - Context path: application path (do tomcat no caso)
- Selecionar o container (no caso tomcat 8)
- Credenciais do tomcat
- url base do tomcat (no caso http://localhost:8001)

Deploy ao fazer altera��o no reposit�rio git 
- Nas configura��es job
  - Marcar o checkbox Consultar periodicamente o SCM
  - em Agenda: * * * * *