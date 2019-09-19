<h2> Innehållsförteckning </h2><ul><li> <a href="#Introduction">Introduktion</a> </li><li> <a href="#Dataset-integration">Datasatsintegration</a> </li><li> <a href="#add-your-datasets-on-gitlab">Lägg till dina datasätt på GitLab</a> </li><li> <a href="#List-of-main-repositories">Lista över huvudförvar</a> </li><li> <a href="#How-to-contribute-code">Hur man bidrar med kod</a> </li><li> <a href="#Description-of-IT-infrastructure">Beskrivning av IT-infrastruktur</a> <ul><li> <a href="#Run-with-Docker">Kör med Docker</a> </li><li> <a href="#Server-infrastructure">Serverinfrastruktur</a> <ul><li> <a href="#Infrastructure">Infrastruktur</a> </li><li> <a href="#Performance">Prestanda</a> </li></ul></li></ul></li><li> <a href="#How-to-define-indicators">Hur man definierar indikatorer</a> </li><li> <a href="#References">referenser</a> </li><li> <a href="#How-to-cite">Hur man citerar</a> </li><li> <a href="#Authors-and-reviewers">Författare och granskare</a> </li><li> <a href="#Acknowledgement">Bekräftelse</a> </li></ul><h2> Introduktion </h2><p> Denna sida innehåller all information som krävs för att utvecklare ska kunna bidra till Hotmaps-plattformen eller för att förstå hur den fungerar. </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Datasatsintegration </h2><p> Integration av nya offentliga datasätt hanteras enligt följande: </p><ol><li> datasätt måste skjutas till ett git-arkiv ( <a href="#Add-your-datasets-on-GitLab">Lägg till dina datasätt på GitLab</a> ) </li><li> varje kväll integrerar ett skript de nya / uppdaterade datasätten till DEV-plattformen </li><li> om allt fungerade bra är datasatsen nu tillgänglig på DEV-plattformen och utvecklare kan integrera det i sin kod </li><li> När kodningen är klar läggs de nya funktionerna till produktionsplattformen genom en ny version </li></ol><p><img alt="dataintegration" src="images/data-integration-workflow.png"/></p><p> Om ett dataset misslyckas under integration skapas ett problem på Taiga (projekthanteringsplattform). Problemet visar felet och utvecklaren bör fixa det och skjuta igen sitt arbete till Git så att manuset kan försöka integrera det igen nästa kväll. </p><p> Källkoden för integrationsskriptet finns på denna länk: <a href="https://github.com/HotMaps/CI_DatasetIntegration">Dataintegration</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Lägg till dina datasätt på GitLab </h2><p> För att lägga till datasätt i listan över offentliga datasätt måste de drivas till ett nytt Git-arkiv på GitLab. Här är GitLab-organisationen där datasätt ska skjutas: <a href="https://gitlab.com/hotmaps">Datasätt på GitLab</a> . </p><p> En gång om dagen kontrolleras förvaren för nya åtaganden och integreras i så fall. Integrationsprocessen kontrollerar om uppgifterna överensstämmer med specifikationen eller inte. </p><p> Här är specifikationen: <a href="uploads/Hotmaps_Data-upload-on-Gitlab_2017-12-04_V4.pdf">Hotmaps_Data-upload-on-Gitlab_2017-12-04_V4.pdf</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Lista över huvudförvar </h2><p> Applikationskoden finns på GitHub under <a href="https://github.com/HotMaps">Hotmaps-organisationen</a> . Denna organisation äger flera förvar </p><ul><li> <a href="https://github.com/HotMaps/Hotmaps-toolbox-service">Hotmaps-toolbox-client</a> innehåller frontend för vår applikation. Det är ett vinkelprojekt (JavaScript) </li><li> <a href="https://github.com/HotMaps/Hotmaps-toolbox-service">Hotmaps-toolbox-service</a> innehåller API för vår applikation. Det är baserat på Flask (Python) </li><li> <a href="https://github.com/HotMaps/hotmaps_wiki">Hotmaps-wiki</a> är den Wiki du läser för närvarande </li><li> <a href="https://github.com/HotMaps/base_calculation_module">basberäkningsmodul</a> är den grundmallen du kan använda för att skapa dina egna beräkningsmoduler för Hotmaps </li><li> en lista med beräkningsmoduler </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Hur man bidrar med kod </h2><p> Om du vill lägga till en kod till Hotmaps har du två möjligheter: om du vill uppdatera gränssnittet eller backend direkt måste du ändra klienten eller servicelageret i verktygslådan. Om du vill lägga till din egen beräkningsmodul kan du skapa ditt eget förvar genom att följa <a href="https://github.com/HotMaps/base_calculation_module">readme för bas_calculation_module-förvaret</a> </p><p> Om du vill utföra lite arbete på Git-förvaret, vänligen arbeta inte direkt med mastergrenen. Skapa en ny gren från utvecklingsgrenen, gör ditt arbete med den här grenen och när din funktion testas kan du slå samman ditt arbete med utvecklingsgrenen som visas i följande graf. </p><p><img alt="git_workflow" src="images/git_workflow.png"/></p><p> För att driva något till något Hotmaps-arkiv måste du vara medlem i Hotmaps-teamet, om du inte är det kan du fortfarande utföra en gaffel av vårt verktyg för att utveckla ditt eget verktyg. </p><p> Du kan hitta mer information om hur du arbetar i dessa dokument: </p><ul><li> <a href="uploads/Hotmaps_python_best_practices_tutorial_2017-08-07_v01.pdf">Hotmaps_python_best_practices_tutorial_2017-08-07_v01.pdf</a> </li><li> <a href="uploads/Hotmaps_Testing_in_python_tutorial_pytest_2017-08-07_v01.pdf">Hotmaps_Testing_in_python_tutorial_pytest_2017-08-07_v01.pdf</a> </li><li> <a href="uploads/GitFlow_Guidelines_CREM_2017-02-01.pdf">GitFlow_Guidelines_CREM_2017-02-01.pdf</a> </li></ul><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Beskrivning av IT-infrastruktur </h2><p><img alt="ReverseProxy_architecture_latest" src="images/ReverseProxy_architecture_latest.png"/></p><p> Alla tjänster och komponenter används via sin egen Docker-behållare. Alla dessa behållare definieras i en enda docker-komponera fil. Bilden ovan representerar IT-arkitekturen för Hotmaps. </p><p> Vissa partnerorganisationer begränsade endast kommunikationen till port 80. För att undvika problem orsakade av denna begränsning skapades en omvänd proxy. Denna omvända proxy erbjuder ett enda startpunkt och distribuerar sedan begäran som skickas av kunden till den berörda tjänsten. Den omvända proxy består av tre komponenter: </p><ol><li> Omvänd proxyserver: den fungerar som en unik startpunkt och distribuerar förfrågningar till rätt tjänster. </li><li> Proxy-gen: det är en tjänst som automatiskt kartar alla tjänster i omvänd proxy. Det är således inte nödvändigt att manuellt lägga till en ny tjänst i proxykonfigurationen </li><li> lets-encrypt: det är en tjänst som tillåter användning av SSL-protokollet. Det är nödvändigt för att aktivera https-protokollet. SSL-certifikaten undertecknas av en e-postadress som är konfigurerad i den här tjänsten. </li></ol><p> Tre nätverk finns: </p><ul><li> hotmaps_nginx tillåter den omvända proxy att kommunicera med api, frontend och geoserver. Den tillåter främst att distribuera en begäran till rätt tjänst bland de tre. </li><li> hotmaps_backend tillåter kommunikation mellan alla komponenter i backend: api, frontend, geoserver och PostgreSQL-databasen. </li><li> hotmaps_cm-net tillåter kommunikation mellan varje beräkningsmodul och api. </li></ul><p> Varje beräkningsmodul har sin egen Docker-behållare. </p><h3> Kör med Docker </h3><p> Hotmaps använder <a href="https://www.docker.com/">Docker-</a> programvara och <a href="https://docs.docker.com/compose/">Docker-Compose-</a> verktyg för att hantera containrar. En docker-compose.yml-fil innehåller hela konfigurationen av Docker-arkitekturen (konfiguration av containrar, nätverk, länkar, ...). Detta gör att containrar kan köras med ett enkelt kommando: </p><pre> <code class="language-shell">docker-compose up</code> </pre><p> <em>Det finns mer om docker-compose på webbanan för Docker: <a href="https://docs.docker.com/compose/reference/">Compose command-line reference</a> and <a href="https://docs.docker.com/compose/compose-file/">Compose file reference</a> .</em> </p><p> Det finns bara en behållare som körs separat från andra: det är databasen eftersom den måste hålla sig uppe hela tiden. Det är därför det inte finns i konfigurationsfilen för docker-compose. </p><h3> Serverinfrastruktur </h3><h4> Infrastruktur </h4><p> För tillfället är servern värd på HES-SO i Schweiz. Det finns två maskiner tillgängliga: en för utveckling (utveckling och testning) och en för produktion (själva verktygslådan, tillgänglig på <a href="https://www.hotmaps.eu">www.hotmaps.eu</a> ). </p><p> Båda maskinerna har samma specifikation: </p><ul><li> CPU: Intel Xeon E5-2680 v4 (8) @ 2,4 GHz) </li><li> RAM: 16 GB </li><li> HDD: 500 GB </li><li> OS: Ubutnu 16.04 LTS </li></ul><h4> Prestanda </h4><p> Vi kör ofta prestanda tester på utvecklingsservern för att garantera en viss mängd samtidiga användare. </p><p> Som ett exempel nedan är resultaten av den första beta-frisättningen jämfört med framtida frisättningstester. Den nya versionen innehåller några prestandaförbättringar. </p><p> <em>Detta exempel visar prestanda tester för samtidiga användare som använder samma funktion: "varaktighetskurva för val av hektar". Den djärva raden visar gränsen där servern börjar ta upp fel. Val av hektar är ett bra exempel eftersom det visar de frågor som kräver mest resurser.</em> </p><p> <strong>Beta release av mars 2019</strong> </p><p> | Antal simulerade användare | Genomsnittlig tid | Median | Max tid | Min tid | Procentandel av fel | | --------------------- | ------------ | ------ | -------- | -------- | -------------------- | | 1 | 2936 | 2936 | 2936 | 2936 | 0 | | 20 | 9329 | 9503 | 11778 | 6901 | 0 | | 50 | 22922 | 22713 | 33401 | 8661 | 0 | | <strong>100</strong> | 33302 | 32875 | 58257 | 4929 | <strong>16</strong> | | 200 | na | na | na | na | na | | 300 | na | na | na | na | na | </p><p> <strong>Framtida släpp på DEV (mars 2019)</strong> </p><p> | Antal simulerade användare | Genomsnittlig tid | Median | Max tid | Min tid | Procentandel av fel | | --------------------- | ------------ | ------ | -------- | -------- | -------------------- | | 1 | 1802 | 1802 | 1802 | 1802 | 0 | | 20 | 5289 | 2677 | 6873 | 2149 | 0 | | 50 | 10775 | 11274 | 17081 | 2577 | 0 | | 100 | 19807 | 20280 | 35142 | 3156 | 0 | | 200 | 37302 | 37575 | 69930 | 3381 | 0 | | <strong>300</strong> | 49091 | 57536 | 83578 | 2447 | <strong>26</strong> | </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Hur man definierar indikatorer </h2><p> <a href="indicator_readme">Indikator Definiton</a> </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> referenser </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Hur man citerar </h2><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Författare och granskare </h2><p> Författare: </p><ul><li> Daniel Hunacek </li><li> Lucien Zuber </li><li> Matthieu Dayer </li></ul><p> granskare: </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2> Bekräftelse </h2><p> Vi vill förmedla vår djupaste uppskattning till Horizon 2020 <a href="https://www.hotmaps-project.eu">Hotmaps-projektet</a> (bidragsavtal nummer 723677), som gav finansieringen för att genomföra den nuvarande utredningen </p><p><ins> <code><strong><a href="#table-of-contents">To Top</a></strong></code> </ins> </p><h2></h2>

This page was automatically translated. View in another language:

[English](en-Developers) (original) [Bulgarian](bg-Developers)<sup>\*</sup> [Croatian](hr-Developers)<sup>\*</sup> [Czech](cs-Developers)<sup>\*</sup> [Danish](da-Developers)<sup>\*</sup> [Dutch](nl-Developers)<sup>\*</sup> [Estonian](et-Developers)<sup>\*</sup> [Finnish](fi-Developers)<sup>\*</sup> [French](fr-Developers)<sup>\*</sup> [German](de-Developers)<sup>\*</sup> [Greek](el-Developers)<sup>\*</sup> [Hungarian](hu-Developers)<sup>\*</sup> [Irish](ga-Developers)<sup>\*</sup> [Italian](it-Developers)<sup>\*</sup> [Latvian](lv-Developers)<sup>\*</sup> [Lithuanian](lt-Developers)<sup>\*</sup> [Maltese](mt-Developers)<sup>\*</sup> [Polish](pl-Developers)<sup>\*</sup> [Portuguese (Portugal, Brazil)](pt-Developers)<sup>\*</sup> [Romanian](ro-Developers)<sup>\*</sup> [Slovak](sk-Developers)<sup>\*</sup> [Slovenian](sl-Developers)<sup>\*</sup> [Spanish](es-Developers)<sup>\*</sup>
<sup>\*</sup>: machine translated