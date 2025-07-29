---
demo:
  title: 'Demo: Verbessern der Codequalität mithilfe von GitHub Copilot Chat'
  module: 'Module 5: Implement code improvements using GitHub Copilot tools'
---

# Demo: Verbessern der Codequalität mithilfe von GitHub Copilot Chat

## Anweisungen

Die Aktivitäten der Demo sind für eine Umgebung konzipiert, die die folgenden Ressourcen umfasst:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Der Begriff „Codequalität“ bezieht sich auf die Gesamtqualität der Codebasis, einschließlich Lesbarkeit, Wartbarkeit und Modularität. Die Codequalität ist ein Maß dafür, wie „gut strukturiert“ Ihr Code ist und wie leicht er verstanden, gewartet und erweitert werden kann.

> [!IMPORTANT]
> Erläutern Sie den Kursteilnehmenden, dass es in dieser Demo nicht um bewährte Methoden für die Entwicklung von qualitativ hochwertigem Code geht. Stattdessen geht es darum, wie man den GitHub Copilot Chat nutzt, um Vorschläge zur Verbesserung der Codequalität in einer Beispielanwendung zu generieren. Die Vorschläge stellen keine bewährten Methoden oder umfassende Lösungen für die Entwicklung von erstklassigem Code dar. Fachkräfte in der Entwicklung sollten die Vorschläge des GitHub Copilot Chats nach eigenem Ermessen und mit eigenem Fachwissen bewerten und umsetzen. Wenn Sie Vorschläge von GitHub Copilot implementieren, heißt das nicht, dass keine gründlichen Codeüberprüfungen und Tests mehr erforderlich sind.

In den folgenden Abschnitten finden Sie eine Übersicht über die Codeumgestaltung und die Codequalität, die Ihre Kursteilnehmenden beachten sollten.

#### Coderefactoring und qualitativ hochwertiger Code

Coderefactoring ist der Prozess der Umstrukturierung von bestehendem Code, ohne dessen äußeres Verhalten zu ändern. Ziel des Coderefactorings ist es, die interne Struktur der Codebasis zu verbessern, damit sie leichter zu verstehen, zu pflegen und zu erweitern ist. Coderefactoring kann Ihnen helfen, hochwertigen Code zu schreiben, indem es die Lesbarkeit erhöht, die Komplexität reduziert, die Modularität verbessert und die Wiederverwendbarkeit erhöht. Jeder dieser Faktoren trägt dazu bei, eine besser verwaltbare und wartbare Codebasis zu schaffen.

Fachkräfte in der Entwicklung sollten die folgenden Faktoren berücksichtigen, wenn sie an der Verbesserung der Codequalität arbeiten:

- Lesbarkeit: Durch Verbesserung oder Optimierung der Lesbarkeit von Code kann das Verständnis für Fachkräfte in der Entwicklung erleichtern.
- Komplexität: Durch die Reduzierung der Codekomplexität wird der Code leichter verständlich, verwaltbar und wartbar.
- Modularität und Wiederverwendbarkeit: Die Aufteilung des Codes in kleinere, wiederverwendbare Module oder Komponenten kann die Verwaltung und Wartung des Codes erleichtern.

Die oben aufgeführten Faktoren stellen drei Bereiche dar, die von Fachkräften in der Entwicklung häufig genannt werden, wenn es um Codequalität geht. Weitere Faktoren, die mit der Codequalität in Verbindung gebracht werden können, sind:

- Prüfbarkeit: Die Leichtigkeit, mit der der Code getestet werden kann, um sicherzustellen, dass er korrekt funktioniert. Oft ein Nebenprodukt von gutem Design und Modularität.
- Erweiterbarkeit: Die Leichtigkeit, mit der der Code erweitert oder verbessert werden kann, um neue Merkmale oder Funktionen hinzuzufügen. Oft ein Nebenprodukt von gutem Design und Modularität.

Die Codequalität ist nicht der einzige Faktor, den Fachkräfte in der Entwicklung bei der Codeüberprüfung berücksichtigen. Hier sind einige weitere Faktoren, die Fachkräfte in der Entwicklung häufig zusätzlich zur Codequalität bewerten:

- Zuverlässigkeit: Die Eignung des Codes, seine beabsichtigten Funktionen unter bestimmten Bedingungen zu erfüllen.
- Leistung: Wie effizient der Code ausgeführt wird.
- Sicherheit: Die Eignung des Codes, Daten und Ressourcen vor unbefugtem Zugriff oder Veränderung zu schützen.
- Skalierbarkeit: Die Eignung des Codes zur Bewältigung einer erhöhten Workload oder eines zukünftigen Wachstums.
- Benutzerfreundlichkeit: Die Leichtigkeit, mit der der Code von Fachkräften in der Entwicklung oder von benutzenden Personen verwendet werden kann.
- Portabilität: Die Eignung des Codes, auf verschiedenen Plattformen oder Umgebungen zu laufen.

> [!NOTE]
> Die nächsten beiden Einheiten dieses Moduls behandeln die Verbesserung der Zuverlässigkeit, Leistung und Sicherheit von Code mithilfe von GitHub Copilot Chat.

Die Verbesserung der Codequalität wird oft als Vorläufer für das Hinzufügen neuer Funktionen oder Erweiterungen angesehen. Sie sollten Verbesserungen der Codequalität in Betracht ziehen, bevor Sie an der Zuverlässigkeit, Leistung oder Sicherheit des Codes arbeiten.

In dieser Demo verwenden Sie GitHub Copilot Chat, um Vorschläge zur Verbesserung der Codequalität in einer Beispielanwendung zu generieren.

### Entwickeln von Prompts für GitHub Copilot Chat

Wiederholen Sie die Bedeutung der Erstellung guter Prompts.

Die Prompt, die Sie für GitHub Copilot Chat schreiben, sollten klar definierten *Kontext* und *Absicht* haben. Unter *Absicht* des Prompts wird das Ziel verstanden, das Sie erreichen möchten. Sie können GitHub Copilot zum Beispiel bitten, „Refactoring durchzuführen, um die Modularität des Codes zu verbessern“. Der *Kontext* des Prompts teilt GitHub Copilot mit, welche Ressourcen berücksichtigt werden sollen. Sie möchten beispielsweise, dass GitHub Copilot den gesamten Arbeitsbereich betrachtet, sich aber auf eine bestimmte Datei oder einen Codeabschnitt konzentriert. Berücksichtigen Sie bei der Entwicklung Ihrer Prompts die folgenden Vorschläge:

- Definieren Sie einen äußeren Kontext, der auf einer höheren Ebene angesiedelt ist als der Code, den Sie aktualisieren möchten. Wenn Sie zum Beispiel eine Methode umgestalten wollen, geben Sie die Klasse oder Datei, die die Methode enthält, als äußeren Kontext an. Identifizieren Sie die Methode als einen inneren Kontext.
- Verwenden Sie Chatteilnehmer und Chatvariablen, um den Kontext anzugeben. Sie können die Chat-Variablen `#file:` und `#selection` verwenden, um den spezifischen Code zu identifizieren, auf den Sie sich konzentrieren. Gegebenenfalls können Sie auch den gesamten Arbeitsbereich (`@workspace`) angeben. Angenommen, Sie wollen eine Methode in einer bestimmten Datei überarbeiten. Sie können die Chatvariable `#file:` verwenden, um GitHub Copilot mitzuteilen, welche Datei er betrachten soll. Sie können die Methode im Editor auswählen und die Chatvariable `#selection` verwenden, um GitHub Copilot mitzuteilen, welchen Code Sie umgestalten möchten. Sie können auch die Chatvariable `@workspace` verwenden, um GitHub Copilot anzuweisen, den gesamten Arbeitsbereich zu berücksichtigen. Verdeutlichen Sie den angegebenen Kontext, indem Sie sich im natürlichsprachlichen Teil Ihres Prompts auf die Auswahl oder die Datei beziehen. Sie könnten zum Beispiel fragen: „Wie kann ich die Lesbarkeit des ausgewählten Codes verbessern?“
- Die Absicht sollte klar und deutlich sein und den Aspekt der Codequalität angeben, den Sie verbessern möchten. Sie könnten zum Beispiel GitHub Copilot Chat fragen: „Wie kann ich die Modularität des ausgewählten Codes verbessern“.

Während dieses Teils der Demo überprüfen Sie das Projekt **APL2007M5BankAccount** und erstellen drei Prompts für GitHub Copilot Chat. Die Prompts zielen darauf ab, die Lesbarkeit des Codes, die Wartbarkeit und die Modularität zu verbessern.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie die Beispielanwendung **APL2007M5BankAccount** in Visual Studio Code.

1. Öffnen Sie die Datei **Program.cs**, und überprüfen Sie den Code.

    Dieses Programm ist eine Konsolenanwendung, die ein Bankensystem simuliert. Hier sind die wichtigsten Features:

    - Main-Methode: Die Main-Methode ist der Einstiegspunkt der Anwendung. Sie erstellt Bankkonten und verwendet diese, um Transaktionen zu simulieren.

    - Konstanten: Das Programm definiert mehrere Konstanten am Anfang der Klasse „Program“. Zu den Konstanten gehören z. B. die Anzahl der zu erstellenden Konten, die Anzahl der zu simulierenden Transaktionen und die Transaktionsgrenzwerte.

1. Nehmen Sie sich eine Minute Zeit, um einige Prompts zu schreiben, die Sie verwenden können, um die Lesbarkeit, Wartung und Modularität von Code zu verbessern.

    Für das BankAccount-Projekt sollten Sie die Dateien BankAccount.cs und/oder Program.cs an den Chatkontext anfügen. Ihre Prompts könnten den folgenden Beispielen ähneln:

    Prompt: `@workspace /explain How can I improve the readability of the [selected code]?`

    Prompt: `@workspace /explain #selection How can I improve the maintainability of the [selected code]?`

    Prompt: `@workspace /explainHow can I improve the modularity of the [selected code]?`

    Prompt: `#selection How can I refactor the [selected code] to improve modularity?`

    Prompt: `@workspace /explain What are some options for simplifying the [selected code]?`

1. Erstellen Sie drei Prompts, die Sie im weiteren Verlauf der Demo verwenden können.

### Umgestalten Ihres Codes mit GitHub Copilot Chat

Sie können den GitHub Copilot Chat nutzen, um Codeaktualisierungen vorzuschlagen, die Ihren Code umgestalten und verbessern. Es ist wichtig, dass Sie Ihren Code und Ihre Ziele verstehen, bevor Sie eine Entscheidung über das Refactoring der Anwendung treffen.

Die Vorschläge, die GitHub Copilot Chat bietet, müssen sorgfältig überprüft werden. Überlegen Sie, welche Vorschläge Ihre Ziele unterstützen, bevor Sie sie implementieren. Für die Zwecke dieser Demo kann Ihre Zeit auch ein Faktor bei der Entscheidung sein, welche Vorschläge umgesetzt werden sollen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Nehmen Sie sich eine Minute Zeit, um die in der Datei „Program.cs“ beinhalteten Methoden zu überprüfen.

    - CreateBankAccounts-Methode: Diese Methode erstellt eine bestimmte Anzahl von Bankkonten mit zufälligen Anfangsguthaben, Kontoinhabernamen, Kontotypen und Eröffnungsterminen. Sie verwendet einen Try-Catch-Block, um ausnahmen zu behandeln, die während der Kontoerstellung auftreten können.

    - SimulateTransactions-Methode: Diese Methode simuliert eine bestimmte Anzahl von Transaktionen in einer Liste von Bankkonten. Sie generiert einen zufälligen Transaktionsbetrag für jede Transaktion und belastet dann das Konto mit diesem Betrag, je nachdem, ob der Betrag positiv oder negativ ist. Sie verwendet einen Try-Catch-Block, um ausnahmen zu behandeln, die während der Transaktionen auftreten können.

    - SimulateTransfers-Methode: Diese Methode ist identisch mit der SimulateTransactions-Methode. Sie soll anscheinend Überweisungen zwischen Konten simulieren, derzeit simuliert sie jedoch nur Transaktionen auf einzelnen Konten.

    - GenerateRandomDollarAmount-Methode: Diese Methode generiert einen zufälligen Dollarbetrag innerhalb eines angegebenen Bereichs. Sie verwendet eine andere Formel, um den Betrag zu generieren, je nachdem, ob der Betrag für einen Kontostand oder eine Transaktion ist.

    - GenerateRandomAccountHolder-Methode: Diese Methode wählt einen zufälligen Kontoinhabernamen aus einer vordefinierten Liste von Namen aus.

    - GenerateRandomAccountType-Methode: Diese Methode wählt einen zufälligen Kontotyp aus einer vordefinierten Liste von Typen aus.

    - GenerateRandomDateOpened-Methode: Diese Methode generiert ein zufälliges Datum innerhalb eines angegebenen Bereichs von Jahren zurück vom aktuellen Datum.

1. Stellen Sie sicher, dass das Projekt ohne Fehler erstellt und ausgeführt wird.

1. Wählen Sie Ihren ersten Prompt aus den von Ihnen vorbereiteten Prompts aus.

1. Wählen Sie den Code aus, den Sie verbessern möchten, und öffnen Sie dann die Chatansicht.

1. Verwenden Sie in der Chatansicht die Schaltfläche **Kontext anfügen**, um dem Chatkontext relevante Dateien hinzuzufügen, und geben Sie dann Ihren Prompt ein.

    Sie können auch die Verwendung eines Drag & Drop-Vorgangs veranschaulichen, um Dateien aus der Projektmappen-Explorer-Ansicht an den Chatkontext anzufügen.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie entscheiden sich für die Arbeit an der Datei Program.cs.
    - Sie wählen den folgenden Prompt: `@workspace /explain #selection How can I improve the readability of the GenerateRandomBalance, GenerateRandomAccountHolder, GenerateRandomAccountType, and GenerateRandomDateOpened methods?`
    - Sie öffnen die Datei Program.cs und wählen die folgenden Methoden aus: `GenerateRandomBalance`, `GenerateRandomAccountHolder`, `GenerateRandomAccountType`, `GenerateRandomDateOpened`.
    - Sie öffnen die Chatansicht und fügen die Datei Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    Nachdem Sie diese Aktionen abgeschlossen haben, schlägt GitHub Copilot Chat Updates vor, die der folgenden Antwort ähneln:

    *Um die Lesbarkeit dieser Methoden zu verbessern, können Sie die folgenden Schritte ausführen:*

    *1. Extrahieren Sie wiederholten Code in separate Methoden: Das Random-Objekt wird mehrmals in verschiedenen Methoden erstellt. Sie können ein statisches Random-Objekt auf Klassenebene erstellen und in allen Methoden verwenden. Dies würde nicht nur die Lesbarkeit verbessern, sondern auch eine bessere Zufälligkeit bieten.*

    `private static readonly Random random = new Random();`

    *2. Verwenden Sie aussagekräftige Variablennamen: Der Variablenname `range` in der GenerateRandomDateOpened-Methode ist ein bisschen vage. Ein aussagekräftigerer Name wie daysRange könnte verwendet werden.*

    *3. Kommentare hinzufügen: Obwohl der Code größtenteils selbsterklärend ist, kann es für andere Fachkräfte in der Entwicklung hilfreich sein, Kommentare hinzuzufügen, um zu erklären, was die einzelnen Methoden tun.*

    *4. Verwenden Sie Konstanten für magische Zahlen: In der Methode „GenerateRandomDateOpened“ wird die Zahl `10` verwendet, um die Anzahl der Jahre darzustellen, die das Startdatum zurückliegen kann. Dies könnte in eine Konstante mit einem beschreibenden Namen (etwa `MaxYearsBack`) extrahiert werden.*

    *5. Verwenden Sie das var-Schlüsselwort: In C# können Sie das var-Schlüsselwort verwenden, wenn die rechte Seite der Zuordnung den Typ offensichtlich macht. Dadurch kann Ihr Code übersichtlicher und einfacher zu lesen sein.*

   *Hier erfahren Sie, wie Ihr Code nach diesen Verbesserungen aussehen kann:*

    ```csharp

    private static readonly Random random = new Random();
    private const int MaxYearsBack = 10;
    static double GenerateRandomBalance(double min, double max)
    {
        double balance = random.NextDouble() * (max - min) + min;
        return Math.Round(balance, 2);
    }
    static string GenerateRandomAccountHolder()
    {
        string[] accountHolderNames = {  /* names here */  };
        var accountHolderName = accountHolderNames[random.Next(0, accountHolderNames.Length)];
        return accountHolderName;
    }
    static string GenerateRandomAccountType()
    {
        string[] accountTypes = {  /* types here */  };
        return accountTypes[random.Next(0, accountTypes.Length)];
    }
    static DateTime GenerateRandomDateOpened()
    {
        DateTime startDate = new DateTime(DateTime.Today.Year - MaxYearsBack, 1, 1);
        int daysRange = (DateTime.Today - startDate).Days;
        DateTime randomDate = startDate.AddDays(random.Next(daysRange));
        if (randomDate.Year == DateTime.Today.Year && randomDate >= DateTime.Today)
        {
            randomDate = randomDate.AddDays(-1);
        }
        return randomDate;
    }

    ```

    > [!IMPORTANT]
    > Beachten Sie die Platzhalterwerte (z. B. `/* types here */`) in den Methoden `GenerateRandomAccountHolder` und `GenerateRandomAccountType`. GitHub Copilot Chat ersetzt gelegentlich Codedetails durch Platzhalter. Diese sind leicht zu erkennen, wenn Sie aufmerksam sind. Sie müssen die Platzhalterwerte durch Werte aus Ihrer Anwendung ersetzen, wenn Sie eine Aktualisierung durchführen. Wenn Sie Platzhalter sehen, sollten Sie eine Kopie Ihres bestehenden Codes erstellen, bevor Sie die vorgeschlagenen Änderungen vornehmen. Wenn der vorgeschlagene Codeblock mit dem Code in Ihrer Anwendung übereinstimmt, können Sie einen Blockkommentar verwenden, um Ihren vorhandenen Code auszukommentieren, und dann die Schaltfläche **Am Cursor einfügen** in der Chatansicht verwenden, um die vorgeschlagenen Aktualisierungen zu implementieren, ohne einen Benennungskonflikt zu verursachen. Sobald Sie sich vergewissert haben, dass die vorgeschlagene Aktualisierung wie erwartet funktioniert, können Sie den Sperrvermerk entfernen.

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, die zur Verbesserung der Lesbarkeit des Codes, der Wartbarkeit und der Modularität beitragen.

    Wenn Sie Blockkommentare verwendet haben, um Ihren bestehenden Code auszukommentieren, können Sie die vorgeschlagenen Aktualisierungen mit der Funktion **Am Cursor einfügen** in der Chatansicht einfügen. Sie können auch die Option „Kopieren“ verwenden und die Aktualisierung an einem Ort Ihrer Wahl einfügen.

    Berücksichtigen Sie die an Ihrem Arbeitsplatz geltenden Kodierungsstandards und -richtlinien, bevor Sie entscheiden, welche Aktualisierungsvorschläge Sie umsetzen möchten.

1. Um sicherzustellen, dass bei der Implementierung Ihrer Updates keine Fehler aufgetreten sind, sollten Sie Ihre Lösung erstellen und ausführen, bevor Sie fortfahren.

1. Geben Sie Ihren zweite Prompt ein und prüfen Sie die vom GitHub Copilot Chat vorgeschlagenen Aktualisierungen.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie implementieren die Aktualisierungen, die der GitHub Copilot Chat für den ersten Beispielprompt vorgeschlagen hat.
    - Sie entscheiden sich, weiterhin an der Datei Program.cs zu arbeiten.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I improve the maintainability of the Main, GenerateRandomBalance, GenerateRandomAccountHolder, GenerateRandomAccountType, and GenerateRandomDateOpened methods?`.
    - Sie wählen die folgende(n) Methode(n): `Main`, `GenerateRandomBalance`, `GenerateRandomAccountHolder`, `GenerateRandomAccountType`, `GenerateRandomDateOpened`.
    - Sie öffnen die Chatansicht und fügen die Datei Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    Nachdem Sie diese Aktionen abgeschlossen haben, schlägt GitHub Copilot Chat Updates vor, die der folgenden Antwort ähneln:

    *Um die Wartbarkeit dieser Methoden zu verbessern, können Sie die folgenden Schritte ausführen:*

    *1. Trennung von Zuständigkeiten: Bei der Main-Methode werden viele Dinge getan: Erstellen von Konten, Simulieren von Transaktionen und Simulieren von Überweisungen. Diese könnten in separate Methoden aufgeteilt werden, um die Lesbarkeit und Wartbarkeit zu verbessern.*

    *2. Fehlerbehandlung: Der Code verwendet eine allgemeine Ausnahme für die Fehlerbehandlung. Es wäre besser, benutzerdefinierte Ausnahmen zu erstellen, die spezifisch für die Anwendung sind. Dies würde das Verständnis und die Behandlung von Fehlern erleichtern.*

    *3. Magische Zahlen: Der Code enthält magische Zahlen (wie 20 für die Anzahl der Konten, 100 für die Anzahl der Transaktionen usw.). Diese sollten durch benannte Konstanten ersetzt werden.*

    *4. Codeduplizierung: Der Code für die Erzeugung von Zufallswerten ist an mehreren Stellen dupliziert. Dies könnte in eine Hilfsklasse oder Methoden umgewandelt werden.*

    ```csharp

    class Program
    {
        private static readonly Random random = new Random();
        private const int MaxYearsBack = 10;
        private const int NumberOfAccounts = 20;
        private const int NumberOfTransactions = 100;
        static void Main(string[] args)
        {
            List<BankAccount> accounts = CreateBankAccounts(NumberOfAccounts);
            SimulateTransactions(accounts, NumberOfTransactions);
            SimulateTransfers(accounts);
        }
        static List<BankAccount> CreateBankAccounts(int numberOfAccounts)
        {
            List<BankAccount> accounts = new List<BankAccount>();
            int createdAccounts = 0;
            while (createdAccounts < numberOfAccounts)
            {
                try
                {
                    // same code as before...
                }
                catch (Exception ex)
                {
                    Console.WriteLine($"Account creation failed: {ex.Message}");
                }
            }
            return accounts;
        }
        static void SimulateTransactions(List<BankAccount> accounts, int numberOfTransactions)
        {
            // same code as before...
        }
        static void SimulateTransfers(List<BankAccount> accounts)
        {
            // same code as before...
        }
        // same helper methods as before...
    }

    ```

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, die zur Verbesserung der Lesbarkeit des Codes, der Wartbarkeit und der Modularität beitragen.

    Wenn Sie Blockkommentare verwendet haben, um Ihren bestehenden Code auszukommentieren, können Sie die vorgeschlagenen Aktualisierungen mit der Funktion **Am Cursor einfügen** in der Chatansicht einfügen. Sie können auch die Option „Kopieren“ verwenden und die Aktualisierung an einem Ort Ihrer Wahl einfügen.

1. Um sicherzustellen, dass die Änderungen keine Fehler verursacht haben, erstellen Sie Ihre Lösung und führen Sie sie aus, bevor Sie fortfahren.

1. Geben Sie Ihren dritten Prompt ein, und nehmen Sie sich dann eine Minute Zeit, um die Vorschläge zu überprüfen.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie implementieren die Updates, die der GitHub Copilot-Chat für den ersten und den zweiten Prompt vorgeschlagen hat.
    - Sie entscheiden sich, weiterhin an der Datei Program.cs zu arbeiten.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I improve the modularity of the Program.cs file?`.
    - Sie wählen den folgenden Link: Wählen Sie die gesamte Program.cs-Datei aus.
    - Sie öffnen die Chatansicht und fügen die Datei Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    Nachdem Sie diese Aktionen abgeschlossen haben, schlägt GitHub Copilot Chat Updates vor, die der folgenden Antwort ähneln:

    *Um die Modularität der Datei Program.cs zu verbessern, können Sie die folgenden Schritte ausführen:*

    *1. Separate Aspekte: Die Klasse `Program` macht zu viel. Es werden Konten erstellt, Transaktionen simuliert und zufällige Daten generiert. Jede dieser Zuständigkeiten könnte eine separate Klasse sein. Sie könnten zum Beispiel eine Klasse `BankAccountFactory` haben, die für die Erstellung von Bankkonten zuständig ist, eine Klasse `TransactionSimulator` für die Simulation von Transaktionen und eine Klasse `RandomDataGenerator` für die Erzeugung von Zufallsdaten.*

    *2. Verwenden von Schnittstellen: Schnittstellen können verwendet werden, um einen Vertrag für Klassen zu definieren. Dadurch kann Ihr Code flexibler und einfacher getestet werden. Sie können beispielsweise eine `IAccountFactory`-Schnittstelle mit einer `Create`-Methode definieren und diese Schnittstelle dann durch `BankAccountFactory` implementieren lassen.*

    *3. Magische Zahlen: Im Code gibt es mehrere „magische Zahlen“ (z. B. 10, 50.000, -500, 500 usw.). Diese Zahlen sollten durch benannte Konstanten ersetzt werden, damit der Code leichter zu lesen und zu warten ist.*

    *4. Duplizierung: Die Methoden `SimulateTransactions` und `SimulateTransfers` weisen nahezu identischen Code auf. Diese Duplizierung kann durch die Schaffung einer gemeinsamen Methode vermieden werden, die beide Methoden aufrufen.*

   *Hier ist ein Beispiel dafür, wie Sie die CreateBankAccounts-Methode umgestalten können:*

    **Codeschnipsel A: Schnittstellen verwenden**

    ```csharp

    interface IAccountFactory
    {
        BankAccount Create(int index);
    }
    class BankAccountFactory : IAccountFactory
    {
        private readonly RandomDataGenerator _randomDataGenerator;
        public BankAccountFactory(RandomDataGenerator randomDataGenerator)
        {
            _randomDataGenerator = randomDataGenerator;
        }
        public BankAccount Create(int index)
        {
            double initialBalance = _randomDataGenerator.GenerateRandomBalance(10, 50000);
            string accountHolderName = _randomDataGenerator.GenerateRandomAccountHolder();
            string accountType = _randomDataGenerator.GenerateRandomAccountType();
            DateTime dateOpened = _randomDataGenerator.GenerateRandomDateOpened();
            return new BankAccount($"Account {index + 1}", initialBalance, accountHolderName, accountType, dateOpened);
        }
    }
    // In the `Program` class, you would then use the `IAccountFactory` to create accounts:
    interface IAccountFactory
    {
        BankAccount Create(int index);
    }
    class BankAccountFactory : IAccountFactory
    {
        private readonly RandomDataGenerator _randomDataGenerator;
        public BankAccountFactory(RandomDataGenerator randomDataGenerator)
        {
            _randomDataGenerator = randomDataGenerator;
        }
        public BankAccount Create(int index)
        {
            double initialBalance = _randomDataGenerator.GenerateRandomBalance(10, 50000);
            string accountHolderName = _randomDataGenerator.GenerateRandomAccountHolder();
            string accountType = _randomDataGenerator.GenerateRandomAccountType();
            DateTime dateOpened = _randomDataGenerator.GenerateRandomDateOpened();
            return new BankAccount($"Account {index + 1}", initialBalance, accountHolderName, accountType, dateOpened);
        }
    }

    ```

    **Codeschnipsel B: Duplizierung**

    ```csharp

    static void SimulateOperations(List<BankAccount> accounts, int numberOfOperations, Action<BankAccount, double> operation)
    {
        foreach (BankAccount account in accounts)
        {
            for (int i = 0; i < numberOfOperations; i++)
            {
                double transactionAmount = GenerateRandomBalance(-500, 500);
                try
                {
                    operation(account, transactionAmount);
                    Console.WriteLine($"Operation: {transactionAmount}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                }
                catch (Exception ex)
                {
                    Console.WriteLine($"Operation failed: {ex.Message}");
                }
            }
            Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
        }
    }
    // Then you can call this method like this:
    SimulateOperations(accounts, NumberOfTransactions, (account, amount) => {
        if (amount >= 0)
        {
            account.Credit(amount);
        }
        else
        {
            account.Debit(-amount);
        }
    });

    ```

    > [!NOTE]
    > Sie brauchen die Aktualisierungsvorschläge, die GitHub Copilot aus Ihrem dritten Prompt generiert hat, nicht zu implementieren. Die Überprüfung der Vorschläge kann Aufschluss darüber geben, wie der Prozess der Codeverbesserung voranschreitet.

Ihre nächsten Demos umfassen die folgenden Themen:

- Verbessern der Codesicherheit und -leistung mithilfe von GitHub Copilot Chat
- Verbessern der Codesicherheit mithilfe von GitHub Copilot Chat

## Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um Vorschläge zur Verbesserung der Codequalität in einer Beispielanwendung zu generieren. Sie haben drei Prompts entwickelt, die darauf abzielten, die Lesbarkeit des Codes, die Wartbarkeit und die Modularität zu verbessern. Sie haben die Vorschläge von GitHub Copilot Chat überprüft und die Updates implementiert, die dazu beigetragen haben, die Codequalität zu verbessern. Sie haben auch zusätzliche Vorschläge berücksichtigt, die Ihren Code weiter verbessern könnten.
