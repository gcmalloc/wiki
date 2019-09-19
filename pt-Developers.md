<h2> Índice </h2><ul><li> <a href="#Introduction">Introdução</a> </li><li> <a href="#Dataset-integration">Integração de conjunto de dados</a> </li><li> <a href="#add-your-datasets-on-gitlab">Adicione seus conjuntos de dados no GitLab</a> </li><li> <a href="#List-of-main-repositories">Lista de repositórios principais</a> </li><li> <a href="#How-to-contribute-code">Como contribuir com código</a> </li><li> <a href="#Description-of-IT-infrastructure">Descrição da infraestrutura de TI</a> <ul><li> <a href="#Run-with-Docker">Executar com o Docker</a> </li><li> <a href="#Server-infrastructure">Infraestrutura do servidor</a> <ul><li> <a href="#Infrastructure">A infraestrutura</a> </li><li> <a href="#Performance">atuação</a> </li></ul></li></ul></li><li> <a href="#How-to-define-indicators">Como definir indicadores</a> </li><li> <a href="#References">Referências</a> </li><li> <a href="#How-to-cite">Como citar</a> </li><li> <a href="#Authors-and-reviewers">Autores e revisores</a> </li><li> <a href="#Acknowledgement">Reconhecimento</a> </li></ul><h2> Introdução </h2><p> Esta página contém todas as informações necessárias para que os desenvolvedores contribuam para a Plataforma Hotmaps ou entendam como está funcionando. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Integração de conjunto de dados </h2><p> A integração de novos conjuntos de dados públicos é tratada da seguinte maneira: </p><ol><li> os conjuntos de dados devem ser enviados para um repositório git ( <a href="#Add-your-datasets-on-GitLab">adicione seus conjuntos de dados no GitLab</a> ) </li><li> todas as noites um script integra os conjuntos de dados novos / atualizados à plataforma DEV </li><li> se tudo funcionou bem, o conjunto de dados agora está disponível na plataforma DEV e os desenvolvedores podem integrá-lo em seu código </li><li> Após a conclusão da codificação, os novos recursos são adicionados à plataforma de produção por meio de uma nova versão </li></ol><p><img alt="integração de dados" src="images/data-integration-workflow.png"/></p><p> Se um conjunto de dados falhar durante a integração, um problema será criado no Taiga (plataforma de gerenciamento de projetos). A questão mostra o erro levantado e o desenvolvedor deve corrigi-lo e enviar novamente seu trabalho ao Git para que o script possa tentar integrá-lo novamente na noite seguinte. </p><p> O código-fonte do script de integração está disponível neste link: <a href="https://github.com/HotMaps/CI_DatasetIntegration">Integração de dados</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Adicione seus conjuntos de dados no GitLab </h2><p> Para adicionar conjuntos de dados à lista de conjuntos públicos, eles devem ser enviados para um novo repositório Git no GitLab. Aqui está a organização GitLab onde os conjuntos de dados devem ser enviados: <a href="https://gitlab.com/hotmaps">Conjuntos de dados no GitLab</a> . </p><p> Uma vez por dia, os repositórios são verificados quanto a novas confirmações e integrados, se houver. O processo de integração verifica se os dados estão em conformidade com a especificação ou não. </p><p> Aqui está a especificação: <a href="uploads/Hotmaps_Data-upload-on-Gitlab_2017-12-04_V4.pdf">Hotmaps_Data-upload-on-Gitlab_2017-12-04_V4.pdf</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Lista de repositórios principais </h2><p> O código do aplicativo está localizado no GitHub na <a href="https://github.com/HotMaps">organização Hotmaps</a> . Esta organização possui vários repositórios </p><ul><li> <a href="https://github.com/HotMaps/Hotmaps-toolbox-service">Hotmaps-toolbox-client</a> contém o frontend do nosso aplicativo. É um projeto Angular (JavaScript) </li><li> <a href="https://github.com/HotMaps/Hotmaps-toolbox-service">Hotmaps-toolbox-service</a> contém a API para nosso aplicativo. É baseado em Flask (Python) </li><li> <a href="https://github.com/HotMaps/hotmaps_wiki">Hotmaps-wiki</a> é o Wiki que você está lendo atualmente </li><li> <a href="https://github.com/HotMaps/base_calculation_module">módulo de cálculo base</a> é o modelo básico que você pode usar para criar seus próprios módulos de cálculo para Hotmaps </li><li> uma lista de módulos de cálculos </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Como contribuir com código </h2><p> Se você deseja adicionar algum código aos Hotmaps, você tem duas possibilidades: se deseja atualizar a interface ou o back-end diretamente, é necessário modificar o cliente ou o repositório de serviços da caixa de ferramentas. Se você deseja adicionar seu próprio módulo de cálculo, é possível criar seu próprio repositório seguindo <a href="https://github.com/HotMaps/base_calculation_module">o leia-me do repositório base_calculation_module</a> </p><p> Se você deseja executar algum trabalho no repositório Git, não trabalhe diretamente com o ramo principal. Crie uma nova ramificação a partir da ramificação de desenvolvimento, faça seu trabalho nesta ramificação e, quando seu recurso for testado, você poderá mesclar seu trabalho com a ramificação de desenvolvimento, como mostra o gráfico a seguir. </p><p><img alt="git_workflow" src="images/git_workflow.png"/></p><p> Para enviar algo para algum repositório de Hotmaps, você precisa ser membro da equipe de Hotmaps. Se não estiver, ainda poderá executar um fork da nossa ferramenta para desenvolver sua própria ferramenta. </p><p> Você pode encontrar mais informações sobre como trabalhar nestes documentos: </p><ul><li> <a href="uploads/Hotmaps_python_best_practices_tutorial_2017-08-07_v01.pdf">Hotmaps_python_best_practices_tutorial_2017-08-07_v01.pdf</a> </li><li> <a href="uploads/Hotmaps_Testing_in_python_tutorial_pytest_2017-08-07_v01.pdf">Hotmaps_Testing_in_python_tutorial_pytest_2017-08-07_v01.pdf</a> </li><li> <a href="uploads/GitFlow_Guidelines_CREM_2017-02-01.pdf">GitFlow_Guidelines_CREM_2017-02-01.pdf</a> </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Descrição da infraestrutura de TI </h2><p><img alt="ReverseProxy_architecture_latest" src="images/ReverseProxy_architecture_latest.png"/></p><p> Todos os serviços e componentes são usados através de seu próprio contêiner Docker. Todos esses contêineres são definidos em um único arquivo de composição do docker. A imagem acima representa a arquitetura de TI dos Hotmaps. </p><p> Algumas organizações parceiras limitaram a comunicação apenas à porta 80. Para evitar os problemas causados por essa limitação, foi criada a criação de um proxy reverso. Esse proxy reverso oferece um único ponto de entrada e depois distribui a solicitação enviada pelo cliente ao serviço em questão. O proxy reverso é composto por três componentes: </p><ol><li> Servidor proxy reverso: serve como um ponto de entrada exclusivo e distribui solicitações para os serviços certos. </li><li> Proxy-gen: é um serviço que mapeia automaticamente todos os serviços no proxy reverso. Portanto, não é necessário adicionar manualmente um novo serviço à configuração do proxy </li><li> lets-encrypt: é um serviço que permite o uso do protocolo SSL. É necessário para ativar o protocolo https. Os certificados SSL são assinados por um endereço de email configurado neste serviço. </li></ol><p> Existem três redes: </p><ul><li> hotmaps_nginx permite que o proxy reverso se comunique com a API, o front-end e o servidor geográfico. Ele permite principalmente distribuir uma solicitação para o serviço correto entre os três. </li><li> hotmaps_backend permite a comunicação entre todos os componentes do backend: api, frontend, geoserver e o banco de dados PostgreSQL. </li><li> hotmaps_cm-net permite a comunicação entre cada módulo de cálculo e a API. </li></ul><p> Cada módulo de cálculo possui seu próprio contêiner Docker. </p><h3> Executar com o Docker </h3><p> HotMaps usa <a href="https://www.docker.com/">Docker</a> software e <a href="https://docs.docker.com/compose/">Docker-Compose</a> ferramenta para gerenciar recipientes. Um arquivo docker-compose.yml contém toda a configuração da arquitetura do Docker (configuração de contêineres, redes, links, ...). Isso permite que os contêineres sejam executados com um comando simples: </p><pre> <code class="language-shell">docker-compose up</code> </pre><p> <em>Há mais sobre docker-compose no site da Web do Docker: <a href="https://docs.docker.com/compose/reference/">Redigir referência de linha de comando</a> e <a href="https://docs.docker.com/compose/compose-file/">Redigir referência de arquivo</a> .</em> </p><p> Existe apenas um contêiner que é executado separadamente dos outros: é o banco de dados, porque precisa ficar sempre ativo. É por isso que não está no arquivo de configuração do docker-compose. </p><h3> Infraestrutura do servidor </h3><h4> A infraestrutura </h4><p> No momento, o servidor está hospedado no HES-SO na Suíça. Existem 2 máquinas disponíveis: uma para desenvolvimento (desenvolvimento e teste) e outra para produção (a caixa de ferramentas real, disponível em <a href="https://www.hotmaps.eu">www.hotmaps.eu</a> ). </p><p> Ambas as máquinas têm a mesma especificação: </p><ul><li> Processador: Intel Xeon E5-2680 v4 (8) @ 2.4GHz) </li><li> RAM: 16GB </li><li> HDD: 500GB </li><li> SO: Ubutnu 16.04 LTS </li></ul><h4> atuação </h4><p> Frequentemente, executamos testes de desempenho no servidor de desenvolvimento para garantir uma certa quantidade de usuários simultâneos. </p><p> Como exemplo, abaixo estão os resultados da primeira versão beta versus os testes de versão futura. A nova versão inclui algumas melhorias de desempenho. </p><p> <em>Este exemplo mostra os testes de desempenho de usuários simultâneos usando a mesma função: "curva de duração para seleção de hectares". A linha em negrito mostra o limite em que o servidor começa a gerar erros. A seleção de hectares é um bom exemplo, pois mostra as consultas que requerem mais recursos.</em> </p><p> <strong>Versão beta de março de 2019</strong> </p><p> | Nb de usuários simulados | Tempo médio | Mediana Tempo máximo | Tempo mínimo | Percentagem de erros | | --------------------- | ------------ | ------ | -------- | -------- | -------------------- | | 1 | 2936 2936 2936 2936 0 | 20 9329 9503 11778 6901 0 | 50 22922 22713 33401 8661 0 | <strong>100</strong> 33302 32875 58257 4929 <strong>16</strong> | 200 na | na | na | na | na | | 300 na | na | na | na | na | </p><p> <strong>Lançamento futuro no DEV (março de 2019)</strong> </p><p> | Nb de usuários simulados | Tempo médio | Mediana Tempo máximo | Tempo mínimo | Percentagem de erros | | --------------------- | ------------ | ------ | -------- | -------- | -------------------- | | 1 | 1802 1802 1802 1802 0 | 20 5289 2677 6873 2149 0 | 50 10775 11274 17081 2577 0 | 100 19807 20280 35142 3156 0 | 200 37302 37575 69930 3381 0 | <strong>300</strong> 49091 57536 83578 2447 <strong>26</strong> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Como definir indicadores </h2><p> <a href="indicator_readme">Definição de Indicador</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Referências </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Como citar </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Autores e revisores </h2><p> Autores: </p><ul><li> Daniel Hunacek </li><li> Lucien Zuber </li><li> Matthieu Dayer </li></ul><p> Revisores: </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Reconhecimento </h2><p> Gostaríamos de expressar nossa mais profunda gratidão ao <a href="https://www.hotmaps-project.eu">Projeto</a> Horizonte <a href="https://www.hotmaps-project.eu">Hotmaps</a> 2020 (Contrato de Doação número 723677), que forneceu o financiamento para a realização da presente investigação </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2></h2>

This page was automatically translated. View in another language:

[English](en-Developers) (original) [Bulgarian](bg-Developers)<sup>\*</sup> [Croatian](hr-Developers)<sup>\*</sup> [Czech](cs-Developers)<sup>\*</sup> [Danish](da-Developers)<sup>\*</sup> [Dutch](nl-Developers)<sup>\*</sup> [Estonian](et-Developers)<sup>\*</sup> [Finnish](fi-Developers)<sup>\*</sup> [French](fr-Developers)<sup>\*</sup> [German](de-Developers)<sup>\*</sup> [Greek](el-Developers)<sup>\*</sup> [Hungarian](hu-Developers)<sup>\*</sup> [Irish](ga-Developers)<sup>\*</sup> [Italian](it-Developers)<sup>\*</sup> [Latvian](lv-Developers)<sup>\*</sup> [Lithuanian](lt-Developers)<sup>\*</sup> [Maltese](mt-Developers)<sup>\*</sup> [Polish](pl-Developers)<sup>\*</sup>  [Romanian](ro-Developers)<sup>\*</sup> [Slovak](sk-Developers)<sup>\*</sup> [Slovenian](sl-Developers)<sup>\*</sup> [Spanish](es-Developers)<sup>\*</sup> [Swedish](sv-Developers)<sup>\*</sup>
<sup>\*</sup>: machine translated