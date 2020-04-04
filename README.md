# trabalho_disciplina

# Objetivo
Descrever aqui todos os processos e etapas importantes durante a realização do trabalho.

# Contextualização 
O projeto final da disciplina foi baseado na necessidade de preparar um relatório para prestação de contas das atividades de campo do meu doutorado. Dessa maneira, foram escolhidas perguntas-chave para serem respondidas através dos dados compilados nas atividades de campo.

# Organização das pastas e dos arquivos
Foram utilizadas as pastas com os nomes sugeridos para organização durante a disciplina. Eu tentei realizar o git ignore para O arquivo data/dados_brutos.xls, porem não consegui executar o comando. 

O arquivo dados_brutos_csv foi alterado de modo que as colunas foram relacionadas a números, que estão associados as informações originais da planilha de dados brutos original. Isso foi feito para facilitar a leitura e o processamento no R. Do mesmo modo, o nome das colunas foram reorganizados dessa maneira, seguindo a mesma estrutura.

A planilha tabela_EP2019.csv foi gerada a partir do processamento dos dados no R. Porém ela foi direcionada para a pasta data, pois configura os dados brutos filtrados através de uma coluna chave. Após a geração dessa tabela, as análises foram realizadas novamente.

# Análises no R
Foram realizadas algumas análises exploratórias dos dados:
1 seleção de colunas específicas ## ex. trabalhando<-dados[,c(2,3)] 
2 soma por linha ## ex. tabela2<-cbind(tabela,rowSums(tabela))
3 adicionada a soma por coluna ## ex. tabela_total_gen_aldeia_1<-rbind(tabela2,colSums(tabela2))
4 alterado nomes de colunas ## ex. colnames(tabela_total_gen_aldeia_1)<-c("F","M","Total")
5 tirada a média de colunas ## ex. aggregate(idade~genero,FUN=mean,data=dados)
6 selecionar as informações da tabela a partir da variável de determinada coluna ## ex. tabela_EP2019<-droplevels(subset(x = dados,subset = dados$EP_2019=="sim"))

# Git hub
Tive certa dificuldade na configuração e na execução do Git. Mas por fim creio que entendi o processo para realizar o commit dos dados desejados.

# Problemas que tive no caminho
Para configurar o git hub ao Rstudio eu tive um pouco de dificuldade. Mas acho que devido as minhas limitações mesmo. Depois de alguma insistência eu consegui fazer commit das pastas que estava querendo. 

Outro problema foi realizar a edição do README através do RStudio. Eu não consegui fazer o push, apesar de achar que estava executando a operação certa (git push -u origin master). Não consegui entender o que houve. Por fim, realizei a edição do README através site do Git hub.

Outro problema, também sem solução e que eu não consegui entender direito, foi que a aba git no RStudio não estava com as pastas que eu fiz o commit. Apesar das pastas aparecerem na minha página do Git hub. Quando eu aperto em qualquer tecla da aba Git no RStudio (push, commit etc), aparece uma mensagem de erro "nome do diretório inválido". Não consegui entender o que aconteceu.
