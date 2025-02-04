---
lab:
  title: 'Übung: Beschleunigen Sie die App-Entwicklung mit GitHub Copilot'
  type: Answer Key
  module: Modules 2-5
---

# Übung: Beschleunigen Sie die App-Entwicklung mit GitHub Copilot
# Antwortschlüssel für Schülerlabs

## Teil 1: Analysieren und Dokumentieren von Code mithilfe von GitHub Copilot-Tools

### Vor der Installation

#### Projektübersicht

Sie sind Softwareentwickler und arbeiten für eine regionale IT-Abteilung. Die meisten Anwendungen, die Sie verwenden, unterstützen die lokale Community. Vor kurzem wurden die Server der Gemeindebibliothek bei einem Unfall beschädigt, und es wird Wochen dauern, bis die Genehmigung für den Austausch der Server vorliegt. Ihre Abteilung muss eine temporäre Lösung entwickeln, mit Bibliothekare grundlegende Aufgaben ausführen können.

Ihr Team hat sich mit den Bibliothekaren getroffen. Sie benötigen eine Mindestlösung, die es ihnen ermöglicht, Bibliothekskunden die wesentlichen Dienstleistungen wie Buchleihen und -rückgaben zu bieten. Ihr Team untersucht die verfügbaren Ressourcen und entwickelt einen Plan. Zunächst wird das Projekt nur Ihnen und einem weiteren Kollegen zugewiesen. Die lokalen Behörden haben die Bibliothek geschlossen, bis Ihre temporäre Lösung verfügbar ist. Sie haben drei Tage Zeit, eine erste Version der Lösung zu entwickeln, mit der die Bibliothek erneut geöffnet werden kann.

Während Ihr Kollege mit der Arbeit an der Software beginnt, verwenden Sie Bibliotheksdatensätze, um JSON-Dateien zu erstellen, die die Kundenkonten, Bücher und Buchausleihen der Bibliothek darstellen. Am Ende des zweiten Tages können Sie beim Code helfen. Die Lösung ist eine Konsolenanwendung, die auf einem der Laptopcomputer der Bibliothek ausgeführt werden kann. Die Bibliothekare verstehen, dass die Zeit nicht für eine schöne Benutzeroberfläche ausreicht, betonen jedoch, dass die App sicher und zuverlässig sein muss. Sie haben noch einen Tag Zeit, bevor Sie Version 1.0 Ihrer App vorführen müssen.

Sie verwenden GitHub Copilot, um die Arbeit so effizient wie möglich zu erledigen. Wenn alles gut geht, wird Ihre App verwendet, um die Leihabläufe der Bibliothek und andere Offsite-Funktionen in Zukunft zu unterstützen.

#### Übungsszenario (Teil 1)

GitHub Copilot kann Ihnen dabei helfen, eine Codebasis zu verstehen und zu dokumentieren, indem Erklärungen und Dokumentation generiert werden.

In Teil 1 dieser Übung verwenden Sie GitHub Copilot, um die Bibliotheksanwendung zu analysieren und zu dokumentieren. Sie erstellen auch ein GitHub-Repository für die Bibliotheksanwendung und generieren mit GitHub Copilot eine Infodatei für das Repository.

Teil 1 umfasst die folgenden Übungen:

- Konfigurieren der GitHub Copilot-Erweiterungen für Visual Studio Code
- Verwenden von GitHub Copilot zum Erklären der Codebasis der Bibliotheksanwendung
- Verwenden von Visual Studio Code zum Erstellen eines GitHub-Repositorys für die Bibliotheksanwendung
- Verwenden Sie die GitHub Copilot-Erweiterungen, um eine README.md-Datei für das Repository zu erstellen.

### Übung 1: Konfigurieren von GitHub Copilot-Erweiterungen für Visual Studio Code

Sie verwenden Ihr GitHub-Konto, um Visual Studio Code zu autorisieren und Ihr GitHub Copilot-Abonnement zu überprüfen.

Führen Sie die folgenden Schritte aus, um die Erweiterungen zu installieren.

1. Öffnen Sie ein Browserfenster.

1. Navigieren Sie zur folgenden URL, um das GitHub Enterprise-Portal zu öffnen:

    ```plaintext
    https://github.com/enterprises/Microsoft-APL/sso
    ```

1. Melden Sie sich mit den folgenden Anmeldeinformationen bei Ihrem GitHub-Konto an:

    E-Mail/Benutzername: `@lab.CloudPortalCredential(1).Username`

    Kennwort: `@lab.CloudPortalCredential(1).Password`

1. Öffnen Sie Visual Studio Code.

1. Wählen Sie im linken Menü die Option **Erweiterungen** aus.

1. Geben Sie im Textfeld „Nach Extensions in Marketplace suchen“ den Suchbegriff **GitHub Copilot** ein, und drücken Sie die EINGABETASTE.

1. Wählen Sie in der gefilterten Liste der Erweiterungen die Erweiterung **„GitHub Copilot**“ aus, die von GitHub erstellt wurde.

1. Wählen Sie auf der GitHub Copilot-Erweiterungsseite **Installieren** aus.

1. Wenn Sie die Benachrichtigung „Melden Sie sich an, um GitHub Copilot zu verwenden“ sehen, wählen Sie „**Bei GitHub anmelden** aus.

    Wenn Sie einen Dialog sehen, der besagt, dass sich GitHub Copilot über GitHub anmelden möchte, wählen Sie „**Zulassen**“ aus.

    Da Sie bereits in Ihrem GitHub-Konto in einem Browserfenster angemeldet sind, sollte sich in Ihrem Browserfenster eine neue Registerkarte „Sitzung überprüfen“ öffnen.

1. Wählen Sie auf der Seite "Sitzung überprüfen" die Option **Weiter** aus.

1. Wählen Sie auf der Seite „Anwendung autorisieren“ die Option**Visual Studio Code autorisieren** aus.

1. Um zu Visual Studio Code zurückzukehren, wählen Sie **Öffnen** aus.

1. Schließen Sie Visual Studio Code und öffnen Sie es anschließend erneut.

    Durch den Neustart von Visual Studio Code wird sichergestellt, dass GitHub Copilot in die Visual Studio Code-Benutzeroberfläche integriert ist.

1. Beachten Sie, dass die Schaltfläche **Open Chat** jetzt auf der rechten Seite des Command Center oben im Visual Studio Code-Fenster sichtbar ist.

#### Zusammenfassung - der Übung 1

In dieser Übung haben Sie die GitHub Copilot-Erweiterung in Visual Studio Code installiert. Sie haben Visual Studio Code auch autorisiert, auf Ihr GitHub-Konto zuzugreifen. Sie können nun GitHub Copilot verwenden, um die Codebasis der Bibliotheksanwendung zu analysieren und zu dokumentieren.

### Übung 2: Analysieren der Codebasis der Bibliotheksanwendung

Bevor Sie ein Coderepository und eine Infodatei erstellen, sollten Sie sich einen Moment Zeit nehmen, um die Codebasis zu untersuchen. Es ist wichtig, die App-Architektur und die wichtigsten Features zu verstehen, bevor Sie das Projekt dokumentieren. Sie sollten die Anwendung auch ausführen, um sicherzustellen, dass sie erwartungsgemäß funktioniert.

#### Aufgabe 1: Laden der Bibliotheksanwendung in Ihre Entwicklungsumgebung

Ihr Kollege hat eine erste Version der Bibliotheksanwendung entwickelt und als ZIP-Datei zur Verfügung gestellt. Um sich auf diese Übung vorzubereiten, müssen Sie die folgenden Aktionen ausführen:

- Laden Sie eine ZIP-Datei herunter, die die Lösung enthält.
- Extrahieren der Codedateien
- Öffnen Sie die Bibliotheksanwendung in Visual Studio Code, und stellen Sie sicher, dass sie erfolgreich erstellt wird.

Gehen Sie folgendermaßen vor, um die Bibliotheksanwendung einzurichten:

1. Stellen Sie sicher, dass Ihr Webbrowser geöffnet ist, und öffnen Sie dann eine neue Browserregisterkarte.

1. Um die Zip-Datei mit Ihrem Codeprojekt herunterzuladen, navigieren Sie zu der folgenden URL:

    ```plaintext
    https://raw.githubusercontent.com/MicrosoftLearning/APL-2007-Accelerate-app-development-by-using-GitHub-Copilot/master/LearnModuleExercises/Downloads/GuidedProjectApp.zip
    ```

    Die ZIP-Datei, die Ihren Lösungscode enthält, GuidedProjectApp.zip, sollte automatisch heruntergeladen werden.

1. Sobald der Download abgeschlossen ist, schließen Sie die Browserregisterkarte.

    Lassen Sie die Browserseite für Ihr GitHub-Konto geöffnet. Sie werden diese später in der Übung brauchen.

1. Öffnen Sie den Windows-Datei-Explorer und navigieren Sie zum Ordner „Downloads“.

1. Entpacken Sie die heruntergeladenen Projektdateien.

    Entpacken Sie das Codeprojekt in Ihrer Entwicklungsumgebung. Zum Beispiel:

    1. Navigieren Sie auf Ihrem lokalen Computer zu Ihrem Downloadordner.

    1. Klicken Sie mit der rechten Maustaste auf **GuidedProjectApp.zip**, und wählen Sie dann **Alle extrahieren** aus.

    1. Wählen Sie **Dateien nach Extrahierung anzeigen** und dann **Extrahieren** aus.

    1. Notieren Sie sich den Speicherort des extrahierten Ordners.

1. Kopieren Sie den extrahierten Ordner „AccelerateDevGitHubCopilot“ an einen leicht zugänglichen Speicherort, z. B. in Ihren Windows-Desktop-Ordner.

1. Öffnen Sie den Ordner **AccelerateDevGitHubCopilot** in Visual Studio Code.

    Zum Beispiel:

    1. Öffnen Sie Visual Studio Code auf Ihrem PC.

    1. Wählen Sie in Visual Studio Code im Menü **Datei** die Option **Ordner öffnen** aus.

    1. Navigieren Sie zum Windows-Desktop-Ordner und suchen Sie dann den Ordner **AccelerateDevGitHubCopilot**.

    1. Wählen Sie **AccelerateDevGitHubCopilot** und dann **Ordner auswählen** aus.

    1. Wählen Sie **Ja, ich vertraue den Autoren** aus.

    > [!NOTE]
    > Es kann 10 bis 20 Sekunden dauern, bis Visual Studio Code die Projektdateien und alle erforderlichen .NET-Updates lädt.

1. Wählen Sie in der Visual Studio Code-Ansicht „EXPLORER“ die Option „SOLUTION EXPLORER“ aus und überprüfen Sie dann die folgende Projektstruktur:

    - AccelerateDevGitHubCopilot\
        - src\
            - Library.ApplicationCore\
            - Library.Console\
            - Library.Infrastructure\
        - tests\
            - UnitTests\

1. Stellen Sie sicher, dass die Lösung erfolgreich erstellt wird.

    Um beispielsweise die Projektmappe in der Ansicht „PROJEKTMAPPEN-EXPLORER“ zu erstellen, klicken Sie mit der rechten Maustaste auf **AccelerateDevGitHubCopilot**, und wählen Sie anschließend **Erstellen** aus.

    Es werden mehrere **Warnungen** angezeigt, es sollten aber keine Fehler auftreten. Sie führen die Anwendung später in dieser Übung aus.

    > [!NOTE]
    > Installieren Sie keine Workload-Updates, es sei denn, Ihr Kursleiter weist Sie dazu an.

#### Übung 2: Verwenden von GitHub Copilot zum Erklären der Codebasis der Bibliotheksanwendung

GitHub Copilot kann Ihnen helfen, eine unbekannte Codebasis zu verstehen, indem Erklärungen auf Projektmappen- und Featureebene generiert werden.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Stellen Sie sicher, dass die AccelerateDevGitHubCopilot-Lösung in Visual Studio Code geöffnet ist.

1. Öffnen Sie die Chatansicht.

    Sie können die Chatansicht auf folgende Weise öffnen:

    - Klicken Sie auf die Schaltfläche **Chat öffnen** (oben im Visual Studio Code-Fenster, direkt rechts neben dem Command Center).
    - Verwenden Sie die Tastenkombination **STRG+ALT+I**.
    - Öffnen Sie das GitHub Copilot-Statusmenü, und wählen Sie dann **GitHub Copilot Chat** aus.

1. Geben Sie eine Eingabeaufforderung ein, bei der der **@workspace** Teilnehmer von GitHub Copilot verwendet wird, um eine Beschreibung des Projekts zu generieren.

    Geben Sie in der Chat-Ansicht beispielsweise den folgenden Prompt ein:

    ```plaintext
    @workspace Describe this project
    ```

    Wenn Sie ein Visual Studio Code-Dialogfeld sehen, in dem steht, dass GitHub Copilot Chat sich mit GitHub anmelden möchte, wählen Sie **Zulassen** aus und schließen Sie dann den Autorisierungsprozess mit Ihrem GitHub-Konto ab.

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot generierte Antwort zu überprüfen.

    Die Antwort sollte der folgenden Beschreibung ähneln:

    ```markdown
    This project is a library management system implemented in C#. It consists of three main components:
    
    1. **Library.ApplicationCore**: This is the core application library containing the main business logic, entities, enums, and interfaces. It includes:
        - Entities such as Book, Patron, Loan, etc.
        - Enums like MembershipRenewalStatus, LoanReturnStatus, and LoanExtensionStatus.
        - Services like LoanService and PatronService.
        - Interfaces like ILoanRepository, IPatronRepository, ILoanService, and IPatronService.
    2. **Library.Console**: This is a console application that interacts with the user. It includes:
        - The main entry point in Program.cs.
        - Configuration settings in appSettings.json.
        - Console interaction logic in ConsoleApp.cs.
    3. **Library.Infrastructure**: This library handles data persistence. It includes:
        - JSON-based repositories like JsonPatronRepository and JsonLoanRepository.
        - Data loading and saving logic in JsonData.

    Additionally, there are unit tests located in the UnitTests directory, which test the functionality of the core services using the NSubstitute mocking framework and xUnit.
    
    The project uses .NET 8.0 and is configured to build and test using GitHub Actions as defined in the build-test.yml file. The solution file is AccelerateDevGitHubCopilot.sln, which includes all the projects and their configurations.
    ```

1. Verwenden Sie die Solution Explorer-Ansicht von Visual Studio Code, um die Projektordner zu erweitern.

1. Öffnen Sie die Datei **ConsoleApp.cs**.

    Die Datei „ConsoleApp.cs“ befindet sich im Projekt „src/Library.Console“.

1. Geben Sie in der Chat-Ansicht eine Eingabeaufforderung ein, die eine Beschreibung der ConsoleApp-Klasse generiert.

    Geben Sie in der Chat-Ansicht beispielsweise den folgenden Prompt ein:

    ```plaintext
    @workspace #editor Describe the ConsoleApp class
    ```

1. Nehmen Sie sich einige Minuten Zeit, um die Antwort zu überprüfen.

    Die Antwort sollte der folgenden Beschreibung ähneln:

    ```markdown
    The ConsoleApp class in ConsoleApp.cs is responsible for managing the console-based user interface of the library management system. It handles user interactions, processes user inputs, and coordinates actions with the underlying services and repositories.

    ### Fields
    - _currentState: Tracks the current state of the console application.
    - matchingPatrons: A list of patrons that match a search query.
    - selectedPatronDetails: Holds details of the currently selected patron.
    - selectedLoanDetails: Holds details of the currently selected loan.
    - _patronRepository: An instance of IPatronRepository for accessing patron data.
    - _loanRepository: An instance of ILoanRepository for accessing loan data.
    - _loanService: An instance of ILoanService for performing loan-related operations.
    - _patronService: An instance of IPatronService for performing patron-related operations.

    ### Constructor
    - ConsoleApp(ILoanService loanService, IPatronService patronService, IPatronRepository patronRepository, ILoanRepository loanRepository): Initializes the ConsoleApp with the provided services and repositories.

    ### Methods
    - Run(): The main entry point for running the console application.
    - PatronSearch(): Handles the logic for searching patrons.
    - ReadPatronName(): Reads the patron's name from the console input.
    - PrintPatronsList(List<Patron> matchingPatrons): Prints a list of matching patrons to the console.
    - PatronSearchResults(): Handles the logic for displaying and selecting from the search results.
    - ReadInputOptions(CommonActions options, out int optionNumber): Reads input options from the console.
    - WriteInputOptions(CommonActions options): Writes the available input options to the console.
    - PatronDetails(): Displays details of the selected patron.
    - LoanDetails(): Displays details of the selected loan and handles actions like extending or returning the loan.

    The class uses a state machine approach to manage different states of the console application, such as searching for patrons, displaying search results, showing patron details, and handling loan details.
    ```

1. Öffnen Sie die Datei **Program.cs**.

1. Geben Sie in der Chat-Ansicht eine Eingabeaufforderung ein, die eine Beschreibung der Datei „Program.cs“ generiert.

    Geben Sie in der Chat-Ansicht beispielsweise den folgenden Prompt ein:

    ```plaintext
    @workspace #editor Describe the Program.cs file
    ```

1. Nehmen Sie sich einige Minuten Zeit, um die Antwort zu überprüfen.

    Die Antwort sollte der folgenden Beschreibung ähneln:

    ```markdown
    The Program.cs file is the entry point for the console application. It sets up the dependency injection container, configures services, and starts the ConsoleApp.
    
    1. **Dependency Injection Setup**:
        - Creates a ServiceCollection to register services.
        - Builds a configuration object from the appSettings.json file.
        - Registers various services and repositories with different lifetimes (singleton, scoped).
    
    2. **Service Registration**:
        - Registers the repositories: JsonPatronRepository and JsonLoanRepository.
        - Registers the services: LoanService and PatronService.
        - Registers the JsonData class as a singleton.
        - Registers the ConsoleApp class as a singleton.
    
    3. **Service Provider**:
        - Builds the service provider from the registered services.
        - Retrieves the ConsoleApp service and runs it asynchronously.

    This setup ensures that all dependencies are properly injected and configured before the application starts running.
    ```

1. Erweitern Sie das Library.Infrastructure-Projekt, und erweitern Sie dann den Dateiordner.

1. Fügen Sie die Dateien **JsonData.cs**, **JsonLoanRepository.cs** und **JsonPatronRepository.cs** zum Chat-Kontext hinzu.

    Sie können die Dateien aus dem Solution Explorer per Drag-and-Drop in die Chat-Ansicht ziehen. Sie können auch die Schaltfläche **Attach-Kontext** (Büroklammer) in der Chat-Ansicht verwenden, um Dateien zum Chat-Kontext hinzuzufügen.

1. Geben Sie einen Prompt in der Chat-Ansicht ein, der eine Erklärung der Datenzugriffsklassen generiert.

    Geben Sie in der Chat-Ansicht beispielsweise den folgenden Prompt ein:

    ```plaintext
    @workspace /explain Explain how the data access classes work
    ```

1. Nehmen Sie sich einige Minuten Zeit, um die Antwort zu überprüfen.

    Die Antwort sollte der folgenden Beschreibung ähneln:

    ```markdown
    The data access classes in this project are designed to handle the loading, saving, and manipulation of data stored in JSON files. These classes include JsonData, JsonPatronRepository, and JsonLoanRepository. Here's an explanation of how each class works:
    
    ### JsonData Class
    The JsonData class is responsible for loading and saving data from and to JSON files. It also provides methods to populate related entities.
    
    #### Key Responsibilities:
    1. **Loading Data**: The LoadData method loads data from JSON files into in-memory collections (Authors, Books, BookItems, Patrons, Loans).
    2. **Saving Data**: The SaveJson method saves data to JSON files. Specific methods like SaveLoans and SavePatrons handle saving loans and patrons, respectively.
    3. **Ensuring Data is Loaded**: The EnsureDataLoaded method ensures that data is loaded into memory before any operations are performed.
    4. **Populating Related Entities**: Methods like GetPopulatedPatron, GetPopulatedLoan, GetPopulatedBookItem, and GetPopulatedBook populate related entities to provide a complete view of the data.
    
    #### Example Methods:
    - **LoadData**: Loads all data from JSON files.
    - **SaveLoans**: Saves loan data to the JSON file.
    - **GetPopulatedPatron**: Populates a patron with related loans.
    - **SearchBookByTitle**: Searches for a book by its title.
    
    ### JsonPatronRepository Class
    The JsonPatronRepository class implements the IPatronRepository interface and provides methods to interact with patron data.

    #### Key Responsibilities:
    1. **Searching Patrons**: The SearchPatrons method searches for patrons by name. 
    2. **Getting a Patron**: The GetPatron method retrieves a patron by ID and populates related data.
    3. **Updating a Patron**: The UpdatePatron method updates patron information and saves it to the JSON file.
    
    #### Example Methods:
    - **SearchPatrons**: Searches for patrons whose names contain the search input.
    - **GetPatron**: Retrieves a patron by ID and populates related loans.
    - **UpdatePatron**: Updates patron information and saves it to the JSON file.
    
    ### JsonLoanRepository Class
    The JsonLoanRepository class implements the ILoanRepository interface and provides methods to interact with loan data.
    
    #### Key Responsibilities:
    1. **Getting a Loan**: The GetLoan method retrieves a loan by ID and populates related data.
    2. **Updating a Loan**: The UpdateLoan method updates loan information and saves it to the JSON file.
    
    #### Example Methods:
    - **GetLoan**: Retrieves a loan by ID and populates related book items and patrons.
    - **UpdateLoan**: Updates loan information and saves it to the JSON file.
    
    ### How They Work Together
    1. **Loading Data**: When the application starts, the JsonData class loads data from JSON files into memory.
    2. **Searching and Retrieving Data**: The JsonPatronRepository and JsonLoanRepository classes use the JsonData class to search and retrieve data. They ensure data is loaded before performing operations.
    3. **Updating Data**: When data is updated, the repository classes call methods on the JsonData class to save the updated data back to the JSON files.
    4. **Populating Related Entities**: The JsonData class provides methods to populate related entities, ensuring that when a patron or loan is retrieved, it includes related data like loans or book items.
    
    ### Example Workflow
    1. **Search for a Patron**:
        - The SearchPatrons method in JsonPatronRepository calls EnsureDataLoaded to ensure data is loaded.
        - It then searches the Patrons collection for matching names and returns the results.

    2. **Get a Loan**:
       - The GetLoan method in JsonLoanRepository calls EnsureDataLoaded to ensure data is loaded.
       - It retrieves the loan by ID and uses GetPopulatedLoan to include related book items and patrons.

    3. **Update a Patron**:
       - The UpdatePatron method in JsonPatronRepository calls EnsureDataLoaded to ensure data is loaded.
       - It updates the patron information and calls SavePatrons to save the updated data to the JSON file.

    By using these data access classes, the application can efficiently manage data stored in JSON files, ensuring that data is loaded, manipulated, and saved correctly.
    ```

1. Nehmen Sie sich ein paar Minuten Zeit, um die JSON-Datendateien zu untersuchen, die zum Simulieren von Bibliotheksdatensätzen verwendet werden.

    Die JSON-Datendateien befinden sich im Ordner „src/Library.Console/Json".

    Die Datendateien verwenden ID-Eigenschaften, um Entitäten zu verknüpfen. Ein Darlehensobjekt hat beispielsweise eine PatronId-Eigenschaft, die mit einem Patron-Objekt mit derselben ID verknüpft ist. Die JSON-Dateien enthalten Daten für Autoren, Bücher, Buchelemente, Kunden und Ausleihen.

    > [!NOTE]
    > Beachten Sie, dass Autorennamen, Buchtitel und Kundennamen für die Zwecke dieses angeleiteten Projekts anonymisiert wurden.

#### Aufgabe 3: Erstellen und Ausführen der Anwendung

Das Ausführen der Anwendung hilft Ihnen, die Benutzeroberfläche, die wichtigsten Features der Anwendung und die Interaktion von App-Komponenten zu verstehen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Stellen Sie sicher, dass die **Projektmappen-Explorer**-Ansicht geöffnet ist.

    Die Projektmappen-Explorer-Ansicht ist nicht identisch mit der Explorer-Ansicht. In der Solution Explorer-Ansicht werden Projekt- und Lösungsdateien als „Verzeichnis“-Knoten verwendet, um die Struktur der Lösung anzuzeigen.

1. Klicken Sie zum Ausführen der Anwendung mit der rechten Maustaste auf **Library.Console**, wählen Sie **Debuggen** aus, und wählen Sie anschließend **Neue Instanz starten** aus.

    Wenn die Optionen **Debuggen** und **Neue Instanz starten** nicht angezeigt werden, stellen Sie sicher, dass Sie die Projektmappen-Explorer-Ansicht und nicht die Explorer-Ansicht verwenden.

    Die folgenden Schritte führen Sie durch einen einfachen Anwendungsfall.

1. Wenn Sie zur Eingabe eines Kundennamens aufgefordert werden, geben Sie **One** ein, und drücken Sie anschließend die EINGABETASTE.

    > [!NOTE]
    > Die Anwendung verwendet einen Suchvorgang, bei dem die Groß-/Kleinschreibung beachtet wird. Sie müssen "Eins" mit dem Großbuchstaben "O" eingeben.

    Daraufhin sollte eine Liste mit Kunden angezeigt werden, die der Suchabfrage entsprechen.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Zahl **2** ein, und drücken Sie anschließend die EINGABETASTE.

    Durch Eingeben von **2** wird der zweite Kunde in der Liste ausgewählt.

    Daraufhin sollten der Name und der Mitgliedschaftsstatus des Kunden angezeigt werden, gefolgt von Details zur Buchausleihe.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Zahl **1** ein, und drücken Sie anschließend die EINGABETASTE.

    Wenn Sie **1** eingeben, wird das erste Buch in der Liste ausgewählt.

    Es sollten Buchdetails aufgeführt sein, einschließlich des Rückgabedatums und des -status.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Option **r** ein, und drücken Sie anschließend die EINGABETASTE.

    Die Eingabe **r** gibt das Buch zurück.

1. Überprüfen Sie, ob die Meldung „Buch wurde erfolgreich zurückgegeben“ angezeigt.

    Die Meldung „Buch wurde erfolgreich zurückgegeben" sollten die Buchdetails folgen. Zurückgegebene Bücher werden mit **Zurückgegeben: Wahr** gekennzeichnet.

1. Um eine neue Suche zu beginnen, geben Sie **s** ein, und drücken Sie dann die EINGABETASTE.

1. Wenn Sie zur Eingabe eines Kundennamens aufgefordert werden, geben Sie **One** ein, und drücken Sie anschließend die EINGABETASTE.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Zahl **2** ein, und drücken Sie anschließend die EINGABETASTE.

1. Überprüfen Sie, ob die erste Buchausleihe als **Zurückgegeben: Wahr** markiert ist.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Option **q** ein, und drücken Sie anschließend die EINGABETASTE.

1. Beenden Sie die Debugsitzung.

#### Zusammenfassung - der Übung 2

Diese Übung hat Ihnen geholfen, die Codebasis der Bibliotheksanwendung und die Interaktion der Anwendung mit dem Benutzer zu verstehen. Sie haben GitHub Copilot verwendet, um Erklärungen für die Projektstruktur, ausgewählte Dateien und Datenzugriffsklassen zu generieren. Sie haben die Anwendung auch ausgeführt, um zu sehen, wie die Konsolenschnittstelle funktioniert und wie die Anwendungskomponenten interagieren.

### Übung 3: Erstellen des GitHub-Repositorys und leeren der README-Datei

Wenn Sie das GitHub-Repository für Ihren Code erstellen, können Sie Ihre Arbeit mit anderen teilen und am Projekt zusammenarbeiten.

#### Aufgabe 1: GitHub-Repository erstellen

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Stellen Sie sicher, dass Ihr GitHub-Konto in einem Browserfenster geöffnet ist.

    Öffnen Sie bei Bedarf ein Browserfenster, und verwenden Sie die folgenden Informationen, um sich anzumelden:

    URL: `https://github.com/enterprises/Microsoft-APL/sso`

    E-Mail/Benutzername: `@lab.CloudPortalCredential(1).Username`

    Kennwort: `@lab.CloudPortalCredential(1).Password`

1. Öffnen Sie Ihr GitHub-Kontomenü, und wählen Sie dann **Ihre Repositorys** aus.

    Es sollte eine Meldung angezeigt werden, die angibt, dass Sie noch keine Repositorys haben.

1. Um Git-Konfigurationsbefehle zu erstellen, die Ihre GitHub-Kontodaten verwenden, öffnen Sie **Notepad** und erstellen Sie dann die folgenden Git-Befehle:

    ```bash
    git config --global user.email "lab assigned email"
    git config --global user.name "user name"
    ```

    Ersetzen Sie **lab assigned email** durch die in der Übungsumgebung definierte E-Mail `@lab.CloudPortalCredential(1).Username`

    Ersetzen Sie **Benutzername** durch Ihren eigenen Namen.

1. Wechseln Sie zum Visual Studio Code-Fenster.

1. Öffnen Sie das integrierte Terminal in Visual Studio Code.

    Wählen Sie im Menü „Terminal“ **Neues Terminal** aus.

1. Um Git mit den Anmeldedaten Ihres GitHub-Kontos zu konfigurieren, geben Sie die beiden Befehle ein, die Sie in Notepad erstellt haben.

1. Öffnen Sie in Visual Studio Code die Ansicht „Quellcodeverwaltung“.

1. Wählen Sie **Publish to GitHub** (Auf GitHub veröffentlichen) aus.

    Wenn ein Dialogfeld geöffnet wird, in dem Sie aufgefordert werden, sich mit Ihrem GitHub-Konto anzumelden, führen Sie die folgenden Schritte aus:

    1. Klicken Sie auf **Zulassen**.
    1. Wählen Sie das Konto aus, das Sie in dieser Übungsumgebung verwenden.
    1. Wählen Sie bei Bedarf erneut **Auf GitHub veröffentlichen** aus.

1. Akzeptieren Sie den Standardnamen für das Repository (AccelerateDevGitHubCopilot) und klicken Sie auf **Im privaten GitHub-Repository veröffentlichen**.

    Beachten Sie, dass Visual Studio Code während des Veröffentlichungsprozesses Statusmeldungen anzeigt.

    Möglicherweise werden Sie aufgefordert, Ihr GitHub-Konto erneut zu autorisieren. Wenn ja, folgen Sie den Anweisungen auf dem Bildschirm, um Ihr Konto im Browser zu autorisieren. Dies kann dazu führen, dass Ihr Repository mit der „first commit“-Übertragungsnachricht veröffentlicht wird.

1. Wenn der Code nicht im Repository veröffentlicht wurde und Sie zur Ansicht „Source Control“ zurückkehren, geben Sie eine Commit-Nachricht ein und wählen Sie dann **Branch veröffentlichen** aus.

    Nach Abschluss des Veröffentlichungsprozesses wird eine Meldung angezeigt, dass Ihr Code erfolgreich im von Ihnen angegebenen GitHub-Repository veröffentlicht wurde.

#### Aufgabe 2: Erstellen einer leeren README-Datei in GitHub

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Wechseln Sie zum Browserfenster mit Ihrem GitHub-Konto.

1. Öffnen Sie das neue AccelerateDevGitHubCopilot-Repository in Ihrem GitHub-Konto.

    Wenn Ihr AccelerateDevGitHubCopilot-Repository nicht angezeigt wird, aktualisieren Sie die Seite. Wenn das Repository immer noch nicht angezeigt wird, führen Sie die folgenden Schritte durch:

    1. Wechseln Sie zu Visual Studio Code.
    1. Öffnen Sie Ihre Benachrichtigungen. Beim Veröffentlichen des neuen Repositorys wurde eine Benachrichtigung generiert.
    1. Wählen Sie **Auf GitHub öffnen** aus, um Ihr Repository zu öffnen.

1. Wählen Sie auf der Registerkarte „Code“ des Repositorys „AccelerateDevGitHubCopilot“ **Infodatei hinzufügen** aus.

1. Geben Sie im Infodatei-Editor **In Kürze verfügbar** ein, und wählen Sie dann **Änderungen committen** aus.

1. Wählen Sie im Dialogfeld „Änderungen übernehmen“ die Option „**Änderungen übernehmen**“ aus.

#### Aufgabe 3: Übertragen Sie die Änderungen in Ihr lokales Repository.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Wechseln Sie zu Visual Studio Code, und stellen Sie sicher, dass die Ansicht „Quellcodeverwaltung“ geöffnet ist.

1. Öffnen Sie das Menü **Weitere Aktionen** und wählen Sie dann **Übertragen** aus.

    Das Menü „Weitere Aktionen“ kann über die Ellipse in der oberen rechten Ecke der Ansicht „Source Control“ geöffnet werden.

1. Öffnen Sie die EXPLORER-Ansicht (klappen Sie den SOLUTION EXPLORER zu und verwenden Sie den Standard-Datei-/Ordner-Explorer von Visual Studio Code) und erweitern Sie dann den Ordner **AccelerateDevGitHubCopilot**.

1. Öffnen Sie die Infodatei.

    Die Meldung „In Kürze verfügbar“ sollte angezeigt werden.

    > [!NOTE]
    > Sie hätten den Inhalt der README-Datei direkt in Visual Studio Code erstellen und die Aktualisierungen dann in das GitHub-Repository hochladen können.

In der nächsten Übung werden Sie die README-Datei Ihres Repositorys mit GitHub Copilot Chat aktualisieren.

#### Zusammenfassung - der Übung 3

In dieser Übung haben Sie geholfen, ein GitHub-Repository für die Bibliotheksanwendung und eine leere README-Datei zu erstellen. Außerdem haben Sie die Änderungen an Ihrem lokalen Repository abgerufen, um sicherzustellen, dass Sie über die neuesten Updates verfügen.

### Übung 4: Erstellen Sie die Projektdokumentation für die README-Datei

Die Infodatei ist ein wesentlicher Bestandteil aller GitHub-Repositorys. Die Infodatei stellt Informationen basierend auf den Anforderungen des Projekts, der Projektmitwirkenden und der Projektbeteiligten bereit.

Bei dieser angeleiteten Projektübung sollte Ihre Infodatei die folgenden Abschnitte enthalten:

- **Projekttitel:** Ein kurzer, klarer Titel für das Projekt.
- **Beschreibung:** Eine detaillierte Erläuterung, worum es sich bei dem Projekt handelt und wofür es verwendet wird.
- **Projektstruktur**: Eine Aufschlüsselung der Projektstruktur einschließlich der wichtigen Ordner und Dateien
- **Wichtige Klassen und Schnittstellen**: Eine Liste der wichtigsten Klassen und Schnittstellen im Projekt
- **Verwendung:** Anleitung zur Verwendung des Projekts (häufig mit Codebeispielen).
- **Lizenz:** Die Lizenz für das Projekt.

#### Aufgabe 1: Verwenden von GitHub Copilot zum Generieren der Projektdokumentation.

In diesem Übungsabschnitt erstellen Sie mithilfe von GitHub Copilot eine Projektdokumentation und fügen diese Ihrer Datei README.md hinzu.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Chatansicht.

    Wenn Sie an bestimmten Codes oder Dateien interessiert sind, können Sie diese per Drag-and-Drop dem Chatansichtskontext hinzuzufügen. In diesem Fall sind Sie an der Gesamtlösung interessiert, sodass Sie den `@workspace` Teilnehmer verwenden, anstatt einzelne Dateien hinzuzufügen.

1. Um die Projektdokumentation für Ihre Infodatei zu generieren, geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace Generate the contents of a README.md file for the code repository. Use "Library App" as the project title. The README file should include the following sections: Description, Project Structure, Key Classes and Interfaces, Usage, License. Format all sections as raw markdown. Use a bullet list with indents to represent the project structure. Do not include ".gitignore" or the ".github", "bin", and "obj" folders.
    ```

    > [!NOTE]
    > Wenn Sie mehrere Eingabeaufforderungen verwenden, würde eine pro Abschnitt der Infodatei detailliertere Ergebnisse liefern. In dieser Übung wird ein einziger Prompt verwendet, um den Prozess zu vereinfachen.

1. Überprüfen Sie die Antwort, um sicherzustellen, dass jeder Abschnitt als Markdown formatiert ist.

    > [!NOTE]
    > Sie können die Readme-Abschnitte einzeln aktualisieren, um detailliertere Informationen bereitzustellen oder für den Fall, dass sie nicht richtig formatiert sind. Sie können auch die Antwort von GitHub Copilot in die Infodatei kopieren und dann direkt in der Markdowndatei Korrekturen vornehmen.

1. Öffnen Sie bei geöffneter Markdown-Datei im Editor das Statusmenü von GitHub Copilot und wählen Sie dann **Vervollständigungen für Markdown aktivieren** aus.

1. Kopieren Sie die vorgeschlagenen Dokumentationsabschnitte in die Infodatei.

    GitHub Copilot kann Vorschläge für die Markdown-Dokumentation generieren. Dieses Feature kann Ihnen beim Verfassen und Formatieren von Markdowndateien helfen.

    Sie können z. B. den Inhalt der README.md-Datei auswählen, den Inlinechat öffnen und dann GitHub Copilot bitten, "die Formatierung der Markdown-Dokumentation zu korrigieren".

1. Passen Sie die Formatierung bei Bedarf an, und speichern Sie dann die aktualisierte README.md Datei.

    Sie sollten über eine README-Datei verfügen, die den Projekttitel, die Beschreibung, die Projektstruktur, wichtige Klassen und Schnittstellen, Verwendungsanweisungen und Lizenzinformationen enthält.

    ```markdown
    # Library App
    
    ## Description
    Library App is a console-based application for managing library operations such as patron management, book loans, and membership renewals. It uses a JSON-based data storage system and provides various services to handle library functionalities.
    
    ## Project Structure
    - AccelerateDevGitHubCopilot.sln
    - README.md
    - src
      - Library.ApplicationCore/
        - Entities/
          - `Author.cs`
          - `Book.cs`
          - `BookItem.cs`
          - `Loan.cs`
          - `Patron.cs`
        - Enums/
          - `LoanExtensionStatus.cs`
          - `LoanReturnStatus.cs`
          - `MembershipRenewalStatus.cs`
        - Interfaces/
          - `IPatronRepository.cs`
          - `IPatronService.cs`
          - `ILoanRepository.cs`
          - `ILoanService.cs`
        - `Library.ApplicationCore.csproj`
        - Services/
          - `PatronService.cs`
          - `LoanService.cs`
      - Library.Console/
        - `appSettings.json`
        - `CommonActions.cs`
        - `ConsoleApp.cs`
        - `ConsoleState.cs`
        - `Library.Console.csproj`
        - `Program.cs`
      - Library.Infrastructure/
        - Data/
          - `JsonData.cs`
          - `JsonLoanRepository.cs`
          - `JsonPatronRepository.cs`
        - `Library.Infrastructure.csproj`
    - tests
      - UnitTests/
        - ApplicationCore/
          - LoanService/
            - `ReturnLoan.cs`
            - `ExtendLoan.cs`
          - PatronService/
            - `RenewMembership.cs`
        - `UnitTests.csproj`
    
    ## Key Classes and Interfaces
    - **Entities**
      - **Author**: Represents an author with properties like Id and Name.
      - **Book**: Represents a book with properties like Id, Title, AuthorId, Genre, ImageName, and ISBN.
      - **BookItem**: Represents a specific copy of a book with properties like Id, BookId, AcquisitionDate, and Condition.
      - **Loan**: Represents a loan with properties like Id, BookItemId, PatronId, LoanDate, DueDate, and ReturnDate.
      - **Patron**: Represents a library patron with properties like Id, Name, MembershipStart, MembershipEnd, and Loans.
    
    - **Enums**
      - **LoanExtensionStatus**: Enum for loan extension statuses.
      - **LoanReturnStatus**: Enum for loan return statuses.
      - **MembershipRenewalStatus**: Enum for membership renewal statuses.
    
    - **Interfaces**
      - **IPatronRepository**: Interface for patron repository with methods like GetPatron, SearchPatrons, and UpdatePatron.
      - **IPatronService**: Interface for patron service with method RenewMembership.
      - **ILoanRepository**: Interface for loan repository with methods like GetLoan and UpdateLoan.
      - **ILoanService**: Interface for loan service with methods like ReturnLoan and ExtendLoan.
    
    - **Services**
      - **PatronService**: Implements IPatronService to handle patron-related operations.
      - **LoanService**: Implements ILoanService to handle loan-related operations.
    
    - **Console**
      - **ConsoleApp**: Main console application class that handles user interactions and application flow.
      - **ConsoleState**: Enum for different states of the console application.
      - **CommonActions**: Enum for common actions in the console application.
    
    - **Infrastructure**
      - **JsonData**: Handles loading and saving data to JSON files.
      - **JsonLoanRepository**: Implements ILoanRepository to manage loan data.
      - **JsonPatronRepository**: Implements IPatronRepository to manage patron data.
    
    ## Usage
    1. Clone the repository.
    2. Open the solution file AccelerateDevGitHubCopilot.sln in Visual Studio.
    3. Build the solution to restore dependencies.
    4. Run the Library.Console project to start the console application.
    5. Follow the on-screen instructions to search for patrons, view patron details, extend loans, return books, and renew memberships.
    
    ## License
    This project is licensed under the MIT License.
    ```

#### Aufgabe 2: Veröffentlichen und verbreiten Sie die Aktualisierungen der README-Datei

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Ansicht „Versionsverwaltung“ von Visual Studio Code.

1. Damit GitHub Copilot eine Commitnachricht generiert, wählen Sie das Symbol auf der rechten Seite des Meldungsfelds aus.

    Es wird eine Commitmeldung ähnlich der folgenden angezeigt:

    ```plaintext
    Update README.md with project description, structure, key classes, usage instructions, and license information
    ```

1. Stellen Sie die Dateiaktualisierungen bereit, und führen Sie einen Commit dafür durch.

1. Synchronisieren oder pushen Sie Ihre Updates an das GitHub-Repository.

    Autorisieren Sie den Synchronisierungs-/Push-Vorgang mit Ihren GitHub-Anmeldedaten, wenn Sie dazu aufgefordert werden.

#### Aufgabe 3: Überprüfen Ihrer Arbeit

Führen Sie die folgenden Schritte aus, um Ihre Arbeit zu überprüfen:

1. Öffnen Sie das GitHub-Repository für das AccelerateDevGitHubCopilot-Projekt.

1. Verwenden Sie die Registerkarte **Code**, um die aktualisierte Infodatei zu überprüfen.

    Möglicherweise müssen Sie den Browser aktualisieren, um die aktualisierte README-Datei zu sehen.

1. Stellen Sie sicher, dass die in der Infodatei beschriebene Projektstruktur mit der Ordnerstruktur des Repositorys übereinstimmt.

    Während der Vorschau der README-Datei können Sie die Dateistruktur auf der linken Seite der GitHub-Schnittstelle verwenden, um die Repositorystruktur zu erweitern und zu überprüfen.

1. Überprüfen Sie den Commitverlauf, und suchen Sie die von GitHub Copilot generierte Commitmeldung.

#### Zusammenfassung - der Übung 4

Diese Übung half Ihnen beim Erstellen der Projektdokumentation für die README-Datei mit GitHub Copilot. Sie haben GitHub Copilot verwendet, um die Projektbeschreibung, Projektstruktur, wichtige Klassen und Schnittstellen, Nutzungsanweisungen und Lizenzinformationen zu generieren. Sie haben auch die Aktualisierungen der README-Datei in das GitHub-Repository übertragen.

## Teil 2: Entwickeln Sie Codefeatures mithilfe von GitHub Copilot-Tools

### Vor der Installation

#### Projektübersicht

Sie und Ihre Kollegen treffen sich, um Ihre Ziele für die Bibliotheksanwendung zu besprechen. Sie möchten die Benutzererfahrung für die Bibliothekare und Kunden verbessern. Sie besprechen mehrere neue Features, die der Anwendung hinzugefügt werden könnten.

Sie verständigen sich darauf, an folgenden Features zu arbeiten:

- Buchverfügbarkeit: Ermöglicht es Bibliothekaren, den Verfügbarkeitsstatus eines Buchs zu bestimmen. Dieses Feature soll eine Nachricht anzeigen, die Aufschluss darüber gibt, ob ein Buch ausgeliehen werden kann. Ist das Buch aktuell an einen anderen Kunden ausgeliehen, soll das Rückgabedatum angezeigt werden.

- Buchausleihe: Ermöglicht es Bibliothekaren, ein Buch an einen Kunden auszuleihen (sofern das Buch verfügbar ist). Dieses Feature soll eine Buchausleihoption für einen Kunden anzeigen, „Loans.json“ mit der neuen Ausleihe aktualisieren und die aktualisierten Ausleihdetails für den Kunden anzeigen.

- Buchreservierungen: Ermöglicht es Bibliothekaren, ein Buch für einen Kunden zu reservieren (es sei denn, das Buch ist bereits reserviert). Dieses Feature soll einen neuen Buchreservierungsprozess implementieren. Für dieses Feature müssen unter Umständen eine neue Datei namens „Reservations.json“ sowie neue Klassen und Schnittstellen erstellt werden, die zur Unterstützung des Reservierungsprozesses erforderlich sind.

Alle arbeiten jeweils an einem der neuen Features und kommen anschließend wieder zusammen. Sie werden an der Funktion arbeiten, um den Verfügbarkeitsstatus eines Buches zu ermitteln. Ihr Kollege arbeitet an dem Feature, das es ermöglicht, ein Buch an einen Kunden auszuleihen. Das letzte Feature (also die Buchreservierung für einen Kunden) wird entwickelt, nachdem die beiden anderen Features fertig sind.

#### Übungsszenario (Teil 2)

GitHub Copilot kann Ihnen beim Entwickeln neuer Funktionen für die Bibliotheksanwendung helfen.

In Teil 2 dieser Übung verwenden Sie GitHub Copilot, um Codevorschläge zu generieren, mit denen Sie die neuen Funktionen schneller und genauer implementieren können.

Teil 2 umfasst die folgenden Übungen:

- Entwickeln eines neuen Buchverfügbarkeitsfeatures
- Führen Sie Ihre Änderungen im Mainbranch des Repositorys zusammen.

### Übung 5: Entwickeln Sie eine neue Funktion zur „Verfügbarkeit von Büchern“

Das Buchverfügbarkeitsfeature muss folgende Codeaktualisierungen umfassen:

- Implementieren Sie eine neue CommonActions.SearchBooks-Aktion, mit der ein Bibliothekar die Option zum Suchen nach einem Buch auswählen kann.
- Erstellen Sie eine neue SearchBooks-Methode in ConsoleApp.cs. Die SearchBooks-Methode sollte einen von Benutzenden bereitgestellten Buchtitel lesen. Überprüfen Sie, ob ein Buch zum Ausleihen verfügbar ist, und zeigen Sie eine Meldung an, die besagt, dass „Buch.Titel zum Ausleihen verfügbar ist“ oder „Buch.Titel an eine andere Benutzerin bzw. einen anderen Benutzer ausgeliehen ist“. Das Rückgabedatum ist „loan.DueDate“.

In dieser Übung werden Sie die folgenden Aufgaben ausführen:

- Erstellen Sie einen Zweig „Buchverfügbarkeit“ in Ihrem Code-Repository.
- Verwenden Sie GitHub Copilot-Vorschläge, um eine neue allgemeine SearchBooks-Aktion zu implementieren, die von einem Bibliothekar ausgewählt werden kann.
- Verwenden Sie GitHub Copilot-Vorschläge, um die SearchBooks-Methode zu entwickeln, die einen von Benutzenden bereitgestellten Buchtitel liest, überprüft, ob ein Buch für die Ausleihe verfügbar ist, und eine Meldung anzeigt, die den Verfügbarkeitsstatus des Buchs angibt.

#### Aufgabe 1: Erstellen Sie einen neuen Zweiges im Repository

Bevor Sie mit der Entwicklung des neuen Buchverfügbarkeitsfeatures beginnen, müssen Sie einen neuen Branch im Repository erstellen. Dadurch können Sie an dem neuen Feature arbeiten, ohne dass sich dies auf den Mainbranch des Repositorys auswirkt. Wenn das neue Feature bereit ist, können Sie es im Mainbranch mergen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Stellen Sie sicher, dass die AccelerateDevGitHubCopilot-Lösung in Visual Studio Code geöffnet ist.

1. Wählen Sie die Ansicht „Quellcodeverwaltung“ aus, und stellen Sie sicher, dass das lokale Repository mit dem Remoterepository synchronisiert wird (Pullen oder Synchronisieren).

1. Wählen Sie links unten im Fenster die Option **main** aus.

1. Um einen neuen Zweig zu erstellen, geben Sie **Buchverfügbarkeit** ein und wählen Sie dann **+ Neuen Zweig erstellen**.

1. Wählen Sie **Branch veröffentlichen** aus, Um den neuen Branch in das Remoterepository zu pushen.

#### Aufgabe 2: Implementieren einer neuen allgemeinen Aktion "SearchBooks"

In diesem Abschnitt der Übung verwenden Sie GitHub Copilot, mit dessen Hilfe Sie eine Menüoption namens „SearchBooks“ implementieren. Bibliothekare wählen die SearchBooks-Aktion aus, um den Verfügbarkeitsstatus eines Buchs zu überprüfen.

Hier sind die Dateiaktualisierungen, die Sie während dieser Aufgabe abgeschlossen haben:

- Aktualisieren Sie CommonActions Enumeration in CommonActions.cs: Fügen Sie eine neue SearchBooks-Aktion zu CommonActions Enumeration hinzu.
- Aktualisieren Sie die WriteInputOptions-Methode in ConsoleApp.cs: Fügen Sie Unterstützung für die Anzeige der neuen Option CommonActions.SearchBooks hinzu.
- Aktualisieren Sie die ReadInputOptions-Methode in ConsoleApp.cs: Fügen Sie Unterstützung für das Lesen (Auswählen) der neuen Option CommonActions.SearchBooks hinzu.
- Aktualisieren Sie die PatronDetails-Methode in ConsoleApp.cs: Fügen Sie Unterstützung für die Verarbeitung der neuen Option CommonActions.SearchBooks hinzu, wenn sie ausgewählt ist.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Ansicht „PROJEKTMAPPEN-EXPLORER“.

1. Öffnen Sie die Datei „CommonActions.cs“ und wählen Sie dann die **CommonActions**-Enumeration aus.

    Sie müssen eine neue SearchBooks-Aktion zu CommonActions hinzufügen.

1. Öffnen Sie den Inlinechat, und geben Sie folgenden Prompt ein:

    ```plaintext
    Update selection to include a new `SearchBooks` action.
    ```

    GitHub Copilot sollte eine Codeaktualisierung vorschlagen, die die neue SearchBooks-Aktion zur CommonActions-Enumeration hinzufügt.

1. Überprüfen Sie die vorgeschlagene Aktualisierung, und wählen Sie anschließend **Annehmen** aus.

    ```csharp

    public enum CommonActions
    {
        Repeat = 0,
        Select = 1,
        Quit = 2,
        SearchPatrons = 4,
        RenewPatronMembership = 8,
        ReturnLoanedBook = 16,
        ExtendLoanedBook = 32,
        SearchBooks = 64
    }

    ```

1. Öffnen Sie die Datei „ConsoleApp.cs“.

1. Suchen Sie die **WriteInputOptions**-Methode und wählen Sie diese aus.

    Sie müssen Unterstützung für die neue Option "CommonActions.SearchBooks" hinzufügen. Zeigen Sie die Option an, um zu überprüfen, ob ein Buch zum Ausleihen verfügbar ist.

1. Öffnen Sie den Inlinechat, und geben Sie folgenden Prompt ein:

    ```plaintext
    Update selection to include an option for the `CommonActions.SearchBooks` action. Use the letter "b" and the message "to check for book availability".
    ```

    GitHub Copilot sollte ein Code-Update vorschlagen, das einen neuen „Falls“-Block für die Aktion „SearchBooks“ hinzufügt.

1. Überprüfen Sie die vorgeschlagene Aktualisierung, und wählen Sie anschließend **Annehmen** aus.

    Die vorgeschlagene Aktualisierung sollte in etwa wie der folgende Codeschnipsel aussehen:

    ```csharp

    static void WriteInputOptions(CommonActions options)
    {
        Console.WriteLine("Input Options:");
        if (options.HasFlag(CommonActions.ReturnLoanedBook))
        {
            Console.WriteLine(" - \"r\" to mark as returned");
        }
        if (options.HasFlag(CommonActions.ExtendLoanedBook))
        {
            Console.WriteLine(" - \"e\" to extend the book loan");
        }
        if (options.HasFlag(CommonActions.RenewPatronMembership))
        {
            Console.WriteLine(" - \"m\" to extend patron's membership");
        }
        if (options.HasFlag(CommonActions.SearchPatrons))
        {
            Console.WriteLine(" - \"s\" for new search");
        }
        if (options.HasFlag(CommonActions.SearchBooks))
        {
            Console.WriteLine(" - \"b\" to check for book availability");
        }
        if (options.HasFlag(CommonActions.Quit))
        {
            Console.WriteLine(" - \"q\" to quit");
        }
        if (options.HasFlag(CommonActions.Select))
        {
            Console.WriteLine("Or type a number to select a list item.");
        }
    }

    ```

1. Scrollen Sie etwas nach oben, um die **ReadInputOptions**-Methode zu finden.

1. Wählen Sie die **ReadInputOptions**-Methode aus.

    Sie müssen Unterstützung für die neue Option "CommonActions.SearchBooks" hinzufügen. Schließen Sie einen Fall ein, der das Auswählen der SearchBooks-Aktion durch Benutzende behandelt.

1. Öffnen Sie den Inlinechat, und geben Sie folgenden Prompt ein:

    ```plaintext
    Update selection to include an option for the `CommonActions.SearchBooks` action.
    ```

    GitHub Copilot sollte ein Code-Update vorschlagen, das einen neuen „Fall“ hinzufügt, der die Auswahl der Aktion „SearchBooks“ durch Benutzende behandelt.

1. Überprüfen Sie die vorgeschlagene Aktualisierung, und wählen Sie anschließend **Annehmen** aus.

    Die vorgeschlagene Aktualisierung sollte in etwa wie der folgende Codeschnipsel aussehen:

    ```csharp

    static CommonActions ReadInputOptions(CommonActions options, out int optionNumber)
    {
        CommonActions action;
        optionNumber = 0;
        do
        {
            Console.WriteLine();
            WriteInputOptions(options);
            string? userInput = Console.ReadLine();
            action = userInput switch
            {
                "q" when options.HasFlag(CommonActions.Quit) => CommonActions.Quit,
                "s" when options.HasFlag(CommonActions.SearchPatrons) => CommonActions.SearchPatrons,
                "m" when options.HasFlag(CommonActions.RenewPatronMembership) => CommonActions.RenewPatronMembership,
                "e" when options.HasFlag(CommonActions.ExtendLoanedBook) => CommonActions.ExtendLoanedBook,
                "r" when options.HasFlag(CommonActions.ReturnLoanedBook) => CommonActions.ReturnLoanedBook,
                "b" when options.HasFlag(CommonActions.SearchBooks) => CommonActions.SearchBooks,
                _ when int.TryParse(userInput, out optionNumber) => CommonActions.Select,
                _ => CommonActions.Repeat
            };
            if (action == CommonActions.Repeat)
            {
                Console.WriteLine("Invalid input. Please try again.");
            }
        } while (action == CommonActions.Repeat);
        return action;
    }

    ```

1. Scrollen Sie nach unten, um die Methode **PatronDetails** zu finden und auszuwählen.

    Hier sind zwei Aktionen erforderlich:

    - Sie müssen CommonActions.SearchBooks zu den Optionen hinzufügen, bevor Sie ReadInputOptions aufrufen.
    - Sie müssen auch ein „anderes falls“ hinzufügen, um die SearchBooks-Aktion zu verarbeiten. Der „anderes, falls"-Block sollte eine neue Methode namens SearchBooks aufrufen.

    Sie können beides zusammen implementieren.

1. Öffnen Sie den Inlinechat, und geben Sie folgenden Prompt ein:

    ```plaintext
    Update selection to add `CommonActions.SearchBooks` to `options` before calling `ReadInputOptions`. Add an `else if` block to handle the `SearchBooks` action. The `else if` block should call a new method named `SearchBooks`.
    ```

    GitHub Copilot sollte ein Codeupdate vorschlagen, das CommonActions.SearchBooks zu den Optionen hinzufügt, bevor ReadInputOptions aufgerufen wird.

1. Überprüfen Sie die vorgeschlagene Aktualisierung, und wählen Sie anschließend **Annehmen** aus.

    ```csharp

    async Task<ConsoleState> PatronDetails()
    {
        Console.WriteLine($"Name: {selectedPatronDetails.Name}");
        Console.WriteLine($"Membership Expiration: {selectedPatronDetails.MembershipEnd}");
        Console.WriteLine();
        Console.WriteLine("Book Loans:");
        int loanNumber = 1;
        foreach (Loan loan in selectedPatronDetails.Loans)
        {
            Console.WriteLine($"{loanNumber}) {loan.BookItem!.Book!.Title} - Due: {loan.DueDate} - Returned: {(loan.ReturnDate != null).ToString()}");
            loanNumber++;
        }
        CommonActions options = CommonActions.SearchPatrons | CommonActions.Quit | CommonActions.Select | CommonActions.RenewPatronMembership | CommonActions.SearchBooks;
        CommonActions action = ReadInputOptions(options, out int selectedLoanNumber);
        if (action == CommonActions.Select)
        {
            if (selectedLoanNumber >= 1 && selectedLoanNumber <= selectedPatronDetails.Loans.Count())
            {
                var selectedLoan = selectedPatronDetails.Loans.ElementAt(selectedLoanNumber - 1);
                selectedLoanDetails = selectedPatronDetails.Loans.Where(l => l.Id == selectedLoan.Id).Single();
                return ConsoleState.LoanDetails;
            }
            else
            {
                Console.WriteLine("Invalid book loan number. Please try again.");
                return ConsoleState.PatronDetails;
            }
        }
        else if (action == CommonActions.Quit)
        {
            return ConsoleState.Quit;
        }
        else if (action == CommonActions.SearchPatrons)
        {
            return ConsoleState.PatronSearch;
        }
        else if (action == CommonActions.RenewPatronMembership)
        {
            var status = await _patronService.RenewMembership(selectedPatronDetails.Id);
            Console.WriteLine(EnumHelper.GetDescription(status));
            // reloading after renewing membership
            selectedPatronDetails = (await _patronRepository.GetPatron(selectedPatronDetails.Id))!;
            return ConsoleState.PatronDetails;
        }
        else if (action == CommonActions.SearchBooks)
        {
            return await SearchBooks();
        }
        throw new InvalidOperationException("An input option is not handled.");
    }

    ```

    > [!NOTE]
    > Inline-Chat-Vorschläge können auch Stub-Code für die SearchBooks-Methode erstellen.

#### Aufgabe 3: Entwickeln der SearchBooks-Methode

Nach Abschluss sollte die SearchBooks-Methode einen von Benutzenden bereitgestellten Buchtitel lesen, überprüfen, ob ein Buch für die Ausleihe verfügbar ist, und eine Meldung anzeigen, die den Verfügbarkeitsstatus des Buchs angibt. Die Methode sollte die Dateien Books.json und Loans.json verwenden, um den passenden Buchtitel zu finden und den Verfügbarkeitsstatus des Buchs zu bestimmen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Nehmen Sie sich kurz Zeit, um sich Gedanken über die Prozessanforderungen für die SearchBooks-Methode zu machen.

    Wozu dient die Methode? Was soll sie zurückgeben? Benötigt sie Parameter?

    Die SearchBooks-Methode sollte den folgenden Prozess implementieren:

    1. Auffordern des Benutzers zur Eingabe eines Buchtitels
    1. Lesen des vom Benutzer angegebenen Buchtitels
    1. Überprüfen, ob ein Buch zum Ausleihen verfügbar ist
    1. Anzeigen einer Nachricht mit einer der folgenden Aussagen:

        - „Buchtitel ist für die Ausleihe verfügbar"
        - „Buchtitel wurde von einem anderen Kunden ausgeliehen". Das Rückgabedatum ist „loan.DueDate“.

    Um die Nachrichtenoptionen zu erstellen, muss Ihr Code auf die folgenden JSON-Dateien zugreifen:

    - Books.json ist erforderlich, um den übereinstimmenden Titel und die BookId zu finden.
    - Loans.json ist erforderlich, um das ReturnDate und DueDate für die entsprechende BookItemId zu finden. Die BookItemId ist identisch mit der BookId in Books.json.

1. Stellen Sie sicher, dass Sie die folgende **SearchBooks**-Methode in der Datei ConsoleApp.cs erstellt haben:

    ```csharp

    async Task<ConsoleState> SearchBooks()
    {
        return ConsoleState.PatronDetails;
    }

    ```

    > [!NOTE]
    > Entfernen Sie unbedingt alle ggf. von GitHub Copilot erstellten Codekommentare. Unnötige und ungenaue Kommentare können die Vorschläge von GitHub Copilot negativ beeinflussen.

1. Wählen Sie die **SearchBooks**-Methode aus.

1. Öffnen Sie den Inlinechat, und geben Sie folgenden Prompt ein:

    ```plaintext
    Update selection to obtain a book title. Prompt the user to "Enter a book title to search for". Read the user input and ensure the book title isn't null.
    ```

    GitHub Copilot sollte eine Codeaktualisierung vorschlagen, die den vom Benutzer angegebenen Buchtitel erfasst.

1. Überprüfen Sie die vorgeschlagene Aktualisierung, und wählen Sie anschließend **Annehmen** aus.

    ```csharp

    async Task<ConsoleState> SearchBooks()
    {
        string? bookTitle = null;
        while (String.IsNullOrWhiteSpace(bookTitle))
        {
            Console.Write("Enter a book title to search for: ");
            bookTitle = Console.ReadLine();
        }
        // Perform book search logic here
        return ConsoleState.PatronDetails;
    }

    ```

    > [!NOTE]
    > GitHub Copilot kann eine separate Methode erstellen, um die Benutzereingabe eines Buchtitels zu verarbeiten. Sie können diesen Vorschlag akzeptieren und die primäre Logik in der SearchBooks-Methode weiter entwickeln.

1. Löschen Sie alle von GitHub Copilot generierten Platzhalterkommentare, und wählen Sie dann die **SearchBooks**-Methode aus.

1. Öffnen Sie die Chatansicht.

1. Fügen Sie die folgenden Dateien zum Chatkontext hinzu: ConsoleApp.cs, JsonData.cs, JsonLoanRepository.cs, Books.json, Loans.json, BookItems.json, .

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace  Explain how to update the `SearchBooks` method and ConsoleApps class to determine whether a book title is available for loan. Inside the SearchBooks method, use a LINQ query and the user supplied book title to return a matching book. If a book is found, use a LINQ query and Loans.json to check if the book is available for loan. If the book has been returned, display a message stating "`book.title` is available for loan". If the book is on loan, display a message stating "`book.title` is on loan to another patron. The return due date is `loan.DueDate`".
    ```

1. Nehmen Sie sich einen Moment Zeit, um die vorgeschlagenen Aktualisierungen zu überprüfen.

    GitHub Copilot sollte Updates vorschlagen, die den folgenden Vorschlägen ähneln:

    Um die SearchBooks-Methode und die ConsoleApp-Klasse zu aktualisieren und festzustellen, ob ein Buchtitel zur Ausleihe verfügbar ist, gehen Sie wie folgt vor:

    a. Fügen Sie eine Methode hinzu, um nach Büchern nach Titel in der JsonData-Klasse zu suchen.
    b. Aktualisieren Sie die SearchBooks-Methode in der ConsoleApp-Klasse, um diese neue Methode zu verwenden.
    c. Überprüfen Sie den Ausleihestatus des Buchs, und zeigen Sie die entsprechende Meldung an.

    Hier ist der aktualisierte Code:

    Schritt 1: Fügen Sie eine Methode zur Suche nach Büchern nach Titel in der JsonData-Klasse hinzu

    ```csharp

    public Book? SearchBookByTitle(string title)
    {
        return Books?.FirstOrDefault(b => b.Title.Equals(title, StringComparison.OrdinalIgnoreCase));
    }

    ```

    Schritt 2: Aktualisieren Sie die SearchBooks-Methode in der ConsoleApp-Klasse

    ```csharp

    async Task<ConsoleState> SearchBooks()
    {
        string bookTitle = ReadBookTitle();
        // ensure data is loaded
        await _jsonData.LoadData();
        // find the book by title
        Book? book = _jsonData.SearchBookByTitle(bookTitle);
        if (book == null)
        {
            Console.WriteLine($"No book found with title: {bookTitle}");
            return ConsoleState.PatronDetails;
        }
        // find the loan status of the book
        Loan? loan = _jsonData.Loans?.FirstOrDefault(l => l.BookItemId == book.Id && l.ReturnDate == null);
        if (loan == null)
        {
            Console.WriteLine($"{book.Title} is available for loan.");
        }
        else
        {
            Console.WriteLine($"{book.Title} is on loan to another patron. The return due date is {loan.DueDate}.");
        }
        return ConsoleState.PatronDetails;
    }

    ```

    Schritt 3: Aktualisieren Sie den Konstruktor der ConsoleApp-Klasse, um JsonData einzuschließen.

    ```csharp

    public class ConsoleApp
    {
        // Existing fields...
        JsonData _jsonData;
        public ConsoleApp(ILoanService loanService, IPatronService patronService, IPatronRepository patronRepository, ILoanRepository loanRepository, JsonData jsonData)
        {
            _patronRepository = patronRepository;
            _loanRepository = loanRepository;
            _loanService = loanService;
            _patronService = patronService;
            _jsonData = jsonData;
        }
        // Other methods...

    }

    ```

    Schritt 4: Aktualisieren Sie das Program.cs, um JsonData an ConsoleApp zu übergeben

    ```csharp

    using Microsoft.Extensions.DependencyInjection;
    using Library.Infrastructure.Data;
    using Library.ApplicationCore;
    using Microsoft.Extensions.Configuration;
    var services = new ServiceCollection();
    var configuration = new ConfigurationBuilder()
    .SetBasePath(Directory.GetCurrentDirectory())
    .AddJsonFile("appSettings.json")
    .Build();
    services.AddSingleton<IConfiguration>(configuration);
    services.AddScoped<IPatronRepository, JsonPatronRepository>();
    services.AddScoped<ILoanRepository, JsonLoanRepository>();
    services.AddScoped<ILoanService, LoanService>();
    services.AddScoped<IPatronService, PatronService>();
    services.AddSingleton<JsonData>();
    services.AddSingleton<ConsoleApp>();
    var servicesProvider = services.BuildServiceProvider();
    var consoleApp = servicesProvider.GetRequiredService<ConsoleApp>();
    consoleApp.Run().Wait();

    ```

    Mit diesen Änderungen sucht die SearchBooks-Methode in der ConsoleApp-Klasse nun nach einem Buch nach Titel in der Books.json-Datei und überprüft den Ausleihestatus in der Loans.json-Datei. Wenn das Buch für die Ausleihe bereit ist, wird eine Meldung angezeigt, die besagt, dass das Buch verfügbar ist. Wenn das Buch ausgeliehen wurde, wird eine Meldung angezeigt, die besagt, dass das Buch ausgeliehen ist und das Rückgabedatum übermittelt.

    > [!NOTE]
    > GitHub Copilot schlägt möglicherweise vor, LINQ-Abfragen in der SearchBooks-Methode zu verwenden, mit der ein Buchobjekt abgerufen wird, anstatt eine Methode in der JsonData-Klasse zu verwenden. Es könnte jedoch auch vorgeschlagen werden, Methoden in der `JsonData` Klasse zu erstellen, um einen Buchtitel abzurufen und den Ausleihstatus zu überprüfen (anstatt LINQ-Abfragen für die SearchBooks-Methode zu verwenden). Die folgenden Anweisungen basieren auf GitHub Copilot-Vorschlägen, die eine Kombination dieser Ansätze verwenden.

1. Fügen Sie die vorgeschlagene SearchBookByTitle-Methode am Ende der **JsonData**-Klasse hinzu.

    ```csharp

    public Book? SearchBookByTitle(string title)
    {
        return Books?.FirstOrDefault(b => b.Title.Equals(title, StringComparison.OrdinalIgnoreCase));
    }

    ```

1. Fügen Sie die _jsonData-Felderklärung vor dem Klassenkonstruktor zur ConsoleApp-Klasse hinzu.

    ```csharp

    JsonData _jsonData;

    ```

1. Fügen Sie dem ConsoleApp-Klassenkonstruktor einen JsonData-Parameter hinzu und verwenden Sie ihn, um das _jsonData-Feld innerhalb des Konstruktors zu initialisieren.

    Der aktualisierte Klassenkonstruktor sollte wie der folgende Codeschnipsel aussehen:

    ```csharp

    public ConsoleApp(ILoanService loanService, IPatronService patronService, IPatronRepository patronRepository, ILoanRepository loanRepository, JsonData jsonData)
    {
        _patronRepository = patronRepository;
        _loanRepository = loanRepository;
        _loanService = loanService;
        _patronService = patronService;
        _jsonData = jsonData;
    }

    ```

1. Beachten Sie, dass JsonData in der ConsoleApp-Klasse nicht erkannt wird.

    Sie müssen „using Library.Infrastructure.Data;“ am Anfang der Datei ConsoleApp.cs hinzufügen.

1. Stellen Sie sicher, dass die folgende "using"-Anweisung am Anfang der ConsoleApp.cs Datei hinzugefügt wird.

    ```csharp

    using Library.Infrastructure.Data;

    ```

1. Verwenden Sie die Codevorschläge, um die **SearchBooks**-Methode zu aktualisieren:

    Der vorgeschlagene Code sollte die SearchBookByTitle-Methode (oder eine LINQ-Abfrage) verwenden, um das Buch anhand des Titels zu suchen. Wenn das Buch gefunden wird, wird mithilfe einer LINQ-Abfrage ermittelt, ob das Buch ausgeliehen ist. Der Code enthält außerdem Logik, um den Verfügbarkeitsstatus des Buchs auf der Grundlage der Suchergebnisse anzuzeigen. Die zum Anzeigen von Antwortnachrichten verwendete Logik kann auf verschiedene Weise implementiert werden. Ein Beispiel finden Sie im folgenden Codeausschnitt.

    Der folgende Codeausschnitt zeigt eine mögliche Implementierung der SearchBook-Methode:

    ```csharp

    async Task<ConsoleState> SearchBooks()
    {
        string bookTitle = ReadBookTitle();
        Book? book = _jsonData.SearchBookByTitle(bookTitle);
        if (book == null)
        {
            Console.WriteLine($"No book found with title: {bookTitle}");
            return ConsoleState.PatronDetails;
        }
        Loan? loan = _jsonData.Loans?.FirstOrDefault(l => l.BookItemId == book.Id && l.ReturnDate == null);
        if (loan == null)
        {
            Console.WriteLine($"{book.Title} is available for loan.");
        }
        else
        {
            Console.WriteLine($"{book.Title} is on loan to another patron. The return due date is {loan.DueDate}.");
        }
        return ConsoleState.PatronDetails;
    }

    ```

1. Vergleichen Sie die vorhandene **Program.cs**-Datei mit den vorgeschlagenen Updates.

    ```csharp

    using Microsoft.Extensions.DependencyInjection;
    using Library.Infrastructure.Data;
    using Library.ApplicationCore;
    using Microsoft.Extensions.Configuration;
    var services = new ServiceCollection();
    var configuration = new ConfigurationBuilder()
        .SetBasePath(Directory.GetCurrentDirectory())
        .AddJsonFile("appSettings.json")
        .Build();
    services.AddSingleton<IConfiguration>(configuration);
    services.AddScoped<IPatronRepository, JsonPatronRepository>();
    services.AddScoped<ILoanRepository, JsonLoanRepository>();
    services.AddScoped<ILoanService, LoanService>();
    services.AddScoped<IPatronService, PatronService>();
    services.AddSingleton<JsonData>();
    services.AddSingleton<ConsoleApp>();
    var servicesProvider = services.BuildServiceProvider();
    var consoleApp = servicesProvider.GetRequiredService<ConsoleApp>();
    consoleApp.Run().Wait();

    ```

    Es ist kein Update erforderlich, wenn die Datei „Program.cs“ bereits den Code enthält, der das ASP.NET Core-Abhängigkeitseinfügungssystem anweist, eine einzelne Instanz der JsonData-Klasse zu erstellen und diese Instanz immer dann zu verwenden, wenn eine JsonData angefordert wird.

1. Wählen Sie die **SearchBooks**-Methode aus.

1. Öffnen Sie die Chatansicht, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```plaintext
    Explain the LINQ queries and the evaluation of the book's availability status.
    ```

1. Nehmen Sie sich kurz Zeit, um die von GitHub Copilot bereitgestellte Erklärung zu überprüfen.

    Für die Abfrage, die überprüft, ob das Buch ausgeliehen ist, sollte eine Beschreibung angezeigt werden, die der folgenden Erläuterung ähnelt:

    ```markdown
    **Search for the Loan Status of the Book**
    ```

    ```csharp

    Loan? loan = _jsonData.Loans?.FirstOrDefault(l => l.BookItemId == book.Id && l.ReturnDate == null);

    ```

    ```markdown
    - _jsonData.Loans: Accesses the list of loans from the JsonData class.

    - ?.: The null-conditional operator ensures that if _jsonData.Loans is null, the entire expression will return null without throwing a NullReferenceException.

    - FirstOrDefault: A LINQ method that returns the first element in the collection that matches the specified condition, or null if no such element is found.

    - Lambda Expression: l => l.BookItemId == book.Id && l.ReturnDate == null

        - l.BookItemId == book.Id: Checks if the BookItemId of the loan matches the Id of the book being searched.

        - l.ReturnDate == null: Checks if the loan's ReturnDate is null, indicating that the book is currently on loan and has not been returned.

    - Result: If a matching loan is found, it is assigned to the loan variable. If no matching loan is found, loan is null.

    **Evaluation of the Book's Availability Status**

    After executing the LINQ queries, the method evaluates the availability status of the book:

      - If loan is null, the book has been returned. The method prints that the book is available for loan.
      - If loan is not null, the book is currently on loan (no return date). The method prints that the book is on loan and provides the date when the book should be returned.

    ```

1. Überprüfen Sie die Logik, die durch die Abfrage zur Ermittlung des Ausleihstatus des Buchs (**Check if the Book is on Loan**) implementiert wird.

    Null-Bedingter Operator: „?.“ Der Operator wird bedingter NULL-Operator genannt. Sie stellt sicher, dass, wenn _jsonData.Loans null ist, der gesamte Ausdruck zu null ausgewertet wird, ohne eine NullReferenceException auszulösen.

    Lambda-Ausdruck: Der Lambda-Ausdruck „l => l.BookItemId == book. Id && l.ReturnDate == null" definiert die Bedingung für die FirstOrDefault-Methode. Es überprüft jedes Ausleihobjekt „l“ darauf, ob seine BookItemId mit der Id des Buchobjekts übereinstimmt und ob sein ReturnDate null ist.

    Dieser Code versucht, die erste Ausleihe in der _jsonData.Loans-Sammlung zu finden, bei dem die BookItemId mit der Id des angegebenen Buchs übereinstimmt und das ReturnDate null ist. Wenn keine solche Ausleihe gefunden wird oder wenn „_jsonData.Loans“ null ist, wird die Ausleihe auf null gesetzt.

    > [!NOTE]
    > Die meisten modernen Bibliotheken verfügen über mehrere Exemplare eines Buchs. Bei diesem Code wird davon ausgegangen, dass nur jeweils ein Exemplar jedes Buches vorhanden ist. Wenn die Bibliothek über mehrere Exemplare des gleichen Buchs verfügt, muss der Code aktualisiert werden, um mehrere Ausleihen des gleichen Buchs zu behandeln. In dieser Schulung gehen wir davon aus, dass nur ein einzelnes Exemplar jedes Buchs vorhanden ist und dass die bereitgestellte Logik ausreicht.

1. Speichern Sie Ihre Aktualisierungsdateien.

1. Erstellen Sie die Projektmappe, um sicherzustellen, dass keine Fehler vorhanden sind.

    Sie werden **Warnmeldungen** sehen, aber es sollte keine Fehler geben.

    Um die Projektmappe in der Ansicht „Projektmappen-Explorer“ zu erstellen, können Sie mit der rechten Maustaste auf **AccelerateDevGitHubCopilot** klicken und anschließend **Erstellen** auswählen.

#### Zusammenfassung - der Übung 5

Sie haben GitHub Copilot verwendet, um eine neue Funktion für die Bibliotheksanwendung zu implementieren. Sie haben einen neuen Zweig im Repository erstellt und dann GitHub Copilot verwendet, um Code-Vorschläge zu generieren, die Ihnen dabei halfen, die neue Funktion schneller und genauer zu implementieren. Sie haben eine neue SearchBooks-Aktion zu CommonActions hinzugefügt, die Methoden WriteInputOptions und ReadInputOptions in ConsoleApp.cs aktualisiert und eine neue SearchBooks-Methode erstellt, um den Verfügbarkeitsstatus eines Buches zu ermitteln.

### Übung 6: Fügen Sie Ihre Änderungen in den Hauptzweig des Repositorys ein

Die von Ihnen erstellte neue Funktion ermöglicht es Bibliothekaren, den Verfügbarkeitsstatus eines Buchs zu bestimmen. Jetzt müssen Sie überprüfen, ob die Funktion wie erwartet arbeitet, und ihre Änderungen im Hauptzweig des Repositorys zusammenführen.

In dieser Übung werden Sie die folgenden Aufgaben ausführen:

- Vergewissern, dass Ihr neues Feature wie erwartet funktioniert
- Synchronisieren Ihrer Änderungen mit dem Remoterepository
- Erstellen Sie einen „Pull Request“ (Anforderung zum Herunterladen), um Ihre Änderungen in den Hauptzweig des Repositorys zu übernehmen.

#### Aufgabe 1: Vergewissern Sie sich, dass Ihre neue Funktion wie erwartet arbeitet

Da Sie über keine automatisierten Tests verfügen, können Sie manuelle Tests verwenden, um zu überprüfen, ob das neue Feature wie erwartet funktioniert. Es ist wichtig, eine überprüfbare Datenquelle zu verwenden. In diesem Fall verwenden Sie die Dateien „Books.json“ und „Loans.json“, um zu überprüfen, ob die neue Funktion den Verfügbarkeitsstatus eines Buches korrekt meldet.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Ansicht „Projektmappen-Explorer“.

1. Klicken Sie zum Ausführen der Anwendung mit der rechten Maustaste auf **Library.Console**, wählen Sie **Debuggen** aus, und wählen Sie anschließend **Neue Instanz starten** aus.

1. Wenn Sie zur Eingabe eines Kundennamens aufgefordert werden, geben Sie **One** ein, und drücken Sie anschließend die EINGABETASTE.

    Daraufhin sollte eine Liste mit Kunden angezeigt werden, die der Suchabfrage entsprechen.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Zahl **2** ein, und drücken Sie anschließend die EINGABETASTE.

    Durch Eingeben von **2** wird der zweite Kunde in der Liste ausgewählt.

    Daraufhin sollten der Name und der Mitgliedschaftsstatus des Kunden angezeigt werden, gefolgt von Details zur Buchausleihe.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Option **b** ein, und drücken Sie anschließend die EINGABETASTE.

    Durch Eingabe von **b** wird die Option für die Suche nach dem Verfügbarkeitsstatus eines Buchs ausgewählt.

    Daraufhin sollte eine Aufforderung zur Eingabe eines Buchtitels angezeigt werden.

1. Geben Sie **Book One** ein, und drücken Sie anschließend die EINGABETASTE.

    In den ursprünglichen Daten, die Sie heruntergeladen haben, ist **Book One** derzeit von **Patron Forty-Nine** ausgeliehen und sollte daher nicht verfügbar sein.

1. Vergewissern Sie sich, dass in der Anwendung eine Nachricht mit dem Hinweis angezeigt wird, dass das Buch von einem anderen Kunden ausgeliehen wurde.

    Möglicherweise müssen Sie nach oben scrollen, um die Nachricht zu sehen.

1. Vergewissern Sie sich, dass **Book Nine** von **Patron One** zurückgegeben wurde.

    In der vorherigen Übung hatte **Patron One** im Rahmen eines Tests der Bibliotheksanwendung **Book Nine** zurückgeben. Sollte die Anwendung anzeigen, dass **Book Nine** von **Patron One** nicht zurückgegeben wurde, verwenden Sie die Eingabeoptionen, um **Book Nine** auszuwählen und zurückzugeben, bevor Sie fortfahren.

    > [!NOTE]
    > Die Datei „Library.Console.csproj“ stellt sicher, dass die JSON-Datendateien beim Erstellen der Anwendung in das Ausgabeverzeichnis kopiert werden. Durch Ausführen von Bereinigungs- oder Neuerstellungsvorgängen werden die Daten jedoch im Wesentlichen zurückgesetzt. Wiederholte Build-Vorgänge setzen die Daten im Ausgabeverzeichnis („/bin/Debug/net8.0/“) nicht zurück.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Option **b** ein, und drücken Sie anschließend die EINGABETASTE.

1. Geben Sie **Book Nine** ein, und drücken Sie anschließend die EINGABETASTE.

1. Vergewissern Sie sich, dass in der Anwendung eine Nachricht mit dem Hinweis angezeigt wird, dass das Buch zum Ausleihen verfügbar ist.

1. Geben Sie an der Eingabeaufforderung „Eingabeoptionen“ die Option **q** ein, und drücken Sie anschließend die EINGABETASTE.

1. Beenden Sie die Debugsitzung.

1. Öffnen Sie die Datei **Loans.json**.

    Die Datei Loans.json wird verwendet, um den Ausleihstatus jedes einzelnen Buches nachzuverfolgen. Mit der Datei Loans.json können Sie überprüfen, ob der Verfügbarkeitsstatus von „Book One“ und „Book Nine“ korrekt ist.

    Die aktualisierte Loans.json Datei sollte sich entweder im Ordner „Library.Console\bin\Debug\net8.0\Json" oder im Ordner „Library.Console\Json" befinden.

    - Wenn Sie den Visual Studio Code-Debugger zum Ausführen der App verwenden, sollte sich die aktualisierte Datei „Loans.json“ im Ordner „Library.Console\bin\Debug\net8.0\Json“ befinden.

    - Wenn Sie die App mit dem Befehl „dotnet run“ aus dem Ordner „AccelerateDevGitHubCopilot\src\Library.Console“ ausführen, sollte sich die aktualisierte Datei „Loans.json“ im Ordner „Library.Console\Json“ befinden.

1. Vergewissern Sie sich, dass die Darlehens-ID 37 und die Darlehens-ID 46 beide für Buch Eins („BookItemId“: 1) gelten.

    - Für die Ausleih-ID 37 sollte ein ReturnDate-Wert vorhanden sein (2024-01-17).
    - Für die Ausleih-ID 46 sollte kein ReturnDate-Wert vorhanden sein. Der Wert von „ReturnDate“ sollte Null sein.

    Der ReturnDate-Wert wird verwendet, um zu bestimmen, ob das Buch derzeit ausgeliehen ist. Wenn der ReturnDate-Wert null ist, gilt das Buch als ausgeliehen.

1. Überprüfen Sie, ob die Ausleih-ID 22 für Buch 9 („BookItemId“: 9) gilt und ob der Wert für „ReturnDate“ auf das heutige Datum eingestellt ist.

    Wenn Sie im Debugger arbeiten und die Lösung nach Änderungen an der Datei „Loans.json“ bereinigt haben, gehen diese Änderungen verloren. Nach der Bereinigung der Lösung wird die Datei „Loans.json“ bei der nächsten Ausführung der Anwendung auf die ursprünglichen Daten zurückgesetzt. Sie können die Datei „Loans.json“ manuell aktualisieren, um den Verfügbarkeitsstatus von Buch Eins und Buch Neun zu testen.

#### Aufgabe 2: Synchronisieren Sie Ihre Änderungen mit dem Remote-Repository

Sie können die Ansicht „Quellcodeverwaltung“ in Visual Studio Code verwenden, um Ihre Änderungen an das lokale Repository zu übergeben. Nachdem Sie Ihre Änderungen übernommen haben, können Sie sie mit dem Remote-Repository synchronisieren.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Wählen Sie die Ansicht „Quellcodeverwaltung“ aus.

1. Stellen Sie sicher, dass die Dateien „CommonActions.cs“, „ConsoleApp.cs“ und „JsonData.cs“ unter **Änderungen** aufgeführt sind.

    Wenn GitHub Copilot LINQ-Abfragen verwendet, um den Verfügbarkeitsstatus eines Buchs direkt in der SearchBooks-Methode zu ermitteln, wird JsonData.cs möglicherweise nicht unter **Änderungen** aufgeführt.

1. Verwenden Sie GitHub Copilot, um eine Nachricht für den **Commit** zu generieren.

1. Wählen Sie **Committen** und anschließend **Ja** aus, um Ihre Änderungen zu stagen und zu committen.

1. Synchronisieren Sie Ihre Änderungen mit dem Remoterepository, oder pushen Sie sie in das Remoterepository.

    Verwenden Sie auf Wunsch Ihr GitHub-Konto, um die Synchronisierung zu authentifizieren und zu autorisieren.

#### Aufgabe 3: Erstellen Sie eine Pull-Anfrage, um Ihre Änderungen in den Mainbranch des Repositorys zu übernehmen.

Sie können eine Pull-Anfrage verwenden, um Änderungen am Hauptzweig des Repositorys vorzuschlagen. Nachdem Sie eine Pull-Anfrage erstellt haben, können Sie die Änderungen überprüfen, kontrollieren, ob die Prüfungen bestanden wurden, und die Änderungen anschließend in den Mainbranch einbinden. GitHub Copilot kann Ihnen helfen, eine Zusammenfassung der Pull-Anforderung zu generieren, damit Prüfer Ihre Änderungen verstehen können.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie Ihr GitHub-Repository in einem Webbrowser.

1. Öffnen Sie die Registerkarte **Pull Requests**.

1. Wählen Sie **New pull request** aus.

1. Stellen Sie unter **Änderungen vergleichen** sicher, dass für den Branch **main** die Option **Basis** konfiguriert ist.

1. Stellen Sie sicher, dass für den Branch **book-availability** die Option **Vergleichen** konfiguriert ist.

    Nachdem Sie die Branches konfiguriert haben, wird ein Vergleich der Änderungen zwischen **main** und **book-availability** angezeigt. Die Änderungen, die Sie an den Dateien CommonActions.cs, ConsoleApp.cs und JsonDaa.cs vorgenommen haben, sollten angezeigt werden.

1. Klicken Sie auf **Pull Request erstellen**.

1. Geben Sie einen Titel für die Pull-Anfrage ein.

    Unternehmensangehörige mit einem Abonnement für GitHub Copilot Enterprise können GitHub Copilot verwenden, um eine zusammenfassende Beschreibung für eine Pull-Anfrage zu erstellen. Die detaillierte Zusammenfassung hilft Prüfern, Ihre Änderungen zu verstehen.

1. Verwenden Sie GitHub Copilot, um eine Zusammenfassung Ihrer Pull-Anfrage zu generieren.

    Um die Zusammenfassung zu erstellen, wählen Sie die Schaltfläche „Copilot-Aktionen“ und dann „**Zusammenfassung**“ aus.

    Sie können die Registerkarte „Vorschau“ verwenden, um die von GitHub Copilot erstellte Zusammenfassung der Pull-Anfragen zu überprüfen.

1. Vergewissern Sie sich, dass der Titel und die Beschreibung Ihre Codeaktualisierungen widerspiegeln, und wählen Sie anschließend **Pull Request erstellen** aus.

1. Warten Sie, bis die Überprüfungen abgeschlossen sind, und vergewissern Sie sich dann, dass alle Prüfungen bestanden wurden und dass keine Konflikte mit dem Basisbranch vorliegen.

    Es kann ein wenig dauern, bis die Überprüfungen abgeschlossen sind. Sie müssen alle identifizierten Probleme behandeln, um die Änderungen im Mainbranch mergen zu können.

1. Wählen Sie **Pull Request mergen** und anschließend **Mergen bestätigen** aus, um Ihre Änderungen im Mainbranch zu mergen.

    Beachten Sie, dass Sie den Zweig „Buchverfügbarkeit“ löschen können, nachdem Sie die Änderungen zusammengeführt haben.

1. Öffnen Sie Visual Studio Code.

1. Wechseln Sie zum **Hauptzweig** des Repositorys.

1. **Pullen** Sie die Änderungen aus dem Remoterepository.

    Wenn Sie dazu aufgefordert werden, verwenden Sie Ihr GitHub-Konto, um den Pull zu authentifizieren und zu autorisieren.

1. Vergewissern Sie sich, dass sich die Änderungen, die Sie im Branch **book-availability** vorgenommen haben, jetzt im Branch **main** befinden.

    Die Änderungen, die Sie an den Dateien „CommonActions.cs“ und „ConsoleApp.cs“ vorgenommen haben, sollten im Hauptzweig vorhanden sein.

#### Zusammenfassung - der Übung 6

In dieser Übung haben Sie den Code getestet und dann die Änderungen im Hauptzweig des Repositorys zusammengeführt. Sie haben Ihre Änderungen im lokalen Repository gespeichert, sie mit dem Remote-Repository synchronisiert und dann eine Pull-Anfrage erstellt, um Ihre Änderungen in den Hauptzweig des Repositorys zu übernehmen. Sie haben GitHub Copilot verwendet, um eine Zusammenfassung der Pull-Anfragen zu erstellen, damit die Prüfer Ihre Änderungen besser verstehen können.

## Teil 3: Entwickeln Sie Unit-Tests mit den GitHub Copilot-Tools

### Vor der Installation

#### Projektübersicht

Ihr Kollege hat ein Testprojekt namens UnitTests erstellt. Die vorhandenen Komponententests decken die Service-Klassen im Projekt „Library.ApplicationCore“ teilweise ab. Das Projekt „Library.ApplicationCore“ enthält die Geschäftsprozesslogik für ein Bibliotheksverwaltungssystem. Das Projekt UnitTests verwendet das xUnit-Framework zum Schreiben und Ausführen von Komponententests. Das Projekt verwendet auch die NSubstitute-Bibliothek zum Erstellen von Pseudoobjekten zu Testywecken.

Sie müssen das Projekt UnitTests erweitern, um die Datenzugriffsklassen im Library.Infrastructure-Projekt abzudecken.

#### Übungsszenario (Teil 3)

GitHub Copilot kann Ihnen beim Schreiben von Komponententests für Ihren Code helfen. Es gibt mehrere Möglichkeiten, GitHub Copilot zum Generieren von Komponententests zu verwenden:

- **Generieren von Testfällen**: Sie können GitHub Copilot verwenden, um Testfälle für Ihren Code zu generieren. Copilot kann Testfälle basierend auf dem von Ihnen geschriebenen Code vorschlagen. Anschließend können Sie diese Testfälle verwenden, um Komponententests für Ihren Code zu erstellen.
- **Generieren von Testmethoden**: Copilot kann auch Testmethoden für Ihren Code generieren. Sie können diese Testmethoden verwenden, um Komponententests für Ihren Code zu erstellen.
- **Generieren von Testassertionen**: Copilot kann Assertionen vorschlagen, die Sie in Ihren Komponententests verwenden können. Diese Assertionen können Ihnen helfen, das Verhalten Ihres Codes zu überprüfen.
- **Generieren von Testmodellen**: Copilot kann Testobjekte generieren, die Sie in Ihren Komponententests verwenden können. Diese Modellobjekte können Ihnen dabei helfen, den Code, den Sie testen möchten, von seinen Abhängigkeiten zu isolieren.
- **Generieren von Testdaten**: Copilot kann Testdaten generieren, die Sie in Ihren Komponententests verwenden können. Diese Testdaten können Ihnen dabei helfen, Ihren Code mit verschiedenen Eingaben zu testen.
- **Generieren von Testeinrichtungscode**: Copilot kann Einrichtungscode für Ihre Komponententests generieren. Dieser Code kann Ihnen beim Einrichten der Testumgebung helfen, bevor Sie Ihre Tests ausführen.
- **Generieren von Testnachbereitungscode**: Copilot kann Nachbereitungscode für Ihre Komponententests generieren. Dieser Code kann Ihnen helfen, die Testumgebung nach dem Ausführen der Tests zu bereinigen.

In Teil 3 dieser Übung entwickeln Sie Komponententests für das Library.Infrastructure-Projekt.

Der Teil umfasst die folgende Übung:

- Verwenden Sie GitHub Copilot, um das UnitTests-Projekt auszuwerten und zu erweitern.

### Übung 7: Verwenden von GitHub Copilot zum Auswerten und Erweitern des UnitTests-Projekts

In dieser Übung verwenden Sie GitHub Copilot, um die folgenden Aufgaben auszuführen:

1. Verwenden Sie GitHub Copilot, um das vorhandene UnitTests-Projekt auszuwerten.

1. Erweitern des UnitTests-Projekts, um mit dem Testen von Datenzugriffsklassen zu beginnen

#### Aufgabe 1: Verwenden von GitHub Copilot zum Auswerten des vorhandenen UnitTests-Projekts

Das Projekt UnitTests implementiert derzeit die folgende Ordnerstruktur:

- UnitTests\
  - ApplicationCore\
    - LoanService\
      - ExtendLoan.cs
      - ReturnLoan.cs
    - PatronService\
      - RenewMembership.cs
  - LoanFactory.cs
  - PatronFactory.cs

Diese Struktur spiegelt den Serviceteil des ApplicationCore-Projekts wider und unterstützt ihn.

- ApplicationCore\
  - Dienste\
    - LoanService.cs: Enthält die Methoden „ExtendLoan“ und „ReturnLoan“.
    - PatronService.cs: Enthält die Methode RenewMembership.

Die Auswertung der vorhandenen Komponententests hilft Ihnen bei der Entwicklung von Komponententests für die Datenzugriffsklassen im Library.Infrastructure-Projekt.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Schließen Sie alle Dateien, die Sie im Editor geöffnet haben.

1. Öffnen Sie die Chatansicht.

1. Fügen Sie dem Chat-Kontext die folgenden Dateien hinzu: **LoanFactory.cs**, **PatronFactory.cs**, **ExtendLoan.cs**, **ReturnLoan.cs**, **RenewMembership.cs**, **LoanService.cs**, **PatronService.cs**.

    Die Dateien befinden sich in den Ordnern „tests/UnitTests“, „tests/UnitTests/ApplicationCore/LoanService“, „tests/UnitTests/ApplicationCore/PatronService“ und „src/Library.ApplicationCore/Services“.

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace Explain the approach to unit testing that's been implemented in this workspace.
    ```

    Dieser Prompt fordert GitHub Copilot auf, den Ansatz für Komponententests im Kontext des Arbeitsbereichs zu erläutern. Im Prompt sind mehrere Dateien enthalten, um den Kontext für die Antwort bereitzustellen.

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Sie sollten eine Erklärung angezeigt bekommen, die der folgenden Beschreibung ähnelt:

    - Mock-Abhängigkeiten: Die Tests verwenden NSubstitute, um Mock-Implementierungen von Schnittstellen zu erstellen.
    - Testorganisation: Tests werden basierend auf den zu testenden Methoden in separate Dateien unterteilt. Beispielsweise werden die Methoden „ExtendLoan“ und „ReturnLoan“ in separaten Dateien im Ordner „LoanService“ getestet.
    - Assertionen: Assertionen werden verwendet, um das erwartete Ergebnis der einzelnen Tests zu überprüfen.
    - Testszenarios: Die Tests decken verschiedene Szenarios für jede Methode ab, z. B. das Zurückgeben unterschiedlicher Status basierend auf der Eingabe.
    - Isolation: Jeder Test ist von anderen isoliert, um Nebenwirkungen zu verhindern.
    - Factorymethoden: Factorymethoden werden verwendet, um Testdaten konsistent zu erstellen.

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace What are the benefits of this approach to unit testing?
    ```

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Sie sollten eine Erklärung sehen, die eine Liste mit Vorteilen zeigt, die der folgenden Liste ähnelt:

    - Isolation von Abhängigkeiten: Das Verwenden von Modellelementen isoliert die Arbeitseinheit von ihren Abhängigkeiten.
    - Wiederholbarkeit und Konsistenz: Factorymethoden bieten eine konsistente Möglichkeit zum Erstellen von Testdaten.
    - Lesbarkeit und Wartungsfreundlichkeit: Deskriptive Testmethoden und klare Anordnung von Testschritten verbessern die Lesbarkeit von Tests.
    - Umfassende Abdeckung: Das Testen verschiedener Szenarios stellt sicher, dass der Code stabil ist und verschiedene Grenzfälle behandelt.
    - Trennung von Zuständigkeiten: Die Trennung der Testdatenerstellung von der Testlogik selbst sorgt dafür, dass die Tests sauber sind und der Fokus auf das getestete Verhalten gelegt wird.
    - Sofortiges Feedback: Das Ausführen von Komponententests liefert sofortiges Feedback zur Korrektheit des Codes.

1. Fügen Sie dem Chat-Kontext die folgenden Dateien hinzu: **ExtendLoan.cs**, **ReturnLoan.cs**, **RenewMembership.cs**, **LoanFactory.cs**, **PatronFactory.cs**, **LoanService.cs**, **PatronService.cs**.

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace How can I extend the `UnitTests` project to begin testing methods in the `Library.Infrastructure` project? Provide a process overview.
    ```

    Diese Eingabeaufforderung fordert GitHub Copilot auf, eine Prozessübersicht für die Erweiterung des UnitTests-Projekts bereitzustellen, um mit dem Testen von Methoden im Library.Infrastructure-Projekt zu beginnen. Im Prompt sind mehrere Dateien enthalten, um den Kontext für die Antwort bereitzustellen.

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Sie sollten eine Erklärung angezeigt bekommen, die der folgenden Beschreibung ähnelt:

    ```markdown
    1. Add Project Reference:

      - Open the UnitTests.csproj file located at tests/UnitTests/UnitTests.csproj.
      - Add a reference to the Library.Infrastructure project.

    2. Identify methods to test:

      - Identify the methods in the Library.Infrastructure project that need to be tested. For example, if you want to test the LoanService class, identify the methods in the LoanService class that need to be tested.

    3. Create Test Classes:

      - Create new test classes in the tests/UnitTests directory to test the methods in the Library.Infrastructure project. For example, if you want to test LoanService, create a file named LoanServiceTests.cs.

    4. Write Unit Tests:

      - In the newly created test classes, write unit tests for the methods in the Library.Infrastructure project. Use the xUnit framework for writing tests and NSubstitute for mocking dependencies.

    5. Run Tests:

      - Use Visual Studio Code's integrated terminal or the Test Explorer to run the tests.
      - Ensure that the tests are discovered and executed correctly.
    ```

#### Aufgabe 2: Erweitern des UnitTests-Projekts, um mit dem Testen von Datenzugriffsklassen zu beginnen

In diesem Abschnitt der Übung verwenden Sie GitHub Copilot, um Komponententests für das Library.Infrastructure-Projekt zu erstellen.

Das Library.Infrastructure-Projekt enthält Datenzugriffsklassen, die mit dem Dateisystem zusammenarbeiten, um Daten zu laden und zu speichern. Das Projekt umfasst die folgenden Klassen:

- JsonData: Eine Klasse, die JSON-Daten lädt und speichert
- JsonLoanRepository: Eine Klasse, die die ILoanRepository-Schnittstelle implementiert und die JsonData-Klasse zum Laden und Speichern von Loan-Daten verwendet
- JsonPatronRepository: Eine Klasse, die die IPatronRepository-Schnittstelle implementiert und die JsonData-Klasse zum Laden und Speichern von Patron-Daten verwendet.

Zunächst schreiben Sie Komponententests für die JsonLoanRepository-Klasse.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Fügen Sie die folgende Projektdatei zum Chatkontext hinzu: **UnitTests.csproj**.

1. Geben Sie in der Chatansicht den folgenden Prompt ein:

    ```plaintext
    @workspace Explain how to add a reference to the Library.Infrastructure project inside `UnitTests.csproj`.
    ```

    Diese Eingabeaufforderung fordert GitHub Copilot auf, zu erklären, wie ein Verweis auf das Projekt „Library.Infrastructure“ in die Datei „UnitTests.csproj“ eingefügt werden kann.

1. Verwenden Sie die GitHub Copilot-Antwort, um die Datei „UnitTests.csproj“ zu aktualisieren.

    Die aktualisierte Datei „UnitTests.csproj“ sollte dem folgenden XML-Code ähneln:

    ```xml

    <Project Sdk="Microsoft.NET.Sdk">
      <PropertyGroup>
        <TargetFramework>net8.0</TargetFramework>
        <ImplicitUsings>enable</ImplicitUsings>
        <Nullable>enable</Nullable>
        <IsPackable>false</IsPackable>
        <IsTestProject>true</IsTestProject>
      </PropertyGroup>
      <ItemGroup>
        <PackageReference Include="coverlet.collector" Version="6.0.0" />
        <PackageReference Include="Microsoft.NET.Test.Sdk" Version="17.8.0" />
        <PackageReference Include="NSubstitute" Version="5.1.0" />
        <PackageReference Include="xunit" Version="2.5.3" />
        <PackageReference Include="xunit.runner.visualstudio" Version="2.5.3" />
      </ItemGroup>
      <ItemGroup>
        <Using Include="Xunit" />
      </ItemGroup>
      <ItemGroup>
        <ProjectReference Include="..\..\src\Library.ApplicationCore\Library.ApplicationCore.csproj" />
        <ProjectReference Include="..\..\src\Library.Infrastructure\Library.Infrastructure.csproj" />
      </ItemGroup>
    </Project>

    ```

1. Öffnen Sie die Datei **JsonLoanRepository.cs**.

    JsonLoanRepository.cs befindet sich im Ordner „src/Library.Infrastructure/Data/".

1. Nehmen Sie sich eine Minute Zeit, um die **JsonLoanRepository.cs**-Datei zu überprüfen.

    ```csharp

    using Library.ApplicationCore;
    using Library.ApplicationCore.Entities;
    namespace Library.Infrastructure.Data;
    public class JsonLoanRepository : ILoanRepository
    {
        private readonly JsonData _jsonData;
        public JsonLoanRepository(JsonData jsonData)
        {
            _jsonData = jsonData;
        }
        public async Task<Loan?> GetLoan(int id)
        {
            await _jsonData.EnsureDataLoaded();
    
            foreach (Loan loan in _jsonData.Loans!)
            {
                if (loan.Id == id)
                {
                    Loan populated = _jsonData.GetPopulatedLoan(loan);
                    return populated;
                }
            }
            return null;
        }
        public async Task UpdateLoan(Loan loan)
        {
            Loan? existingLoan = null;
            foreach (Loan l in _jsonData.Loans!)
            {
                if (l.Id == loan.Id)
                {
                    existingLoan = l;
                    break;
                }
            }
            if (existingLoan != null)
            {
                existingLoan.BookItemId = loan.BookItemId;
                existingLoan.PatronId = loan.PatronId;
                existingLoan.LoanDate = loan.LoanDate;
                existingLoan.DueDate = loan.DueDate;
                existingLoan.ReturnDate = loan.ReturnDate;
                await _jsonData.SaveLoans(_jsonData.Loans!);
                await _jsonData.LoadData();
            }
        }
    }

    ```

1. Beachten Sie die folgenden Details zur **JsonLoanRepository**-Klasse:

    - Die JsonLoanRepository-Klasse enthält zwei Methoden: GetLoan und UpdateLoan.
    - Die Klasse JsonLoanRepository verwendet ein JsonData-Objekt, um Ausleihdaten zu laden und zu speichern.

    Zunächst schreiben Sie Komponententests für die GetLoan-Methode.

1. Erstellen Sie die folgende Ordnerstruktur im **UnitTests**-Projekt.

    - Infrastruktur\
        - JsonLoanRepository\

    Diese Ordnerstruktur spiegelt den Ansatz für die Library.ApplicationCore-Komponententests wieder.

1. Erstellen Sie eine Klassendatei mit dem Namen **GetLoan** im Ordner JsonLoanRepository.

1. Nehmen Sie sich eine Minute Zeit, um die Anforderungen an die Feld- und Klassenkonstruktoren für die GetLoan-Unit-Tests zu betrachten.

    Die JsonLoanRepository.GetLoan-Methode empfängt beim Aufrufen einen Ausleih-ID-Parameter. Die Methode verwendet „_jsonData.EnsureDataLoaded“, um die neuesten JSON-Daten abzurufen, und „_jsonData.Loans“, um nach einem passenden Ausleihvorgang zu suchen. Wenn die Methode eine übereinstimmende Ausleih-ID findet, gibt sie ein ausgefülltes Ausleihobjekt zurück (ausgefüllt). Wenn die Methode keine übereinstimmende Ausleih-ID finden kann, gibt sie null zurück.

    GetLoan-Komponententests:

    - Sie können ein Mock-Ausleihvorgangs-Repository-Objekt („_mockLoanRepository“) verwenden, um den Fall zu testen, in dem eine übereinstimmende ID gefunden wird. Laden Sie das Modell mit der ID, die Sie suchen möchten. Die Klasse ReturnLoanTest zeigt, wie die ILoanRepository-Schnittstelle vorgetäuscht und ein Ausleihevorgangs-Repository-Mockobjekt instanziiert wird.

    - Sie können ein nicht-mockartiges Ausleihevorgangsregisterobjekt („_jsonLoanRepository“) verwenden, um den Fall zu testen, in dem keine übereinstimmende ID gefunden wird. Geben Sie einfach eine Loan-ID an, die nicht in der Datei enthalten ist. Alle über 100 sollten funktionieren.

    - Sie benötigen ein JsonData-Objekt, um ein nicht-mockartiges JsonLoanRepository-Objekt zu erstellen. Da das UnitTests-Projekt keinen Zugriff auf das vom ConsoleApp-Projekt erstellte JsonData-Objekt hat, müssen Sie eines über die IConfiguration-Schnittstelle erstellen.

1. Fügen Sie dem Chat-Kontext die folgenden Dateien hinzu: **JsonLoanRepository.cs**, **ReturnLoan.cs**, **LoanService.cs**, **LoanFactory.cs**, **JsonData.cs**.

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace Create fields and a class constructor for the `GetLoan.cs` file. The class will be used to create unit tests for the GetLoan method in the `JsonLoanRepository.cs` file. Create the following private readonly fields: `_mockLoanRepository`, `_jsonLoanRepository`, `_configuration`, and `_jsonData`. Instantiate the fields in the `GetLoanTest` constructor. Use `ConfigurationBuilder` to create a `_configuration` object that can be used to instantiate the JsonData object.
    ```

    Dieser Prompt fordert GitHub Copilot auf, Felder und einen Klassenkonstruktor vorzuschlagen.

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Es sollte ein Codevorschlag angezeigt werden, der dem folgenden Codeausschnitt ähnelt:

    ```csharp

    using NSubstitute;
    using Library.ApplicationCore;
    using Library.ApplicationCore.Entities;
    using Library.ApplicationCore.Interfaces;
    using Library.Infrastructure.Data;
    using Microsoft.Extensions.Configuration;
    namespace UnitTests.Infrastructure.JsonLoanRepository;
    public class GetLoanTest
    {
        private readonly ILoanRepository _mockLoanRepository;
        private readonly JsonLoanRepository _jsonLoanRepository;
        private readonly IConfiguration _configuration;
        private readonly JsonData _jsonData;
        public GetLoanTest()
        {
            _mockLoanRepository = Substitute.For<ILoanRepository>();
            _configuration = new ConfigurationBuilder()
                .AddJsonFile("appsettings.json")
                .Build();
            _jsonData = new JsonData(_configuration);
            _jsonLoanRepository = new JsonLoanRepository(_jsonData);
        }
        // Add test methods here
    }

    ```

1. Verwenden Sie den von GitHub Copilot bereitgestellten Code-Vorschlag, um **GetLoan.cs** zu aktualisieren.

1. Beachten Sie die folgenden Probleme:

    - Es gibt einen Konflikt zwischen dem „namespace“ und der Verwendung von „JsonLoanRepository“ im Code. Sie sollten „namespace" in GetLoans.cs aktualisieren, um dem in den Dateien ReturnLoan.cs und RenewMembership.cs verwendeten Muster zu folgen.

    - Wenn ILoanRepository in Ihrem Code nicht erkannt wird, müssen Sie möglicherweise eine Anweisungsrichtlinie für Library.ApplicationCore am Anfang der Datei hinzufügen.

    - Wenn das _configuration-Objekt nicht korrekt instanziiert wird, müssen Sie möglicherweise die Codezeile mit ConfigurationBuilder aktualisieren. Sie können den Code vereinfachen, indem Sie „_configuration = new ConfigurationBuilder().Build();“ verwenden.

    - Wenn GitHub Copilot „using Library.ApplicationCore.Interfaces“ vorschlägt, können Sie es am Anfang der Datei löschen.

1. Aktualisieren Sie die **GetLoan.cs**-Datei so, dass sie mit dem folgenden Codeausschnitt übereinstimmt:

    ```csharp

    using NSubstitute;
    using Library.ApplicationCore;
    using Library.ApplicationCore.Entities;
    using Library.Infrastructure.Data;
    using Microsoft.Extensions.Configuration;
    namespace UnitTests.Infrastructure.JsonLoanRepositoryTests;
    public class GetLoanTest
    {
        private readonly ILoanRepository _mockLoanRepository;
        private readonly JsonLoanRepository _jsonLoanRepository;
        private readonly IConfiguration _configuration;
        private readonly JsonData _jsonData;
        public GetLoanTest()
        {
            _mockLoanRepository = Substitute.For<ILoanRepository>();
            _configuration = new ConfigurationBuilder().Build();
            _jsonData = new JsonData(_configuration);
            _jsonLoanRepository = new JsonLoanRepository(_jsonData);
        }
    }

    ```

    Die Aktualisierungen des Codes betreffen die im vorherigen Schritt identifizierten Probleme. Durch die Erstellung des Projekts werden die im Editor identifizierten Probleme behoben.

1. Fügen Sie dem Chat-Kontext die folgenden Dateien hinzu: **JsonLoanRepository.cs**, **ReturnLoan.cs**, **LoanService.cs**, **LoanFactory.cs**, **JsonData.cs**, **Loans.json**.

1. Wählen Sie den Inhalt der Datei „GetLoan.cs“ aus und geben Sie dann die folgende Eingabeaufforderung in der Chat-Ansicht ein:

    ```plaintext
    @workspace Update the selection to include a unit test for the `JsonLoanRepository.GetLoan` method. The unit test should test the case where a loan ID is found in the data. Use `_mockLoanRepository` to arrange the expected return loan. Use `_jsonLoanRepository` to return an actual loan. Asserts should verify that the return loan ID matches the expected loan ID. Use a loan ID that exists in the `Loans.json` file.
    ```

    Diese Eingabeaufforderung fordert GitHub Copilot auf, einen Komponententest für die Methode „JsonLoanRepository.GetLoan“ vorzuschlagen. Der Komponententest sollte den Fall testen, in dem eine Loan-ID in den Daten gefunden wird. Der Test sollte „_mockLoanRepository“ verwenden, um die erwartete Rückgabe zu arrangieren, „_jsonLoanRepository“, um einen tatsächlichen Ausleihevorgang zurückzugeben, und Behauptungen zu überprüfen, ob die Rückgabe-ID mit der erwarteten Ausleihe-ID übereinstimmt. Die Ausleihe-ID sollte in der Loans.json-Datei vorhanden sein.

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Es sollte ein Codevorschlag angezeigt werden, der dem folgenden Codeausschnitt ähnelt:

    ```csharp

    using NSubstitute;
    using Library.ApplicationCore;
    using Library.ApplicationCore.Entities;
    using Library.Infrastructure.Data;
    using Microsoft.Extensions.Configuration;
    using Xunit;
    namespace UnitTests.Infrastructure.JsonLoanRepositoryTests;
    public class GetLoanTest
    {
        private readonly ILoanRepository _mockLoanRepository;
        private readonly JsonLoanRepository _jsonLoanRepository;
        private readonly IConfiguration _configuration;
        private readonly JsonData _jsonData;
        public GetLoanTest()
        {
            _mockLoanRepository = Substitute.For<ILoanRepository>();
            _configuration = new ConfigurationBuilder().Build();
            _jsonData = new JsonData(_configuration);
            _jsonLoanRepository = new JsonLoanRepository(_jsonData);
        }
        [Fact(DisplayName = "JsonLoanRepository.GetLoan: Returns loan when loan ID is found")]
        public async Task GetLoan_ReturnsLoanWhenLoanIdIsFound()
        {
            // Arrange
            var loanId = 1; // Use a loan ID that exists in the Loans.json file
            var expectedLoan = new Loan { Id = loanId, BookItemId = 101, PatronId = 202, LoanDate = DateTime.Now, DueDate = DateTime.Now.AddDays(14) };
            _mockLoanRepository.GetLoan(loanId).Returns(expectedLoan);
            await _jsonData.EnsureDataLoaded(); // Ensure data is loaded
            // Act
            var actualLoan = await _jsonLoanRepository.GetLoan(loanId);
            // Assert
            Assert.NotNull(actualLoan);
            Assert.Equal(expectedLoan.Id, actualLoan?.Id);
        }
    }

    ```

1. Verwenden Sie den von GitHub Copilot bereitgestellten Code-Vorschlag, um **GetLoan.cs** zu aktualisieren.

    Die JsonLoanRepository.GetLoan-Methode ruft „_jsonData.EnsureDataLoaded“ auf, um sicherzustellen, dass die JSON-Daten geladen werden. Sie können die Codezeile, die „_jsonData.EnsureDataLoaded“ in der Testmethode aufruft, löschen, falls sie enthalten ist.

    Wenn die Klasse „Ausleihe“ in Ihrem Code nicht erkannt wird, stellen Sie sicher, dass Sie oben in der Datei „GetLoan.cs“ eine Anweisung „using Library.ApplicationCore.Entities“ haben. Die „Ausleihe"-Klasse befindet sich im Namensbereich „Library.ApplicationCore.Entities".

1. Erstellen Sie die AccelerateDevGitHubCopilot-Lösung, um sicherzustellen, dass keine Fehler vorliegen.

1. Verwenden Sie das Feature für die automatische Vervollständigung von GitHub Copilot, um einen Test für den Fall zu erstellen, in dem die Loan-ID nicht gefunden wird.

    Fügen Sie nach der Methode „GetLoan_ReturnsLoanWhenLoanIdIsFound“ eine Leerzeile ein.

    Akzeptieren Sie die Vorschläge für die automatische Vervollständigung, um eine neue Testmethode zu erstellen.

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Das Feature für die automatische Vervollständigung von GitHub Copilot wird wahrscheinlich ein Modell eines erwarteten Loan-Elements erstellen, obwohl es nicht benötigt wird. Sie können den Code löschen, der einen erwarteten Ausleihevorgang vortäuscht, aber Sie benötigen eine Ausleih-ID, die in der Datei „Loans.json“ nicht vorhanden ist.

    Es sollte ein Codevorschlag angezeigt werden, der einem der folgenden Codeausschnitte ähnelt:

    ```csharp

    [Fact(DisplayName = "JsonLoanRepository.GetLoan: Returns null when loan ID is not found")]
    public async Task GetLoan_ReturnsNullWhenLoanIdIsNotFound()
    {
        // Arrange
        var loanId = 999; // Use a loan ID that does not exist in the Loans.json file
        var expectedLoan = new Loan { Id = loanId, BookItemId = 101, PatronId = 202, LoanDate = DateTime.Now, DueDate = DateTime.Now.AddDays(14) };
        _mockLoanRepository.GetLoan(loanId).Returns(expectedLoan);
        // Act
        var actualLoan = await _jsonLoanRepository.GetLoan(loanId);
        // Assert
        Assert.Null(actualLoan);
    }

    ```

1. Akzeptieren Sie den Vorschlag zur automatischen Vervollständigung, der einen AusleiheID-Wert zuweist, der nicht im Datensatz enthalten ist.

    Wenn keiner der Vorschläge AusleihID-Nummern zuweist, die nicht im Datensatz enthalten sind, können Sie die Tastenkombination **Strg+Eingabe** verwenden, um weitere Vorschläge aufzulisten.

1. Beachten Sie, dass die Komponententests Zugriff auf die JSON-Datendateien erfordern.

    Die JsonLoanRepository.GetLoan-Methode verwendet ein JsonData-Objekt zum Laden und Speichern von Ausleihevorgangsdaten.

    Die JSON-Datendateien befinden sich im Ordner „Library.Console\Json“. Sie müssen die Datei „UnitTests.csproj“ aktualisieren, um diese Dateien in das Testprojekt aufzunehmen.

1. Fügen Sie der Datei **UnitTests.csproj** den folgenden XML-Ausschnitt hinzu:

    ```xml

    <ItemGroup>
        <None Include="..\..\src\Library.Console\Json\**\*">
            <Link>Json\%(RecursiveDir)%(FileName)%(Extension)</Link>
            <CopyToOutputDirectory>PreserveNewest</CopyToOutputDirectory>
        </None>
    </ItemGroup>

    ```

    Dadurch wird sichergestellt, dass die JSON-Datendateien beim Ausführen der Tests in das Ausgabeverzeichnis kopiert werden.

#### Aufgabe 3: Überprüfen Ihrer Arbeit

Es gibt mehrere Möglichkeiten zum Ausführen der Komponententests für die JsonLoanRepository-Klasse. Sie können den Test Explorer von Visual Studio Code, das integrierte Terminal oder den Befehl „dotnet test“ verwenden.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Stellen Sie sicher, dass die Datei „GetLoans.cs“ im Editor geöffnet ist.

1. Erstellen Sie die Lösung, und vergewissern Sie sich, dass keine Fehler vorhanden sind.

    Klicken Sie mit der rechten Maustaste auf **AccelerateDevGitHubCopilot**, und wählen Sie dann **Erstellen** aus.

1. Beachten Sie die grüne Wiedergabeschaltfläche links neben den Testmethoden.

1. Öffnen Sie die Test-Explorer-Ansicht von Visual Studio Code.

    Um die Test-Explorer-Ansicht zu öffnen, wählen Sie das Reagenzglassymbol auf der Aktivitätsleiste links aus. Der Test-Explorer wird auf der Benutzeroberfläche als „Testen“ beschriftet.

    Der Test-Explorer ist eine Strukturansicht, in der alle Testfälle in Ihrem Arbeitsbereich angezeigt werden. Sie können Ihre Testfälle ausführen/debuggen und die Testergebnisse mithilfe des Test-Explorers anzeigen.

1. Erweitern Sie **UnitTests** und die darunter liegenden Knotenpunkte, um **GetLoanTest** zu finden.

1. Führen Sie den Testfall **JsonLoanRepository.GetLoan: Returns loan when loan ID is found** aus.

    > [!NOTE]
    > GitHub Copilot hat die Testmethode möglicherweise anders benannt. Führen Sie die Testmethode aus, die eine Ausleihe-ID verwendet, die in den Daten vorhanden ist.

1. Beachten Sie die Testergebnisse in der Test-Explorer-Ansicht und im Editor.

    Es sollte ein grünes Häkchen angezeigt werden, wenn der Test erfolgreich durchgeführt wurde.

1. Verwenden Sie den Editor, um den Testfall **JsonLoanRepository.GetLoan: Returns null when loan ID is not found** auszuführen.

1. Beachten Sie die Testergebnisse in der Test-Explorer-Ansicht und im Editor.

    Um den Test im Editor auszuführen, wählen Sie links neben der Testmethode die grüne Wiedergabeschaltfläche aus.

1. Stellen Sie sicher, dass der Testfall **JsonLoanRepository.GetLoan: Returns null when loan ID is not found** erfolgreich durchgeführt wird.

    Links neben beiden Tests sollte ein grünes Häkchen angezeigt werden.

#### Zusammenfassung - der Übung 7

In dieser Übung haben Sie GitHub Copilot verwendet, um das vorhandene UnitTests-Projekt zu bewerten und das Projekt zu erweitern, um mit dem Testen der Datenzugriffsklassen im Library.Infrastructure-Projekt zu beginnen. Sie haben einen Verweis auf das Library.Infrastructure-Projekt in der Datei UnitTests.csproj hinzugefügt und Komponententests für die JsonLoanRepository-Klasse erstellt. Mithilfe von GitHub Copilot haben Sie die Unit-Tests für die GetLoan-Methode in der JsonLoanRepository-Klasse geschrieben. Sie haben die Komponententests mithilfe des Test-Explorers von Visual Studio Code ausgeführt und überprüft, ob die Tests bestanden haben.

## Teil 4: Codeabschnitte mit den GitHub Copilot-Tools umgestalten und verbessern

### Vor der Installation

#### Projektübersicht

Sie und Ihre Kollegen haben die erste Entwicklungsphase des Projekts abgeschlossen und untersuchen nun Möglichkeiten, ihre Codebasis umzugestalten und zu verbessern.

Codeumgestaltung ist ein Prozess, der vorhandenen Code neu strukturiert, ohne dessen externes Verhalten zu ändern. Die Umgestaltung wird häufig verwendet, um einen bestimmten Aspekt Ihres Codes zu verbessern. GitHub Copilot kann Ihnen helfen, Ihren Code umzugestalten, indem Änderungen vorgeschlagen werden, die die Qualität, Zuverlässigkeit, Leistung und Sicherheit des Codes verbessern.

#### Übungsszenario (Teil 4)

In Teil 4 dieser Übung verwenden Sie GitHub Copilot, um die folgenden Codeabschnitte umzugestalten:

- Sie gestalten die EnumHelper-Klasse so um, dass Wörterbücher anstelle von Reflexion verwendet werden. Durch das Verwenden von Wörterbüchern wird die Leistung verbessert, indem der Mehraufwand der Reflexion reduziert wird. Das Entfernen der Reflexion verbessert auch die Lesbarkeit, Wartungsfreundlichkeit und Sicherheit von Code.

- Sie gestalten die Datenzugriffsmethoden so um, dass LINQ (Language Integrated Query) anstelle von foreach-Schleifen verwendet wird. Das Verwenden von LINQ bietet eine präzisere und besser lesbare Möglichkeit zum Abfragen von Sammlungen, Datenbanken und XML-Dokumenten. Außerdem kann dadurch die Lesbarkeit, Wartungsfreundlichkeit und Leistung von Code verbessert werden.

Dieser Teil umfasst die folgenden Übungen:

- Verwenden von GitHub Copilot zum Umgestalten der EnumHelper-Klasse.
- Verwenden Sie GitHub Copilot, um die Datenzugriffsklassen mit LINQ zu verbessern.

### Übung 8: Verwenden von GitHub Copilot zum Umgestalten der EnumHelper-Klasse

Die Reflexion ist ein leistungsfähiges Feature, mit dem Sie Objekte während der Runtime untersuchen und bearbeiten können. Reflexion kann jedoch langsam sein, und es gibt dabei potenzielle Sicherheitsrisiken, die berücksichtigt werden sollten.

Die vorhandene EnumHelper-Klasse verwendet die Reflexion, um das Beschreibungsattribut eines Enumerationswerts abzurufen. Sie können die EnumHelper-Klasse so umgestalten, dass Wörterbücher anstelle von Reflexion verwendet werden. Das Verwenden von Wörterbüchern kann die Leistung verbessern und Bedenken bezüglich der Sicherheit beseitigen, die mit Reflexion verbunden sind.

In dieser Übung verwenden Sie GitHub Copilot, um die EnumHelper-Klasse umzugestalten.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Verwenden Sie die Projektmappen-Explorer-Ansicht, um die Datei „EnumHelper.cs“ zu öffnen.

    EnumHelper.cs befindet sich im Ordner „src/Library.ApplicationCore/Enums".

    ```csharp

    using System.ComponentModel;
    using System.Reflection;
    namespace Library.ApplicationCore.Enums;
    public static class EnumHelper
    {
        public static string GetDescription(Enum value)
        {
            if (value == null)
                return string.Empty;
            FieldInfo fieldInfo = value.GetType().GetField(value.ToString())!;
            DescriptionAttribute[] attributes =
                (DescriptionAttribute[])fieldInfo.GetCustomAttributes(typeof(DescriptionAttribute), false);
            if (attributes != null && attributes.Length > 0)
            {
                return attributes[0].Description;
            }
            else
            {
                return value.ToString();
            }
        }
    }

    ```

1. Öffnen Sie die Chat-Ansicht und fügen Sie dann die folgenden Dateien zum Chat-Kontext hinzu: **EnumHelper.cs**, **LoanExtensionStatus.cs**, **LoanReturnStatus.cs**, **MembershipRenewalStatus.cs**.

1. Geben Sie den folgenden Prompt ein:

    ```plaintext
    @workspace I want to refactor the `EnumHelper` class using dictionaries rather than reflection to get enum description attributes. I want a separate dictionary for each enum. The enum values are in the `LoanExtensionStatus.cs`, `LoanReturnStatus.cs`, and `MembershipRenewalStatus.cs` files. Explain how to update the EnumHelper class to use dictionaries and provide the updated code.
    ```

    Dieser Prompt fordert GitHub Copilot auf, eine Erklärung zum Aktualisieren der EnumHelper-Klasse für das Verwenden von Wörterbüchern anstelle von Reflexion bereitzustellen. Außerdem wird nach dem aktualisierten Code gefragt, der für jeden Enumerationswert Wörterbücher verwendet.

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellte Erklärung zu überprüfen.

    Sie sollte der folgenden Beschreibung ähneln:

    ```markdown
    To refactor the EnumHelper class to use dictionaries for each enum, you need to create a dictionary for each enum type that maps the enum values to their descriptions. This will eliminate the need for reflection at runtime.

    Here's how you can update the EnumHelper class:

    1. Create dictionaries for each enum type.
    2. Populate these dictionaries with the enum values and their corresponding descriptions.
    3. Update the GetDescription method to use these dictionaries.

    Below is the updated code for the EnumHelper class:

    ```

    ```csharp

    using System.ComponentModel;
    using System.Collections.Generic;
    namespace Library.ApplicationCore.Enums
    {
        public static class EnumHelper
        {
            private static readonly Dictionary<MembershipRenewalStatus, string> MembershipRenewalStatusDescriptions = new()
            {
                { MembershipRenewalStatus.Success, "Membership renewal was successful." },
                { MembershipRenewalStatus.PatronNotFound, "Patron not found." },
                { MembershipRenewalStatus.TooEarlyToRenew, "It is too early to renew the membership." },
                { MembershipRenewalStatus.LoanNotReturned, "Cannot renew membership due to an outstanding loan." },
                { MembershipRenewalStatus.Error, "Cannot renew membership due to an error." }
            };
            private static readonly Dictionary<LoanReturnStatus, string> LoanReturnStatusDescriptions = new()
            {
                { LoanReturnStatus.Success, "Book was successfully returned." },
                { LoanReturnStatus.LoanNotFound, "Loan not found." },
                { LoanReturnStatus.AlreadyReturned, "Cannot return book as the book is already returned." },
                { LoanReturnStatus.Error, "Cannot return book due to an error." }
            };
            private static readonly Dictionary<LoanExtensionStatus, string> LoanExtensionStatusDescriptions = new()
            {
                { LoanExtensionStatus.Success, "Book loan extension was successful." },
                { LoanExtensionStatus.LoanNotFound, "Loan not found." },
                { LoanExtensionStatus.LoanExpired, "Cannot extend book loan as it already has expired. Return the book instead." },
                { LoanExtensionStatus.MembershipExpired, "Cannot extend book loan due to expired patron's membership." },
                { LoanExtensionStatus.LoanReturned, "Cannot extend book loan as the book is already returned." },
                { LoanExtensionStatus.Error, "Cannot extend book loan due to an error." }
            };
            public static string GetDescription(Enum value)
            {
                if (value == null)
                    return string.Empty;
                return value switch
                {
                    MembershipRenewalStatus status => MembershipRenewalStatusDescriptions[status],
                    LoanReturnStatus status => LoanReturnStatusDescriptions[status],
                    LoanExtensionStatus status => LoanExtensionStatusDescriptions[status],
                    _ => value.ToString()
                };
            }
        }
    }

    ```

    ```markdown

    This refactored EnumHelper class uses dictionaries to store the descriptions for each enum type. The GetDescription method now uses pattern matching to determine the type of the enum and retrieves the description from the appropriate dictionary. This approach avoids the use of reflection and improves performance.

    ```

    > [!NOTE]
    > Wenn GitHub Copilot die Wörterbücher nicht mit den richtigen Beschreibungen auffüllt, stellen Sie sicher, dass die GitHub Copilot-Erweiterung keinen Neustart anfordert. Falls Copilot sie korrekt auffüllt, starten Sie die Erweiterung neu, und verwenden Sie den Prompt erneut.

1. Verwenden Sie die von GitHub Copilot vorgeschlagene EnumHelper-Klasse, um Ihre EnumHelper.cs-Datei zu aktualisieren.

1. Stellen Sie sicher, dass die aktualisierte EnumHelper-Klasse die Enumerationswerte aus den Dateien LoanExtensionStatus.cs, LoanReturnStatus.cs und MembershipRenewalStatus.cs verwendet.

    Öffnen Sie die einzelnen Enumerationsdateien, und stellen Sie sicher, dass die Enumerationswerte in den Wörterbüchern korrekt sind. Wenn Diskrepanzen vorliegen, fordern Sie GitHub Copilot dazu auf, die Wörterbücher für jede Enumeration einzeln zu aktualisieren. Beispielsweise können Sie die folgende Eingabeaufforderung für die Aufzählung „LoanExtensionStatus“ verwenden:

    ```plaintext
    @workspace Use the description values in LoanExtensionStatus.cs to update the LoanExtensionStatus dictionary in the EnumHelper class. Provide the updated code for the LoanExtensionStatus dictionary in the EnumHelper class.
    ```

    Verwenden Sie bei Bedarf denselben Ansatz für die Aufzählungen „LoanReturnStatus“ und „MembershipRenewalStatus“.

1. Nehmen Sie sich eine Minute Zeit, um die **GetDescription**-Methode zu überprüfen.

    ```csharp

    public static string GetDescription(Enum value)
    {
        if (value == null)
            return string.Empty;
        return value switch
        {
            MembershipRenewalStatus status => MembershipRenewalStatusDescriptions[status],
            LoanReturnStatus status => LoanReturnStatusDescriptions[status],
            LoanExtensionStatus status => LoanExtensionStatusDescriptions[status],
            _ => value.ToString()
        };
    }

    ```

    Dieser Code verwendet den Musterabgleich, um den Typ der Enumeration zu bestimmen und die Beschreibung aus dem entsprechenden Wörterbuch abzurufen. Die „switch“-Anweisung überprüft den Typ des Aufzählungswerts und gibt die entsprechende Beschreibung aus dem Wörterbuch zurück. Wenn der Enumerationswert im Wörterbuch nicht gefunden wird, gibt die Methode den Enumerationswert als Zeichenfolge zurück.

    Wenn Sie GitHub Copilot auffordern, diesen Code umzugestalten und die Lambdaausdrücke zu entfernen, kann er einfacher gelesen werden:

    ```csharp

    public static string GetDescription(Enum value)
    {
        if (value == null)
            return string.Empty;
        switch (value)
        {
            case MembershipRenewalStatus status:
                return MembershipRenewalStatusDescriptions[status];
            case LoanReturnStatus status:
                return LoanReturnStatusDescriptions[status];
            case LoanExtensionStatus status:
                return LoanExtensionStatusDescriptions[status];
            default:
                return value.ToString();
        }
    }

    ```

1. Speichern Sie die Änderungen in Ihrer EnumHelper.cs-Datei.

1. Erstellen Sie Ihre Lösung so, dass keine Fehler auftreten.

    Es werden Warnungen angezeigt. Sie können sie vorerst ignorieren.

#### Zusammenfassung - der Übung 8

In dieser Übung haben Sie GitHub Copilot verwendet, um die EnumHelper-Klasse so umzugestalten, dass sie Wörterbücher anstelle von Spiegelungen verwendet. Durch das Verwenden von Wörterbüchern wird die Leistung verbessert, indem der Mehraufwand der Reflexion reduziert wird. Das Entfernen der Reflexion verbessert auch die Lesbarkeit, Wartungsfreundlichkeit und Sicherheit von Code.

### Übung 9: Verwenden von GitHub Copilot, um die Datenzugriffsklassen mit LINQ zu verbessern

LINQ (Language Integrated Query) ist ein leistungsfähiges Feature in C#, mit dem Sie Sammlungen, Datenbanken und XML-Dokumente einheitlich abfragen können. LINQ bietet im Vergleich zu herkömmlichen foreach-Schleifen eine präzisere und besser lesbare Möglichkeit zum Abfragen von Daten.

Diese Übung umfasst die folgenden Aufgaben:

- Gestalten Sie zum Verwenden von LINQ die Methoden in JsonData.cs um.
- Gestalten Sie zum Verwenden von LINQ die Methoden in JsonLoanRepository.cs um.
- Gestalten Sie zum Verwenden von LINQ die Methoden in JsonPatronRepository.cs um.

#### Aufgabe 1: Umgestalten der Methoden in JsonData.cs zum Verwenden von LINQ

Die JsonData-Klasse enthält die folgenden Datenzugriffsmethoden: GetPopulatedPatron, GetPopulatedLoan, GetPopulatedBookItem und GetPopulatedBook. Diese Methoden verwenden foreach-Schleifen, um Sammlungen zu durchlaufen und Objekte aufzufüllen. Sie können diese Methoden zum Verwenden von LINQ umgestalten, um die Lesbarkeit und Wartungsfreundlichkeit von Code zu verbessern.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Datei „JsonData.cs“.

1. Wählen Sie die **GetPopulatedPatron**-Methode aus.

    Die Methode GetPopulatedPatron dient dazu, ein vollständig ausgefülltes Patron-Objekt zu erstellen. Sie kopiert die grundlegenden Eigenschaften des Patrons und füllt ihre Ausleihsammlung mit detaillierten Ausleihobjekten.

    ```csharp

    public Patron GetPopulatedPatron(Patron p)
    {
        Patron populated = new Patron
        {
            Id = p.Id,
            Name = p.Name,
            ImageName = p.ImageName,
            MembershipStart = p.MembershipStart,
            MembershipEnd = p.MembershipEnd,
            Loans = new List<Loan>()
        };
        foreach (Loan loan in Loans!)
        {
            if (loan.PatronId == p.Id)
            {
                populated.Loans.Add(GetPopulatedLoan(loan));
            }
        }
        return populated;
    }

    ```

1. Öffnen Sie einen Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    ```plaintext
    #selection refactor selection to `return new Patron` using LINQ
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public Patron GetPopulatedPatron(Patron p)
    {
        return new Patron
        {
            Id = p.Id,
            Name = p.Name,
            ImageName = p.ImageName,
            MembershipStart = p.MembershipStart,
            MembershipEnd = p.MembershipEnd,
            Loans = Loans!
                .Where(loan => loan.PatronId == p.Id)
                .Select(GetPopulatedLoan)
                .ToList()
        };
    }

    ```

    Zunächst wird eine LINQ-Abfrage verwendet, um die „foreach (Ausleihobjekt ausleihen in Ausleihevorgang!)“-Schleife zu ersetzen. Wenn der LINQ-Code vorhanden ist, können Sie einen Objektinitialisierer verwenden, um dem neuen Patron-Objekt Objekteigenschaften zuzuweisen. Dadurch wird die Notwendigkeit einer separaten ausgefüllten Instanz des Patron-Objekts verringert. Insgesamt ist der aktualisierte Code kürzer und besser lesbar.

    Der Code verwendet den Eingabe-Patron „p“, um dem neuen Patron-Objekt einige grundlegende Eigenschaften zuzuweisen. Anschließend wird die Ausleihe-Auflistung mit den Ausleihen gefüllt, die den eingegebenen Benutzenden zugeordnet sind, und jede Ausleihe wird mithilfe der Methode „GetPopulatedLoan“ umgewandelt.

    Sie können die LINQ-Codezeile aufschlüsseln, die die Ausleihe-Auflistung füllt:

    - `Loans!`: Die "Ausleihevorgänge!" Expressions greift auf die Ausleihe-Auflistung zu. Der „!“-Operator ist ein Null-toleranter Operator, der angibt, dass der Entwickler sicher ist, dass der Wert bei den Ausleihevorgängen nicht null ist. Sie sollten sicherstellen, dass die Ausleihevorgänge ordnungsgemäß initialisiert sind, bevor Sie die GetPopulatedPatron-Methode aufrufen.
    - `.Where(loan => loan.PatronId == p.Id)`: Dieser Code filtert die Ausleihevorgänge, um nur diejenigen einzuschließen, die zu dem Eingabe-Patron „p“ gehören.
    - `.Select(GetPopulatedLoan)`: Dieser Code transformiert jedes gefilterte Ausleih-Element mithilfe der GetPopulatedLoan-Methode.
    - `.ToList()`: Konvertiert das Ergebnis in eine Liste von Ausleihobjekten.

1. Um das vorgeschlagene Update zu akzeptieren, wählen Sie **Annehmen** aus.

    Nachdem Sie nun gesehen haben, wie die GetPopulatedPatron-Methode umgestaltet werden kann, können Sie die Methoden GetPopulatedLoan, GetPopulatedBookItem und GetPopulatedBook so umgestalten, dass auch diese LINQ verwenden.

1. Überarbeiten Sie die Methoden **GetPopulatedLoan**, **GetPopulatedBookItem** und **GetPopulatedBook** nach demselben Ansatz.

    Verwenden Sie beispielsweise die folgenden Prompts, um die drei Methoden umzugestalten:

    Für die **GetPopulatedLoan**-Methode:

    ```plaintext
    #selection refactor selection to `return new Loan` using LINQ. Use `GetPopulatedBookItem` for the `BookItem` property. Use `Single` for BookItem and Patron properties.
    ```

    Für die **GetPopulatedBookItem**-Methode:

    ```plaintext
    #selection refactor selection to `return new BookItem` using LINQ. Use `GetPopulatedBook` and `Single` for the `BookItem` property.
    ```

    Für die **GetPopulatedBook**-Methode:

    ```plaintext
    #selection refactor selection to `return new Book` using LINQ. Use `Where` and `Select` for `Author` property. Use `First` author.
    ```

1. Nachdem Sie die vorgeschlagenen Updates akzeptiert haben, nehmen Sie sich einen Moment Zeit, um Ihre Codeänderungen zu überprüfen.

    Ihr aktualisierter Code sollte dem folgenden Code ähneln:

    ```csharp

    public Loan GetPopulatedLoan(Loan l)
    {
        return new Loan
        {
            Id = l.Id,
            BookItemId = l.BookItemId,
            PatronId = l.PatronId,
            LoanDate = l.LoanDate,
            DueDate = l.DueDate,
            ReturnDate = l.ReturnDate,
            BookItem = GetPopulatedBookItem(BookItems!.Single(bi => bi.Id == l.BookItemId)),
            Patron = Patrons!.Single(p => p.Id == l.PatronId)
        };
    }
    public BookItem GetPopulatedBookItem(BookItem bi)
    {
        return new BookItem
        {
            Id = bi.Id,
            BookId = bi.BookId,
            AcquisitionDate = bi.AcquisitionDate,
            Condition = bi.Condition,
            Book = GetPopulatedBook(Books!.Single(b => b.Id == bi.BookId))
        };
    }
    public Book GetPopulatedBook(Book b)
    {
        return new Book
        {
            Id = b.Id,
            Title = b.Title,
            AuthorId = b.AuthorId,
            Genre = b.Genre,
            ISBN = b.ISBN,
            ImageName = b.ImageName,
            Author = Authors!.Where(a => a.Id == b.AuthorId).Select(a => new Author {
                Id = a.Id,
                Name = a.Name
            }).First()
        };
    }

    ```

1. Verwenden Sie die intelligente Aktion **Erklären**, um eine Erklärung der LINQ-Abfragen anzuzeigen.

    Die intelligente Aktion **Explain** bietet eine detaillierte Erklärung der im Code verwendeten LINQ-Abfragen.

    Sie können beispielsweise die intelligente Aktion **Explain** auf die Methode „GetPopulatedBook“ anwenden, um eine Erklärung der LINQ-Abfrage zu erhalten, die zum Auffüllen der Eigenschaft „Author“ des Buchobjekts verwendet wird.

    ```csharp

    Author = Authors!.Where(a => a.Id == b.AuthorId).Select(a => new Author {
        Id = a.Id,
        Name = a.Name
    }).First()

    ```

    Die intelligente Aktion **Explain** bietet eine detaillierte Erklärung der LINQ-Abfrage, die zum Auffüllen der Eigenschaft Autor des Buchobjekts verwendet wird.

    Die Erklärung könnte z. B. wie folgt aussehen:

    ```plaintext
    The active selection is a C# code snippet that assigns a value to the Author property. This value is derived from a collection of Author objects named Authors. The code uses LINQ (Language Integrated Query) to filter and transform the data within this collection.
    
    First, the Authors! expression uses the null-forgiving operator (!) to indicate that Authors is not null, even if the compiler might think otherwise. This is a way to suppress nullable warnings. The Where method is then called on the Authors collection to filter the elements. The lambda expression a => a.Id == b.AuthorId is used to find all Author objects where the Id matches the AuthorId property of another object b.
    
    After filtering, the Select method is used to project each filtered Author object into a new Author object. This is done by creating a new instance of the Author class and copying the Id and Name properties from the original Author object.
    
    Finally, the First method is called to retrieve the first element from the resulting sequence. This means that the Author property will be assigned the first Author object that matches the filter criteria and has been projected into a new Author instance.
    
    This approach ensures that the Author property is set to a new Author object with the same Id and Name as the first matching Author in the Authors collection.
    ```

1. Speichern Sie die Änderungen in der JsonData.cs-Datei.

1. Erstellen Sie Ihre Lösung so, dass keine Fehler auftreten.

    Es werden Warnungen angezeigt. Sie können sie vorerst ignorieren.

#### Aufgabe 2: Umgestalten der Methoden in JsonLoanRepository.cs zum Verwenden von LINQ

Die JsonLoanRepository-Klasse enthält die Datenzugriffsmethoden GetLoan und UpdateLoan. Sie gestalten diese beiden Methoden um, indem Sie foreach-Schleifen durch LINQ ersetzen, um die Lesbarkeit und Wartungsfreundlichkeit von Code zu verbessern.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die Datei **JsonLoanRepository.cs**.

1. Wählen Sie die **GetLoan**-Methode aus.

    Die GetLoan-Methode dient dazu, einen Ausleihvorgang anhand seiner ID abzurufen.

    ```csharp

    public async Task<Loan?> GetLoan(int id)
    {
        await _jsonData.EnsureDataLoaded();
        foreach (Loan loan in _jsonData.Loans!)
        {
            if (loan.Id == id)
            {
                Loan populated = _jsonData.GetPopulatedLoan(loan);
                return populated;
            }
        }
        return null;
    }

    ```

1. Öffnen Sie den Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    Geben Sie beispielsweise die folgende Eingabeaufforderung ein:

    ```plaintext
    #selection refactor selection using LINQ with `_jsonData.Loans!. Use `Where`, `Select` and `GetPopulatedLoan` to return `FirstOrDefault`.
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public async Task<Loan?> GetLoan(int id)
    {
        await _jsonData.EnsureDataLoaded();
        Loan? loan = _jsonData.Loans!
            .Where(l => l.Id == id)
            .Select(l => _jsonData.GetPopulatedLoan(l))
            .FirstOrDefault();
        return loan;
    }

    ```

    Der aktualisierte Code verwendet LINQ, um die Loan-Sammlung so zu filtern, dass nur das Loan-Element mit der angegebenen ID enthalten ist. Beachten Sie, dass das ein Ausleihevorgang als kündbar (`Loan? loan`) deklariert werden sollte. Anschließend wird der Ausleihevorgang mithilfe der GetPopulatedLoan-Methode umgewandelt und das erste Ergebnis zurückgegeben. Wenn kein passender Ausleihevorgang gefunden wird, gibt FirstOrDefault null zurück. Die Methode gibt dann dieses Ausleiheobjekt zurück, das null sein kann, wenn kein Ausleihvorgang mit der angegebenen „ID“ existiert. Mit diesem Ansatz wird sichergestellt, dass das zurückgegebene Loan-Element vollständig mit allen erforderlichen dazugehörigen Daten aufgefüllt wird und einen umfassenden Überblick über den Loan-Datensatz bietet.

    Dieser Code könnte weiter vereinfacht werden:

    ```csharp

    public async Task<Loan?> GetLoan(int id)
    {
        await _jsonData.EnsureDataLoaded();
        return _jsonData.Loans!
            .Where(l => l.Id == id)
            .Select(l => _jsonData.GetPopulatedLoan(l))
            .FirstOrDefault();
    }

    ```

1. Um die aktualisierte GetLoan-Methode zu akzeptieren, klicken Sie auf **Annehmen**.

1. Wählen Sie die **UpdateLoan**-Methode aus.

    ```csharp

    public async Task UpdateLoan(Loan loan)
    {
        Loan? existingLoan = null;
        foreach (Loan l in _jsonData.Loans!)
        {
            if (l.Id == loan.Id)
            {
                existingLoan = l;
                break;
            }
        }
        if (existingLoan != null)
        {
            existingLoan.BookItemId = loan.BookItemId;
            existingLoan.PatronId = loan.PatronId;
            existingLoan.LoanDate = loan.LoanDate;
            existingLoan.DueDate = loan.DueDate;
            existingLoan.ReturnDate = loan.ReturnDate;
            await _jsonData.SaveLoans(_jsonData.Loans!);
            await _jsonData.LoadData();
        }
    }

    ```

1. Öffnen Sie den Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    Geben Sie beispielsweise die folgende Eingabeaufforderung ein:

    ```plaintext
    #selection refactor selection using LINQ find an existing loan `_jsonData.Loans!. Replace existing loan.
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public async Task UpdateLoan(Loan loan)
    {
        Loan? existingLoan = _jsonData.Loans!.FirstOrDefault(l => l.Id == loan.Id);
        if (existingLoan != null)
        {
            existingLoan.BookItemId = loan.BookItemId;
            existingLoan.PatronId = loan.PatronId;
            existingLoan.LoanDate = loan.LoanDate;
            existingLoan.DueDate = loan.DueDate;
            existingLoan.ReturnDate = loan.ReturnDate;
            await _jsonData.SaveLoans(_jsonData.Loans!);
            await _jsonData.LoadData();
        }
    }

    ```

    Der aktualisierte Code verwendet LINQ, um das vorhandene Loan-Element in der Loan-Sammlung zu finden. Anschließend wird das vorhandene Loan-Element mit den neuen Loan-Daten aktualisiert. Dann wird die aktualisierte Loan-Sammlung mit der Methode gespeichert, und die Daten werden neu geladen. Mit diesem Ansatz wird sichergestellt, dass die Loan-Daten korrekt aktualisiert werden und dass die Änderungen am Datenspeicher beibehalten werden.

    Sie können den Code auch hinzufügen, um sicherzustellen, dass die Daten geladen werden, bevor die Methode ausgeführt wird:

    ```csharp

    public async Task UpdateLoan(Loan loan)
    {
        await _jsonData.EnsureDataLoaded();
        Loan? existingLoan = _jsonData.Loans!.FirstOrDefault(l => l.Id == loan.Id);
        if (existingLoan != null)
        {
            existingLoan.BookItemId = loan.BookItemId;
            existingLoan.PatronId = loan.PatronId;
            existingLoan.LoanDate = loan.LoanDate;
            existingLoan.DueDate = loan.DueDate;
            existingLoan.ReturnDate = loan.ReturnDate;
            await _jsonData.SaveLoans(_jsonData.Loans!);
            await _jsonData.LoadData();
        }
    }

    ```

1. Um die aktualisierte UpdateLoan-Methode zu akzeptieren, wählen Sie **Annehmen** aus.

1. Speichern Sie Ihre Änderungen in der JsonLoanRepository.cs-Datei.

1. Erstellen Sie Ihre Lösung so, dass keine Fehler auftreten.

    Es werden Warnungen angezeigt. Sie können sie vorerst ignorieren.

#### Aufgabe 3: Umgestalten der Methoden in JsonPatronRepository.cs zur Verwendung von LINQ

Die JsonPatronRepository-Klasse enthält die Methoden SearchPatrons, GetPatron und UpdatePatron und eignet sich hervorragend für eine Optimierung. Sie gestalten diese Methoden um, indem Sie foreach-Schleifen durch LINQ ersetzen, um die Lesbarkeit und Wartungsfreundlichkeit von Code zu verbessern.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Übung zu absolvieren:

1. Öffnen Sie die **JsonPatronRepository.cs**-Datei.

1. Wählen Sie die **SearchPatrons**-Methode aus.

    Die Methode SearchPatrons dient der Suche nach Patrons anhand ihres Namens.

    ```csharp

    public async Task<List<Patron>> SearchPatrons(string searchInput)
    {
        await _jsonData.EnsureDataLoaded();
        List<Patron> searchResults = new List<Patron>();
        foreach (Patron patron in _jsonData.Patrons)
        {
            if (patron.Name.Contains(searchInput))
            {
                searchResults.Add(patron);
            }
        }
        searchResults.Sort((p1, p2) => String.Compare(p1.Name, p2.Name));
        searchResults = _jsonData.GetPopulatedPatrons(searchResults);
        return searchResults;
    }

    ```

1. Öffnen Sie den Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    Geben Sie beispielsweise die folgende Eingabeaufforderung ein:

    ```plaintext
    #selection refactor selection using LINQ with `_jsonData.Patrons!. Replace the loop with `Where`, `OrderBy`, and `GetPopulatedPatrons`.
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public async Task<List<Patron>> SearchPatrons(string searchInput)
    {
        await _jsonData.EnsureDataLoaded();
        List<Patron> searchResults = _jsonData.Patrons!
            .Where(patron => patron.Name.Contains(searchInput))
            .OrderBy(patron => patron.Name)
            .ToList();
        searchResults = _jsonData.GetPopulatedPatrons(searchResults);
        return searchResults;
    }

    ```

1. Um die aktualisierte SearchPatrons-Methode zu akzeptieren, wählen Sie **Annehmen**aus.

1. Wählen Sie die **GetPatron**-Methode aus.

    Die GetPatron-Methode ist so konzipiert, dass das Patron-Element zurückgegeben wird, das der angegebenen „ID" entspricht.

    ```csharp

    public async Task<Patron?> GetPatron(int id)
    {
        await _jsonData.EnsureDataLoaded();
        foreach (Patron patron in _jsonData.Patrons!)
        {
            if (patron.Id == id)
            {
                Patron populated = _jsonData.GetPopulatedPatron(patron);
                return populated;
            }
        }
        return null;
    }

    ```

1. Öffnen Sie den Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    Geben Sie beispielsweise die folgende Eingabeaufforderung ein:

    ```plaintext
    #selection refactor selection using LINQ with `_jsonData.Patrons!. Use `Where`, `Select` and `GetPopulatedPatron` to return `FirstOrDefault`
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public async Task<Patron?> GetPatron(int id)
    {
        await _jsonData.EnsureDataLoaded();
        var patron = _jsonData.Patrons!
            .Where(p => p.Id == id)
            .Select(p => _jsonData.GetPopulatedPatron(p))
            .FirstOrDefault();
        return patron;
    }

    ```

    Dieser Code könnte weiter vereinfacht werden:

    ```C#

    public async Task<Patron?> GetPatron(int id)
    {
        await _jsonData.EnsureDataLoaded();
        return _jsonData.Patrons!
            .Where(p => p.Id == id)
            .Select(p => _jsonData.GetPopulatedPatron(p))
            .FirstOrDefault();
    }

    ```

1. Um die aktualisierte GetPatron-Methode zu akzeptieren, wählen Sie **Annehmen** aus.

1. Wählen Sie die **UpdatePatron**-Methode aus.

    Die UpdatePatron-Methode dient dazu, den Benutzer mit der angegebenen „ID“ zu aktualisieren.

    ```csharp

    public async Task UpdatePatron(Patron patron)
    {
        await _jsonData.EnsureDataLoaded();
        var patrons = _jsonData.Patrons!;
        Patron existingPatron = null;
        foreach (var p in patrons)
        {
            if (p.Id == patron.Id)
            {
                existingPatron = p;
                break;
            }
        }
        if (existingPatron != null)
        {
            existingPatron.Name = patron.Name;
            existingPatron.ImageName = patron.ImageName;
            existingPatron.MembershipStart = patron.MembershipStart;
            existingPatron.MembershipEnd = patron.MembershipEnd;
            existingPatron.Loans = patron.Loans;
            await _jsonData.SavePatrons(patrons);
            await _jsonData.LoadData();
        }
    }

    ```

1. Öffnen Sie den Inline-Chat, und geben Sie dann einen Prompt ein, durch den die Methode mit LINQ umgestaltet wird.

    Geben Sie beispielsweise die folgende Eingabeaufforderung ein:

    ```plaintext
    #selection refactor selection using LINQ to find `patron` in `_jsonData.Patrons!. Replace existing patron with `patron`.
    ```

1. Nehmen Sie sich einen Moment Zeit, um das vorgeschlagene Update zu überprüfen.

    Das vorgeschlagene Update sollte dem folgenden Code ähneln:

    ```csharp

    public async Task UpdatePatron(Patron patron)
    {
        await _jsonData.EnsureDataLoaded();
        var patrons = _jsonData.Patrons!;
        var existingPatron = patrons.FirstOrDefault(p => p.Id == patron.Id);
        if (existingPatron != null)
        {
            existingPatron.Name = patron.Name;
            existingPatron.ImageName = patron.ImageName;
            existingPatron.MembershipStart = patron.MembershipStart;
            existingPatron.MembershipEnd = patron.MembershipEnd;
            existingPatron.Loans = patron.Loans;
            await _jsonData.SavePatrons(patrons);
            await _jsonData.LoadData();
        }
    }

    ```

1. Um die aktualisierte UpdatePatron-Methode zu akzeptieren, wählen Sie **Annehmen** aus.

#### Aufgabe 4: Überprüfen Ihrer Arbeit

Führen Sie die folgenden Schritte aus, um Ihre Arbeit zu überprüfen:

1. Um die Lösung zu bereinigen, klicken Sie mit der rechten Maustaste auf **AccelerateAppDevGitHubCopilot** und wählen Sie dann **Bereinigen** aus.

    Mit dieser Aktion werden alle Buildartefakte des vorherigen Build entfernt. Durch das Bereinigen der Lösung werden die JSON-Datendateien währenddessen im Ausgabeverzeichnis effektiv auf ihre ursprünglichen Werte zurückgesetzt.

1. Erstellen Sie die Anwendung, und stellen Sie sicher, dass keine Fehler vorhanden sind.

1. Führen Sie die Anwendung aus.

    Sie können die Anwendung über die Ansicht „Projektmappen-Explorer“ ausführen, indem Sie mit der rechten Maustaste auf das Projekt **Library.Console** klicken und dann **Debug** und dann **Neue Instanz starten** auswählen.

1. Wenn Sie zur Eingabe eines Patron-Namens aufgefordert werden, geben Sie **One** ein, und drücken Sie dann die EINGABETASTE.

1. Geben Sie bei der Eingabeaufforderung "Matching Patrons" **2** ein, und drücken Sie dann die EINGABETASTE.

1. Geben Sie bei der Eingabeaufforderung "Book Loans" **1** ein, und drücken Sie dann die EINGABETASTE.

1. Geben Sie bei der Eingabeaufforderung "Input Options" **r** ein, und drücken Sie dann die EINGABETASTE.

1. Überprüfen Sie, ob die Meldung lautet: **„Buch wurde erfolgreich zurückgegeben“**. angezeigt.

1. Um eine neue Suche zu beginnen, geben Sie **s** ein, und drücken Sie dann die EINGABETASTE.

1. Wenn Sie zur Eingabe eines Patron-Namens aufgefordert werden, geben Sie **One** ein, und drücken Sie dann die EINGABETASTE.

1. Geben Sie bei der Eingabeaufforderung "Matching Patrons" **2** ein, und drücken Sie dann die EINGABETASTE.

1. Überprüfen Sie, ob die erste Buchausleihe als **Zurückgegeben: Wahr** markiert ist.

1. Geben Sie bei der Eingabeaufforderung "Input Options" **q** ein, und drücken Sie dann die EINGABETASTE.

1. Beenden Sie die Anwendung.

#### Zusammenfassung - der Übung 9

In dieser Übung haben Sie die Datenzugriffsmethoden in den Klassen JsonData, JsonLoanRepository und JsonPatronRepository für die Verwendung von LINQ umgestaltet. Diese Änderungen verbessern die Lesbarkeit, Wartbarkeit und Leistung des Codes.
