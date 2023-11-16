# Automatizando a extração de dados do Active Directory para construção de relatórios.

Atualmente, existem diversas ferramentas disponíveis que facilitam a gestão do Active Directory (AD) para os administradores, especialmente no que diz respeito ao desenvolvimento de relatórios e gráficos. No entanto, muitas das melhores soluções são pagas, o que representa um obstáculo significativo para várias empresas.
Diante desse cenário, o objetivo deste projeto é oferecer suporte àqueles que desejam acessar e compilar informações do seu AD sem a necessidade de executar scripts repetidamente, criar planilhas ou realizar cruzamentos de dados no Excel cada vez que precisam elaborar relatórios. Além disso, o projeto visa auxiliar aqueles interessados em aprender a automatizar o processo de extração e montagem de relatórios do Active Directory, tornando a gestão mais eficiente e menos dependente de ferramentas pagas.

* ![image](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/blob/main/Imagens/pwb_user.PNG?raw=true)

Softwares que seram utilizados neste projeto:
|Software |Descrição|
|----|----|
| Active Directory |Origem dos dados
| PowerShell     |Ferramenta de extração
| Microsoft SQL Server  |Local para armazenar os dados.
| Power BI | Ferramenta de analise de dados.


### Atenção:
<i><b> Este projeto não tem objetivo de substituir ferramentas como [Varonis](https://www.varonis.com/blog/what-is-active-directory), porém é possível obter muitas das informações que o Varonis traz via PowerShell.</i></b>


### O que será feito neste projeto.
+ Criação de uma base de dados no MS SQL Server que vai armazenar os dados.
+ Desenvolvimento dos scripts de extração em PowerShell.
+ Desenvolvimento de View, procedures e functions no MS SQL Server que vão auxiliar no tratamento dos dados.
+ Automatizar a extração dos dados utilizando o MS SQL Agent.
+ Desenvolvimento dos painéis no Power BI Desktop.

### O que será extraido do Active Directory.
- Usuários
- Grupos
- Computadores
- Controladores de domínio.
- OU - Unidades organizacionais.
- Contatos.
- GPO - Diretiva de Grupo.

### Relatórios a serem desenvolvidos com as informações extraídas.
- Qualitativos:
    - Todos os usuários desativados que está fora da OU "BLOQUEADOS" e "DESATIVADOS"
    - Lista de usuários com a senha expirada, porém com a conta ativa.
    - Gráfico  com os indicadores de usuários que terão a conta expiradas nos próximos 60 dias.
    - Gráfico  com a proporção dos status das contas: "Ativa", "Desabilitada", Expirada” etc.
- Quantitativo:
    - Total de contas
    - Contas desativadas
    - Contas Ativas
    - Contas ativas de funcionários da casa.
    - Contas ativas de Cedidos
    - Contas ativas de Terceirizados.
    - Contas Ativas e expiradas.
    - Contas desativadas fora da OU "Bloqueados" ou "Desativados"  


## A execução do projeto será divido nos tópicos  abaixo:

+ [Desenvolvimento da base de dados.](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/blob/main/base_de_dados/README.md)
+ [Desenvolvimento dos scripts de extração em PowerShell.](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/blob/main/script_extracao/README.md)
+ [Executar o tratamento dos dados.](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/blob/main/tratamento_de_dados/README.md)
+ [Automatizar a extração dos dados utilizando o MS SQL Agent.](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/blob/main/automatizar_extra/README.md)
+ [Desenvolvimento dos painéis no Power BI Desktop.](https://github.com/j-a-vicente/Automatizando_a_extra_ao_Active_Directory_relatorios/tree/main/power_bi_desktop)
