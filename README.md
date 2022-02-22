# Teste de Python - MoreDeve
Teste de Python para testar habilidades com `OOP` e `Estrutura de dados básicas`.
> #### Antes de iniciar o teste preencha as váriaveis `NOME_DO_CANDIDATO` com seu nome completo e `EMAIL_DO_CANDIDATO` com o seu email.
---
## Desafio
Empresas que possuem um setor altamente regulamentado temem Atos normativos (Leis, Decretos, ...) que impactam na existência da própria empresa. \
Normalmente elas adotam uma posição de vigia, ficando de olho em novas Normas para, no pior dos casos, ter mais tempo para se preparar. \
O intuito desse desafio é fazer o download dos `PDFs` dos Jornais (Diários Oficiais) e extrair algumas informações básicas. 
####
Para isso é necessário fazer os seguintes métodos da classe `JournalDownloader`:
> ### Baixar os jornais
> Os métodos abaixo deverão baixar os jornais de um determinado período de tempo e enviar para o método **dump_json**:
> * o `caminho do PDF`,
> * o `número da edição`,
> * a `data`. \
> O **dump_json** retornará o caminho do `JSON` criado. \
> Esses métodos deverão retornar uma lista dos caminhos dos `JSONs`.
> > **get_day_journals** \
> Pega todos os jornais de um determinado dia. 
> 
> > **get_month_journals** \
> Pega todos os jornais de um determinado mês.
> 
> > **get_year_journals**\
> Pega todos os jornais de um determinado ano.
 
> **parse** \
Extrai informações da resposta do `request_journals` e retorna uma lista de tuplas composta pela data e edição.

> **download_all** \
Baixa todos os jornais passados pelo argumento `editions`, os `PDFs` devem estar contido na pasta `pdfs`.
> Os nomes dos `PDFs` devem estar com o nome em ordem, exemplo: `0.pdf`, `1.pdf`, ...\
> Execute o método `dump_json` passando nos argumentos o caminho do `PDF`, o `número de edição` e a `data`, respectiviamente, para salvar um `JSON` contendo essas informações.\
> Retorna a lista dos caminhos dos `JSONs`.
---
## Observações
* Use o `assert` para garantir que a data não esteja no futuro e seja válida. 
* O ano mínimo deverá ser `1970`.
* Ordene os resultados pelo número de edição.
* Não altere os nomes das funções, métodos e classes já estabelecidos. 
###
Utilize as funções disponibilizadas:

> **request_journals** \
Retorna a resposta como dicionário, caso exista, dos jornais de um período dado.
> O período é definido do `start_date` ao `end_date`, esses argumentos devem ser em string no padrão `ano-mês-dia`.
> Exemplo: `2022-02-20`

> **download_mutiple_jornals** \
Baixa os jornais por meio do seus números de edições (`editions`) e salva em seu respectivos caminhos para onde deve ser baixado (`paths`) especificados.
> Retorna os caminhos dos `PDFs`.