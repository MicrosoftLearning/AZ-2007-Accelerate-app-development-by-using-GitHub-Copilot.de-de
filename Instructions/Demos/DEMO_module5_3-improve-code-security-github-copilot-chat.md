---
demo:
  title: 'Demo: Verbessern der Codesicherheit mithilfe von GitHub Copilot Chat'
  module: 'Module 5: Implement code improvements using GitHub Copilot tools'
---

# Demo: Verbessern der Codesicherheit mithilfe von GitHub Copilot Chat

## Anweisungen

Die Aktivitäten der Demo sind für eine Umgebung konzipiert, die die folgenden Ressourcen umfasst:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Codesicherheit bezieht sich auf die Maßnahmen, die ergriffen werden, um Software vor unbefugtem Zugriff, Datenpannen und anderen Sicherheitsbedrohungen zu schützen. Codesicherheit ist ein wesentlicher Aspekt der Softwareentwicklung, der den Schutz von Anwendungen und Systemen vor Sicherheitsbedrohungen umfasst. Durch Steigerung Ihrer Codesicherheit können Sie Ihre Anwendungen und Systeme vor Sicherheitsbedrohungen schützen.

> [!IMPORTANT]
> Erläutern Sie den Kursteilnehmenden, dass es in dieser Demo nicht um bewährte Methoden für die Entwicklung von sicherem Code geht. Stattdessen geht es darum, wie man den GitHub Copilot Chat nutzt, um Vorschläge zur Verbesserung der Codesicherheit in einer Beispielanwendung zu generieren. Die Vorschläge stellen keine bewährten Methoden oder umfassende Lösungen für die Entwicklung von sicherem Code dar. Fachkräfte in der Entwicklung sollten die Vorschläge von GitHub Copilot Chat nach eigenem Ermessen und auf der Grundlage der eigenen Kompetenzen bewerten und implementieren. Wenn Sie Vorschläge von GitHub Copilot implementieren, heißt das nicht, dass keine gründlichen Codeüberprüfungen und Tests mehr erforderlich sind.

#### Codesicherheit

Die Gewährleistung der Codesicherheit liegt in der Verantwortung aller, nicht nur der Fachkräfte in der Entwicklung. Die Fachkräfte in der Entwicklung spielen jedoch eine entscheidende Rolle, indem sie dafür sorgen, dass der von ihnen geschriebene Code sicheren Codierungspraktiken folgt. Sichere Codierungsverfahren tragen dazu bei, dass Softwareschwachstellen nicht von Angreifern ausgenutzt werden können. Fachkräfte in der Entwicklung können durch die Einhaltung von Praktiken zur sicheren Codierung dazu beitragen, die Software vor Sicherheitsbedrohungen zu schützen und sicherzustellen, dass sie sicher und zuverlässig ist.

Die folgenden Abschnitte geben einen Überblick über Verfahren zur Codesicherheit, die Ihre Kursteilnehmenden beachten sollten.

##### Bewerten der Codesicherheit mithilfe eines umfassenden Ansatzes

Bei der Bewertung der Codesicherheit ist es wichtig, einen umfassenden Ansatz zu verfolgen, der verschiedene Aspekte des Lebenszyklus der Softwareentwicklung einbezieht. Im Folgenden finden Sie einige wichtige Überlegungen:

- Methoden für sichere Codierung: Einhaltung von Standards und Richtlinien zur sicheren Codierung, um Schwachstellen zu vermeiden.
- Tools zur Codeanalyse: Einsatz von statischen und dynamischen Codeanalysetools zur Aufdeckung von Sicherheitsmängeln.
- Verwaltung von Abhängigkeiten: Sicherstellung, dass die Bibliotheken und Abhängigkeiten von Drittanbietern auf dem neuesten Stand und frei von bekannten Sicherheitslücken sind.
- Authentifizierung und Autorisierung: Implementierung von robusten Authentifizierungs- und Autorisierungsmechanismen zum Schutz vor unbefugtem Zugriff.
- Datenschutz: Verschlüsselung sensibler Daten sowohl im Ruhezustand als auch bei der Übertragung, um Datenpannen zu verhindern.
- Fehlerbehandlung: Entwicklung von Verfahren zur sicheren Fehlerbehandlung, die keine sensiblen Informationen preisgeben.
- Sicherheitstests: Durchführung von gründlichen Sicherheitstests, einschließlich Penetrationstests und Schwachstellenbewertungen.
- Compliance: Sicherstellung, dass der Code den einschlägigen Sicherheitsstandards und -vorschriften entspricht.
- Aus- und Weiterbildung: Wir bieten Fachkräften in der Entwicklung fortlaufende Sicherheitsschulungen und -trainings, um sie über die neuesten Bedrohungen und bewährten Methoden auf dem Laufenden zu halten.Providing developers with ongoing security education and training to keep them informed about the latest threats and best practices.
- Incident Response: Ausarbeitung eines genau definierten Reaktionsplans für Zwischenfälle. Im Falle eines Sicherheitsverstoßes muss der Reaktionsplan zugänglich sein.

Die Berücksichtigung dieser Faktoren und die Integration bewährter Methoden in den Entwicklungsprozess tragen dazu bei, dass sichere Inhalte und Anwendungen erstellt werden können.

##### Durchführung von Überprüfungen der Codesicherheit

Um sicherzustellen, dass der Code sicher ist, sollten Fachkräfte in der Entwicklung die folgenden Aspekte ihres Codes überprüfen:

- Richtigkeit: Überprüfen, ob der Code frei von logischen Fehlern und Mängeln ist, die zu Sicherheitslücken führen könnten.
- Sicherheit: Sicherstellen, dass der Code den bewährten Methoden der Sicherheit entspricht und keine Schwachstellen enthält.
- Diagnose: Einführung geeigneter Protokollierungs- und Diagnosefunktionen zur Erkennung von und Reaktion auf Sicherheitsvorfälle.
- Entwurfsfehler oder -einschränkungen: Überprüfen der Codierung, um sicherzustellen, dass es keine Schwachstellen oder Einschränkungen gibt, die ausgenutzt werden könnten.
- Skalierung und Leistung: Berücksichtigung der Leistung und Skalierbarkeit des Codes. Schlechte Leistung und Skalierbarkeit können die Sicherheit in Hochlastszenarien beeinträchtigen.
- Lokalisierung: Sicherstellen, dass der Code sicher mit verschiedenen Gebietsschemata umgeht, was sich auf die Datenformatierung und -darstellung auswirken kann.
- Barrierefreiheit (UX): Sicherstellen, dass die Sicherheitsmaßnahmen die Zugänglichkeit und die Erfahrung der benutzenden Person nicht beeinträchtigen.Verify that security measures do not negatively impact the accessibility and user experience.
- Tests: Überprüfen der Teststrategien und Sicherstellen, dass die Sicherheitstests gründlich sind und alle Aspekte des Codes abdecken.
- Instrumentierung: Sicherstellen, dass der Code so instrumentiert ist, dass er die Sicherheitsüberwachung und die Erkennung von Bedrohungen unterstützt.
- Konventionen für Konsistenz- und Codeformatvorlagen: Pflegen eines einheitlichen Codierungsstils, der sicheren Codierungsrichtlinien und -standards folgt.

Wenn Fachkräfte in der Entwicklung diese Aspekte ihres Codes überprüfen, können sie die Sicherheit ihres Codes erheblich verbessern. Code Reviews helfen Fachkräften in der Entwicklung, einen Beitrag zur Gesamtsicherheit der von ihnen entwickelten Software zu leisten.

##### Analysieren von Coderisiken

Bestimmte Teile einer Anwendung sind anfälliger für Sicherheitsangriffe, und es ist wichtig, sich auf die Absicherung dieser Bereiche zu konzentrieren. Hier sind einige der anfälligeren Bereiche:

- Integrationspunkte: Für Integrationspunkte mit abhängigen Produktteams müssen Überprüfungen des Sicherheitsentwurfs durchgeführt werden. Überprüfungen sind für Produkte, die Daten mit hohem geschäftlichen Einfluss („High Business Impact“, HBI) oder Unternehmensanwendungen und -dienste verarbeiten, unerlässlich.
- Interne Systeme: Interne Vorfälle sind eine häufige Ursache für Sicherheitsverletzungen, insbesondere in kleinen Unternehmen.
- E-Mail-Systeme: E-Mail-Server, insbesondere diejenigen, die nicht unterstützt oder nicht gepatcht sind, sind dauerhaft anfällig.
- Datenbanken und Speicher: Datenbanken, die eine Vorverschlüsselung sensibler Daten vor der Speicherung erfordern, können anfällig sein, wenn die Daten nicht wie erwartet verschlüsselt werden.
- Laufzeitumgebung: Technologien wie Runtime Application Self-Protection (RASP) können Angriffe auf eine Anwendung in Echtzeit erkennen, wodurch die Laufzeitumgebung zu einem kritischen Bereich wird, der gesichert werden muss.
- Webanwendungen: Webanwendungen werden häufig von Angreifern mit Methoden wie Einschleusung von SQL-Befehlen, Cross-Site Scripting (XSS) und Pufferüberläufen angegriffen.
- Endpunkte: Geräte und Anwendungen sind dem Risiko von Cyberangriffen ausgesetzt. Es ist wichtig, die Angriffsfläche durch Funktionen wie Ransomwareabwehr, Steuerelemente für Anwendungen, Webschutz und Netzwerkfirewall zu reduzieren.

Fachkräfte in der Entwicklung und Sicherheitsteams sollten diesen Bereichen Priorität einräumen und strenge Sicherheitsmaßnahmen zum Schutz vor potenziellen Angriffen einführen. Regelmäßige Sicherheitsüberprüfungen, Aktualisierungen und die Einhaltung bewährter Methoden können dazu beitragen, diese Schwachstellen zu entschärfen.

##### Suchen nach häufig auftretenden Sicherheitsfehlern

Fachkräfte in der Entwicklung können auf verschiedene Sicherheitslücken in ihrem Code stoßen, die zu Sicherheitslücken führen können, wenn sie nicht ordnungsgemäß behoben werden. Einige typische Sicherheitsfehler sind:

- Einschleusungsfehler: Zum Beispiel SQL-, NoSQL-, OS- und LDAP-Einschleusung, bei der nicht vertrauenswürdige Daten als Teil eines Befehls oder einer Abfrage an einen Interpreter gesendet werden.
- Fehlerhafte Authentifizierung: Wenn die Authentifizierung und die Sitzungsverwaltung falsch implementiert sind, kann die Authentifizierung unterbrochen werden. Gute Implementierungen stellen sicher, dass Kennwörter, Schlüssel und Sitzungstokens nicht von Angreifern missbraucht werden können.
- Offenlegung vertraulicher Daten: Ein unzureichender Schutz sensibler Daten kann dazu führen, dass sie bei der Übertragung über das Netz oder im Ruhezustand gefährdet sind.
- Fehlerhafte Zugriffssteuerung: Die Steuerelemente, die den Zugriff von benutzenden Personen regeln, werden nicht richtig durchgesetzt.
- Cross-Site Scripting (XSS): XSS-Fehler treten immer dann auf, wenn eine Anwendung nicht vertrauenswürdige Daten ohne ordnungsgemäße Validierung oder Escaping in eine Webseite einfügt.
- Unsichere Deserialisierung: Dies kann zu Remotecodeausführung, Replay-Angriffen, Einschleusungsangriffen und Angriffen zur Ausweitung von Berechtigungen führen.
- Unzureichende Protokollierung und Überwachung: Unzureichende Protokollierung und Überwachung in Verbindung mit fehlender oder unzureichender Integration in die Reaktion auf Vorfälle ermöglichen weitere Angriffe.
- Unsichere, direkte Verweise auf Objekte (IDOR): Ein Problem der Zugriffssteuerung, das auftritt, wenn eine Anwendung direkten Zugriff auf Objekte auf der Grundlage von Eingaben der benutzenden Person ermöglicht.
- Fehlende Zugriffssteuerung auf Funktionsebene: Manchmal schützt eine Anwendung die Steuerelemente der Funktionsebene nicht ordnungsgemäß, so dass Angreifer Anforderungen für den Zugriff auf Funktionen ohne entsprechende Berechtigung fälschen können.

Viele andere Sicherheitslücken können im Code gefunden werden. Es ist wichtig, dass Fachkräfte in der Entwicklung Tools und bewährte Methoden einsetzen, um diese Probleme proaktiv zu erkennen und zu beheben.

### Entwickeln von Prompts für GitHub Copilot Chat

Die Prompts, die Sie für GitHub Copilot Chat schreiben, müssen einen klar definierten Kontext und eine klar definierte Absicht haben. Berücksichtigen Sie bei der Entwicklung Ihrer Prompts die folgenden Vorschläge:

- Definieren Sie einen äußeren Kontext, der auf einer höheren Ebene angesiedelt ist als der Code, den Sie aktualisieren möchten. Wenn Sie zum Beispiel eine Methode verbessern möchten, geben Sie die Klasse oder Datei, die die Methode enthält, als äußeren Kontext an. Identifizieren Sie die Methode als inneren Kontext.
- Verwenden Sie Chatteilnehmer und Chatvariablen, um den Kontext anzugeben. Sie können die Chat-Variablen `#file:` und `#selection` verwenden, um den spezifischen Code zu identifizieren, auf den Sie sich konzentrieren. Gegebenenfalls können Sie auch den gesamten Arbeitsbereich (`@workspace`) einschließen. Nehmen Sie im natürlichsprachlichen Teil Ihres Prompts Bezug auf die Datei- oder Codeauswahl.
- Die Absicht muss klar, präzise und spezifisch sein. Ihr Prompt muss die Art der Verbesserung enthalten, die Sie erreichen möchten.

Während dieses Teils der Demo überprüfen Sie das Projekt **APL2007M5BankAccount-Security** und erstellen drei Prompts für GitHub Copilot Chat. Die Prompts richten sich auf die Steigerung der Codesicherheit.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie das Projekt **APL2007M5BankAccount-Security **, und überprüfen Sie die Codedateien **Program.cs** und **BankAccount.cs**.

    Die Datei **Program.cs** enthält den Code für eine einfache Bankanwendung, die die Erstellung von Bankkonten, Transaktionen und Überweisungen simuliert.

    Die Datei **BankAccount.cs** enthält den Code für die `BankAccount`-Klasse, die ein Bankkonto mit grundlegenden Funktionen wie Einzahlung, Abhebung und Saldoabfrage darstellt.

1. Nehmen Sie sich einen Moment Zeit, um einige Prompts zu beschreiben, mit denen die Codesicherheit verbessert werden kann.

    Bei diesem Projekt können Sie folgende Prompts verwenden, um Verbesserungsvorschläge für die Codesicherheit zu generieren:

    Prompt: `@workspace /explain How can I implement authentication in the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I protect sensitive data in the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I implement logging of suspicious account activities of the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve the security of exception handling in the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve the security of the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve the security of the [selected code]?` (Anfügen von Program.cs an den Chatkontext)

1. Wählen Sie drei Prompts aus, die Sie im weiteren Verlauf der Demo verwenden können.

    Versuchen Sie, zwei Prompts auszuwählen, die Sicherheitsfragen in der Datei BankAccount.cs und eine für die Datei Program.cs behandeln. In dieser Übung stellt die Klasse „BankAccount“ Ihr „Produkt“ dar. Die Datei Program.cs verwendet die Klasse BankAccount, um Kontoaktivitäten und -transaktionen zu simulieren.

### Verbessern der Codesicherheit der BankAccount-Klasse mithilfe von GitHub Copilot Chat

Die Entwicklung von sicherem Code ist für jedes Softwareprojekt unerlässlich. Das erforderliche Maß an Sicherheit hängt von der Art der Anwendung und der von ihr verarbeiteten Daten ab.

In dieser Demo verwenden Sie GitHub Copilot Chat, um Vorschläge zur Verbesserung der Sicherheit der Klasse „BankAccount“ im Projekt **APL2007M5BankAccount-Security** zu generieren.

Der GitHub Copilot Chat kann zur Verbesserung der Codesicherheit eingesetzt werden. Ihre Prompts können GitHub Copilot dazu veranlassen, Vorschläge zur Verbesserung der Authentifizierung, des Datenschutzes, der Protokollierung und Dutzender anderer Themen zu erstellen. Sie können auch weiter gefasste Prompts erstellen, um allgemeine Vorschläge zur Steigerung der Codesicherheit anzufordern. Eine Kombination aus spezifischen und allgemeinen Prompts kann Ihnen dabei helfen, Bereiche mit Verbesserungsbedarf zu identifizieren und die erforderlichen Änderungen zu implementieren.

> [!TIP]
> Die Implementierung und das Testen vorgeschlagener Aktualisierungen dauert eine gewisse Zeit, und Zeit ist während dieser Demo möglicherweise ein Faktor. Die Wahl von Prompts, die sich auf bestimmte Verbesserungsbereiche konzentrieren, kann Ihnen beim Zeitmanagement helfen. Zu weit gefasste Prompts können eine Vielzahl von Vorschlägen oder komplexe Vorschläge generieren, die sich nur schwer in kurzer Zeit auswerten und implementieren lassen. Sollten Sie feststellen, dass die vorgeschlagenen Aktualisierungen zu weit gefasst oder zu komplex sind, können Sie Ihre Prompts mit spezifischeren Details aktualisieren.

1. Stellen Sie sicher, dass das Projekt ohne Fehler erstellt und ausgeführt wird.

    Warnungen sind akzeptabel, solange die Anwendung ausgeführt wird. Aber Fehler müssen behoben werden, bevor Sie mit der Verwendung von GitHub Copilot Chat beginnen.

1. Öffnen Sie die Datei „BankAccount.cs“ in Visual Studio Code, und wählen Sie dann den gesamten Code in der Datei aus.

1. Öffnen Sie die Chatansicht.

1. Verwenden Sie in der Chatansicht die Schaltfläche **Kontext anfügen**, um dem Chatkontext relevante Dateien hinzuzufügen, und geben Sie dann Ihren Prompt ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie öffnen die Datei BankAccount.cs und markieren den gesamten Code.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I implement authentication in the BankAccount.cs file?`
    - Sie öffnen die Chatansicht und fügen die Dateien BankAccount.cs und Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    In diesem Fall schlägt GitHub Copilot-Chat Updates vor, die der folgenden Antwort ähneln:

    *Die Implementierung der Authentifizierung in diesem Zusammenhang würde in der Regel bedeuten, dass der Klasse „BankAccount“ eine Methode hinzugefügt wird, die die Identität der Person überprüft, der das Konto gehört, bevor bestimmte Vorgänge zugelassen werden. Dies kann mit einem Kennwort, einer PIN oder einer anderen Form der Authentifizierung geschehen.*

    *Hier ein einfaches Beispiel dafür, wie Sie der Klasse BankAccount eine Authentifizierung auf Kennwortbasis hinzufügen können:*

    ```csharp

    public class BankAccount
    {
        // Existing code...
        private string password;
        public BankAccount(string accountNumber, double initialBalance, string accountHolderName, string accountType, DateTime dateOpened, string password)
        {
            // Existing code...
    
            this.password = password;
        }
        public bool Authenticate(string password)
        {
            return this.password == password;
        }
        public void Credit(double amount, string password)
        {
            if (!Authenticate(password))
            {
                throw new Exception("Authentication failed.");
            }
            // Existing code...
        }
        // Similar changes would be made to the Debit, Transfer, and other methods...
    }

    ```

    *In diesem Beispiel wird ein Kennwort als Parameter zum BankAccount-Konstruktor hinzugefügt und in einem privaten Feld gespeichert. Es wird eine Authentifizierungsmethode hinzugefügt, die überprüft, ob das angegebene Kennwort mit dem gespeicherten Kennwort übereinstimmt. Die Credit-Methode (und andere Methoden, die eine Authentifizierung erfordern sollten) wird so geändert, dass sie ein Kennwort als Argument annimmt und „Authenticate“ aufruft, bevor der Vorgang ausgeführt wird.*

    *Dies ist eine sehr einfache Form der Authentifizierung und nicht sicher genug für echte Anwendungen. In einer echten Anwendung sollten Sie den Hash des Kennworts vor der Speicherung mit Salt validieren und sichere Methoden für die Übertragung des Kennworts von der benutzenden Person zur Anwendung verwenden. Sie sollten auch die Verwendung einer Zwei-Faktor-Authentifizierung oder anderer sicherer Methoden in Betracht ziehen.*

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, um die Codesicherheit für die `BankAccount`-Klasse zu verbessern.

    Die Datei Program.cs muss aktualisiert werden, um das Kennwort und die Authentifizierung zu verwenden, die der Klasse BankAccount hinzugefügt wurde. Sie können den GitHub Copilot-Chat verwenden, um Vorschläge zum Aktualisieren der Datei Program.cs zu generieren.

    1. Wählen Sie den Inhalt der Datei Program.cs aus, fügen Sie die Dateien Program.cs und BankAccount.cs an den Chatkontext an, und geben Sie dann den folgenden Prompt in die Chatansicht ein:

        ```plaintext
        @workspace /Explain How can I update the Program.cs file to use the password and authentication added to BankAccount.cs?
        ```

    1. Überprüfen Sie die vom GitHub Copilot-Chat bereitgestellten Vorschläge, und implementieren Sie dann die vorgeschlagenen Updates.

    1. Vergewissern Sie sich, dass die Änderungen keine Fehler verursacht haben, bevor Sie fortfahren. Erstellen Sie dazu Ihre Lösung, und führen Sie sie aus.

        Verwenden Sie GitHub Copilot, um Probleme zu beheben, die während des Buildprozesses identifiziert wurden.

    > [!IMPORTANT]
    > Stellen Sie sicher, dass die Kursteilnehmenden verstehen, dass diese sehr einfache Form der Authentifizierung nicht sicher genug für echte Anwendungen ist. In einer echten Anwendung würden Sie den Hash des Kennworts vor der Speicherung mit Salt validieren und sichere Methoden für die Übertragung des Kennworts von der benutzenden Person zur Anwendung verwenden wollen. Sie sollten auch die Verwendung einer Zwei-Faktor-Authentifizierung oder anderer sicherer Methoden in Betracht ziehen.

1. Stellen Sie sicher, dass Ihre Anwendung kompiliert und ausgeführt wird, bevor Sie fortfahren.

1. Wählen Sie den gesamten Code in der Datei „BankAccount.cs“ aus, und geben Sie dann Ihren zweiten Prompt in die Chatansicht ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie öffnen die Datei BankAccount.cs und markieren den gesamten Code.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I protect account numbers and account holder names in the selected code?`
    - Sie öffnen die Chatansicht und fügen die Dateien BankAccount.cs und Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    In diesem Fall schlägt GitHub Copilot-Chat Updates vor, die der folgenden Antwort ähneln:

    *Um vertrauliche Daten wie Kontonummern und Kontoinhabernamen in Ihrer Klasse BankAccount zu schützen, können Sie die folgenden Schritte ausführen:*

    *1. Kapselung verwenden:*

    *– Machen Sie die vertraulichen Eigenschaften „privat“ und stellen Sie kontrollierten Zugriff über Methoden bereit.*

    *2. Vertrauliche Daten verschlüsseln:*

    *– Verwenden Sie die Verschlüsselung, um vertrauliche Daten sicher zu speichern.*

    *3. Klartextspeicher verwenden:*

    *– Stellen Sie sicher, dass vertrauliche Daten nicht in Klartext gespeichert oder übertragen werden.*

    *Aktualisierte Implementierung*

    *Hier ist eine aktualisierte Version von BankAccount.cs, welche die Verschlüsselung für Kontonummern und Kontoinhabernamen verwendet:*

    ```csharp

    using System;
    using System.Security.Cryptography;
    using System.Text;
    namespace BankAccountApp
    {
        public class InsufficientFundsException : Exception
        {
            public double AttemptedAmount { get; }
            public double CurrentBalance { get; }
    
            public InsufficientFundsException(double attemptedAmount, double currentBalance)
                : base($"Insufficient balance for debit. Attempted to debit {attemptedAmount}, but current balance is {currentBalance}.")
            {
                AttemptedAmount = attemptedAmount;
                CurrentBalance = currentBalance;
            }
        }
        public class InvalidAccountTypeException : Exception
        {
            public string AccountType { get; }
            public InvalidAccountTypeException(string accountType)
                : base($"Invalid account type: {accountType}.")
            {
                AccountType = accountType;
            }
        }
        public class InvalidAccountNumberException : Exception
        {
            public string AccountNumber { get; }
            public InvalidAccountNumberException(string accountNumber)
                : base($"Invalid account number: {accountNumber}.")
            {
                AccountNumber = accountNumber;
            }
        }
        public class InvalidAccountHolderNameException : Exception
        {
            public string AccountHolderName { get; }
            public InvalidAccountHolderNameException(string accountHolderName)
                : base($"Invalid account holder name: {accountHolderName}.")
            {
                AccountHolderName = accountHolderName;
            }
        }
        public class InvalidDateOpenedException : Exception
        {
            public DateTime DateOpened { get; }
            public InvalidDateOpenedException(DateTime dateOpened)
                : base($"Invalid date opened: {dateOpened}.")
            {
                DateOpened = dateOpened;
            }
        }
        public class InvalidInitialBalanceException : Exception
        {
            public double InitialBalance { get; }
            public InvalidInitialBalanceException(double initialBalance)
                : base($"Invalid initial balance: {initialBalance}.")
            {
                InitialBalance = initialBalance;
            }
        }
        public class InvalidInterestRateException : Exception
        {
            public double InterestRate { get; }
            public InvalidInterestRateException(double interestRate)
                : base($"Invalid interest rate: {interestRate}.")
            {
                InterestRate = interestRate;
            }
        }
        public class InvalidTransferAmountException : Exception
        {
            public double TransferAmount { get; }
            public InvalidTransferAmountException(double transferAmount)
                : base($"Invalid transfer amount: {transferAmount}.")
            {
                TransferAmount = transferAmount;
            }
        }
        public class InvalidCreditAmountException : Exception
        {
            public double CreditAmount { get; }
            public InvalidCreditAmountException(double creditAmount)
                : base($"Invalid credit amount: {creditAmount}.")
            {
                CreditAmount = creditAmount;
            }
        }
        public class InvalidDebitAmountException : Exception
        {
            public double DebitAmount { get; }
            public InvalidDebitAmountException(double debitAmount)
                : base($"Invalid debit amount: {debitAmount}.")
            {
                DebitAmount = debitAmount;
            }
        }
        public class AuthenticationException : Exception
        {
            public AuthenticationException(string message) : base(message) { }
        }
        public class BankAccount
        {
            public enum AccountTypes
            {
                Savings,
                Checking,
                MoneyMarket,
                CertificateOfDeposit,
                Retirement
            }
            private string EncryptedAccountNumber { get; }
            private string EncryptedAccountHolderName { get; }
            public double Balance { get; private set; }
            public AccountTypes AccountType { get; }
            public DateTime DateOpened { get; }
            private const double MaxTransferAmountForDifferentOwners = 500;
            private string Username { get; }
            private string Password { get; }
            public BankAccount(string accountNumber, double initialBalance, string accountHolderName, string accountType, DateTime dateOpened, string username, string password)
            {
                if (accountNumber.Length != 10)
                {
                    throw new InvalidAccountNumberException(accountNumber);
                }
                if (initialBalance < 0)
                {
                    throw new InvalidInitialBalanceException(initialBalance);
                }
                if (accountHolderName.Length < 2)
                {
                    throw new InvalidAccountHolderNameException(accountHolderName);
                }
                if (dateOpened > DateTime.Now)
                {
                    throw new InvalidDateOpenedException(dateOpened);
                }
                EncryptedAccountNumber = Encrypt(accountNumber);
                EncryptedAccountHolderName = Encrypt(accountHolderName);
                Balance = initialBalance;
                AccountType = (AccountTypes)Enum.Parse(typeof(AccountTypes), accountType);
                DateOpened = dateOpened;
                Username = username;
                Password = password;
            }
            public void Credit(double amount)
            {
                if (amount < 0)
                {
                    throw new InvalidCreditAmountException(amount);
                }
                Balance += amount;
            }
            public void Debit(double amount)
            {
                if (amount < 0)
                {
                    throw new InvalidDebitAmountException(amount);
                }
                if (Balance >= amount)
                {
                    Balance -= amount;
                }
                else
                {
                    throw new InsufficientFundsException(amount, Balance);
                }
            }
            public double GetBalance()
            {
                return Balance;
            }
            public void Transfer(BankAccount toAccount, double amount)
            {
                ValidateTransferAmount(amount);
                ValidateTransferLimitForDifferentOwners(toAccount, amount);
                if (Balance >= amount)
                {
                    Debit(amount);
                    toAccount.Credit(amount);
                }
                else
                {
                    throw new InsufficientFundsException(amount, Balance);
                }
            }
            private void ValidateTransferAmount(double amount)
            {
                if (amount < 0)
                {
                    throw new InvalidTransferAmountException(amount);
                }
            }
            private void ValidateTransferLimitForDifferentOwners(BankAccount toAccount, double amount)
            {
                if (Decrypt(EncryptedAccountHolderName) != Decrypt(toAccount.EncryptedAccountHolderName) && amount > MaxTransferAmountForDifferentOwners)
                {
                    throw new Exception("Transfer amount exceeds maximum limit for different account owners.");
                }
            }
            public void PrintStatement()
            {
                Console.WriteLine($"Account Number: {Decrypt(EncryptedAccountNumber)}, Balance: {Balance}");
            }
            public double CalculateInterest(double interestRate)
            {
                if (interestRate < 0)
                {
                    throw new InvalidInterestRateException(interestRate);
                }
                return Balance * interestRate;
            }
            public void Authenticate(string username, string password)
            {
                if (Username != username || Password != password)
                {
                    throw new AuthenticationException("Invalid username or password.");
                }
            }
            private string Encrypt(string plainText)
            {
                using (Aes aes = Aes.Create())
                {
                    aes.Key = Encoding.UTF8.GetBytes("A very strong key"); // Use a secure key
                    aes.IV = Encoding.UTF8.GetBytes("A strong IV123456"); // Use a secure IV
                    ICryptoTransform encryptor = aes.CreateEncryptor(aes.Key, aes.IV);
                    using (var ms = new System.IO.MemoryStream())
                    {
                        using (var cs = new CryptoStream(ms, encryptor, CryptoStreamMode.Write))
                        {
                            using (var sw = new System.IO.StreamWriter(cs))
                            {
                                sw.Write(plainText);
                            }
                        }
                        return Convert.ToBase64String(ms.ToArray());
                    }
                }
            }
            private string Decrypt(string cipherText)
            {
                using (Aes aes = Aes.Create())
                {
                    aes.Key = Encoding.UTF8.GetBytes("A very strong key"); // Use a secure key
                    aes.IV = Encoding.UTF8.GetBytes("A strong IV123456"); // Use a secure IV
                    ICryptoTransform decryptor = aes.CreateDecryptor(aes.Key, aes.IV);
                    using (var ms = new System.IO.MemoryStream(Convert.FromBase64String(cipherText)))
                    {
                        using (var cs = new CryptoStream(ms, decryptor, CryptoStreamMode.Read))
                        {
                            using (var sr = new System.IO.StreamReader(cs))
                            {
                                return sr.ReadToEnd();
                            }
                        }
                    }
                }
            }
        }
    }

    ```

    *Syntax:*

    *– Stellen Sie sicher, dass Sie über die erforderlichen kryptografischen Bibliotheken verfügen. Das obige Beispiel verwendet der Einfachheit halber eine AES-Verschlüsselung mit einem hartcodierten Schlüssel und IV. In einer realen Anwendung sollten Sie Schlüssel und IVs sicher verwalten, wenn möglich mit einem Schlüsselverwaltungsdienst.*

    > [!IMPORTANT]
    > In einer realen Anwendung sollten Sie Schlüssel und IVs sicher verwalten, wenn möglich mit einem Schlüsselverwaltungsdienst. Die in diesem Training bereitgestellten Beispiele identifizieren Verbesserungsbereiche, stellen aber keine bewährten Methoden für sichere Verschlüsselung dar. Sie können GitHub Copilot-Chat verwenden, um weitere Vorschläge zur Verbesserung der Verschlüsselung und des Datenschutzes in Ihrer Anwendung zu verfolgen.

1. Die vorgeschlagenen Updates für den zweiten Prompt müssen nicht implementiert werden.

    Im Beispiel würden die vorgeschlagenen Updates dazu beitragen, die Sicherheit der Anwendung zu verbessern, aber sie erfordern erhebliche Konfigurationen und Updates für den Code von „Program.cs“, der außerhalb des Umfangs dieser Demo liegt.

### Verbessern der Codesicherheit der Program-Klasse mithilfe von GitHub Copilot Chat

1. Öffnen Sie die Datei „Program.cs“ in Visual Studio Code, und wählen Sie dann den gesamten Code in der Datei aus.

1. Öffnen Sie die Chatansicht, und geben Sie dann den ersten Prompt ein, den Sie für die Program-Klasse vorbereitet haben.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie öffnen die Datei Program.cs und wählen den gesamten Code aus.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I improve the security of the Program.cs file?`
    - Sie öffnen die Chatansicht und fügen die Dateien BankAccount.cs und Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    In diesem Fall schlägt GitHub Copilot-Chat Updates vor, die der folgenden Antwort ähneln:

    *Um die Sicherheit der Datei Program.cs zu verbessern, sollten Sie sich auf die folgenden Bereiche konzentrieren:*

    *1. Sichere Kennwortbehandlung:*

    *– Verwenden Sie sicheres Kennworthashing, und vermeiden Sie es, Kennwörter als Klartext zu speichern.*
    *– Verwenden Sie eine Bibliothek wie BCrypt.Net für das Kennworthashing.*

    *2. Vertrauliche Daten verschlüsseln:*

    *– Verschlüsseln Sie vertrauliche Daten wie Kontonummern und Kontoinhabernamen.*

    *3. Vermeiden hartcodierter Kennwörter:*

    *– Vermeiden Sie hartcodierte Kennwörter. Generieren Sie stattdessen sichere zufällige Kennwörter, oder fordern Sie Benutzende auf, eigene Kennwörter zu erstellen.*

    *4. Sichere Zufallszahlengenerierung verwenden:*

    *– Verwenden Sie einen kryptografisch sicheren Zufallszahlengenerator zum Generieren vertraulicher Daten.*

    *Aktualisierte Implementierung*

    *Hier ist eine aktualisierte Version von Program.cs, welche diese Verbesserungen enthält:*

    ```csharp

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Security.Cryptography;
    using System.Text;
    using System.Threading.Tasks;
    namespace BankAccountApp
    {
        class Program
        {
            private static readonly Random random = new Random();
            private const int MaxYearsBack = 10;
            private const int NumberOfAccounts = 20;
            private const int NumberOfTransactions = 100;
            private const double minTransactionAmount = -500.0;
            private const double maxTransactionAmount = 500.0;
            private const double minAccountStart = 200.0;
            private const double maxAccountStart = 1000.0;
            static async Task Main()
            {
                List<BankAccount> accounts = CreateBankAccounts(NumberOfAccounts);
                await SimulateTransactionsAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
                await SimulateTransfersAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
            }
            static List<BankAccount> CreateBankAccounts(int numberOfAccounts)
            {
                List<BankAccount> accounts = new();
                int createdAccounts = 0;
                while (createdAccounts < numberOfAccounts)
                {
                    try
                    {
                        double initialBalance = GenerateRandomDollarAmount(true, minAccountStart, maxAccountStart);
                        string accountHolderName = GenerateRandomAccountHolder();
                        string accountType = GenerateRandomAccountType();
                        DateTime dateOpened = GenerateRandomDateOpened();
                        string accountNumber = "102000" + random.Next(1000, 9999).ToString();
                        string username = "user" + createdAccounts;
                        string password = GenerateSecurePassword();
                        BankAccount account = new(accountNumber, initialBalance, accountHolderName, accountType, dateOpened, username, password);
                        accounts.Add(account);
                        createdAccounts++;
                    }
                    catch (ArgumentException ex)
                    {
                        Console.WriteLine($"Account creation failed due to invalid argument: {ex.Message}");
                        // Log the exception
                    }
                    catch (Exception ex)
                    {
                        Console.WriteLine($"Account creation failed: {ex.Message}");
                        // Log the exception
                    }
                    finally
                    {
                        // Any cleanup code would go here.
                    }
                }
                return accounts;
            }
            static async Task SimulateTransactionsAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                var tasks = accounts.Select(async account =>
                {
                    for (int i = 0; i < numberOfTransactions; i++)
                    {
                        double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                        try
                        {
                            account.Authenticate(account.Username, account.Password); // Authenticate before transaction
                            if (transactionAmount >= 0)
                            {
                                account.Credit(transactionAmount);
                                Console.WriteLine($"Credit: {transactionAmount}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                            }
                            else
                            {
                                account.Debit(-transactionAmount);
                                Console.WriteLine($"Debit: {transactionAmount}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                            }
                        }
                        catch (Exception ex)
                        {
                            Console.WriteLine($"Transaction failed: {ex.Message}");
                        }
                    }
                    Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                });
                await Task.WhenAll(tasks);
            }
            static async Task SimulateTransfersAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                var tasks = accounts.Select(async account =>
                {
                    for (int i = 0; i < numberOfTransactions; i++)
                    {
                        double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                        try
                        {
                            account.Authenticate(account.Username, account.Password); // Authenticate before transfer
                            BankAccount toAccount = accounts[random.Next(accounts.Count)];
                            toAccount.Authenticate(toAccount.Username, toAccount.Password); // Authenticate target account
                            account.Transfer(toAccount, transactionAmount);
                            Console.WriteLine($"Transfer: {transactionAmount}, From: {account.AccountNumber}, To: {toAccount.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                        }
                        catch (Exception ex)
                        {
                            Console.WriteLine($"Transfer failed: {ex.Message}");
                        }
                    }
                    Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                });
                await Task.WhenAll(tasks);
            }
            static double GenerateRandomDollarAmount(bool isAccount, double min, double max)
            {
                if (isAccount)
                {
                    double accountStartingValue = random.NextDouble() * (max - min) + min;
                    return Math.Round(accountStartingValue, 2);
                }
                else
                {
                    double transactionAmount = random.NextDouble() * random.Next((int)min, (int)max) + random.NextDouble();
                    return Math.Round(transactionAmount, 2);
                }
            }
            static string GenerateRandomAccountHolder()
            {
                string[] accountHolderNames = { "John Smith", "Maria Garcia", "Mohammed Khan", "Sophie Dubois", "Liam Johnson", "Emma Martinez", "Noah Lee", "Olivia Kim", "William Chen", "Ava Wang", "James Brown", "Isabella Nguyen", "Benjamin Wilson", "Mia Li", "Lucas Anderson", "Charlotte Liu", "Alexander Taylor", "Amelia Patel", "Daniel Garcia", "Sophia Kim" };
                var accountHolderName = accountHolderNames[random.Next(0, accountHolderNames.Length)];
                return accountHolderName;
            }
            static string GenerateRandomAccountType()
            {
                string[] accountTypes = { "Savings", "Checking", "Money Market", "Certificate of Deposit", "Retirement" };
                return accountTypes[random.Next(0, accountTypes.Length)];
            }
            static DateTime GenerateRandomDateOpened()
            {
                DateTime startDate = new(DateTime.Today.Year - MaxYearsBack, 1, 1);
                int daysRange = (DateTime.Today - startDate).Days;
                DateTime randomDate = startDate.AddDays(random.Next(daysRange));
                if (randomDate.Year == DateTime.Today.Year && randomDate >= DateTime.Today)
                {
                    randomDate = randomDate.AddDays(-1);
                }
                return randomDate;
            }
            static string GenerateSecurePassword()
            {
                const int passwordLength = 12;
                const string validChars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#$%^&*()";
                StringBuilder password = new StringBuilder();
                using (RNGCryptoServiceProvider rng = new RNGCryptoServiceProvider())
                {
                    byte[] uintBuffer = new byte[sizeof(uint)];
                    while (passwordLength > password.Length)
                    {
                        rng.GetBytes(uintBuffer);
                        uint num = BitConverter.ToUInt32(uintBuffer, 0);
                        password.Append(validChars[(int)(num % (uint)validChars.Length)]);
                    }
                }
                return password.ToString();
            }
        }
    }

    ```

1. Beachten Sie, dass die Updates für Program.cs sich auf die sichere Zufallszahlengenerierung konzentrierten.

    Die anderen Vorschläge gelten für die Klasse BankAccount, und die Implementierung liegt außerhalb des Umfangs dieses Trainings.

1. Erstellen Sie einen zusätzlichen Prompt für Program.cs, der die sichere Ausnahmebehandlung sicherstellen soll.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Wenn Sie in der Chatansicht beispielsweise `@workspace /explain How can I implement secure exception handling in the Program.cs file?` eingegeben haben, schlägt GitHub Copilot Chat Aktualisierungen vor, die in etwa wie in der folgenden Antwort aussehen:

    *Um die sichere Ausnahmebehandlung in der Datei Program.cs zu implementieren, sollten Sie die folgenden bewährten Methoden befolgen:*

    *1. Abfangen spezifischer Ausnahmen:*

    *– Fangen Sie bestimmte Ausnahmen ab, anstatt einen allgemeinen Catch-Block (Exception ex) zu verwenden. Dies hilft dabei, verschiedene Arten von Fehlern zu verstehen und angemessen zu behandeln.*

    *2. Sicheres Protokollieren von Ausnahmen:*

    *– Protokollieren Sie Ausnahmen sicher, ohne vertrauliche Informationen verfügbar zu machen. Verwenden Sie ein Protokollierungsframework zum Verwalten von Protokollen.*

    *3. Bereitstellen von benutzerfreundlichen Nachrichten:*

    *– Stellen Sie benutzerfreundliche Fehlermeldungen bereit, ohne interne Details preiszugeben.*

    *4. Verwenden abschließender Blöcke für die Bereinigung:*

    *– Verwenden Sie abschließende Blöcke, um sicherzustellen, dass alle erforderlichen Bereinigungen durchgeführt werden, unabhängig davon, ob eine Ausnahme ausgelöst wurde.*

    *5. Vermeiden des Abfangen nicht kritischer Ausnahmen:*

    *– Vermeiden Sie das Abfangen von Ausnahmen, die weitergegeben werden sollten, z. B. OutOfMemoryException oder StackOverflowException.*

    *Hier ist eine aktualisierte Version von Program.cs mit sicherer Ausnahmebehandlung:*

    ```csharp

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Security.Cryptography;
    using System.Text;
    using System.Threading.Tasks;
    namespace BankAccountApp
    {
        class Program
        {
            private static readonly Random random = new Random();
            private const int MaxYearsBack = 10;
            private const int NumberOfAccounts = 20;
            private const int NumberOfTransactions = 100;
            private const double minTransactionAmount = -500.0;
            private const double maxTransactionAmount = 500.0;
            private const double minAccountStart = 200.0;
            private const double maxAccountStart = 1000.0;
            static async Task Main()
            {
                List<BankAccount> accounts = CreateBankAccounts(NumberOfAccounts);
                await SimulateTransactionsAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
                await SimulateTransfersAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
            }
            static List<BankAccount> CreateBankAccounts(int numberOfAccounts)
            {
                List<BankAccount> accounts = new();
                int createdAccounts = 0;
                while (createdAccounts < numberOfAccounts)
                {
                    try
                    {
                        double initialBalance = GenerateRandomDollarAmount(true, minAccountStart, maxAccountStart);
                        string accountHolderName = GenerateRandomAccountHolder();
                        string accountType = GenerateRandomAccountType();
                        DateTime dateOpened = GenerateRandomDateOpened();
                        string accountNumber = "102000" + random.Next(1000, 9999).ToString();
                        string username = "user" + createdAccounts;
                        string password = GenerateSecurePassword();
                        BankAccount account = new(accountNumber, initialBalance, accountHolderName, accountType, dateOpened, username, password);
                        accounts.Add(account);
                        createdAccounts++;
                    }
                    catch (ArgumentException ex)
                    {
                        Console.WriteLine($"Account creation failed due to invalid argument: {ex.Message}");
                        // Log the exception securely
                        LogException(ex);
                    }
                    catch (Exception ex)
                    {
                        Console.WriteLine($"Account creation failed: {ex.Message}");
                        // Log the exception securely
                        LogException(ex);
                    }
                    finally
                    {
                        // Any cleanup code would go here.
                    }
                }
                return accounts;
            }
            static async Task SimulateTransactionsAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                var tasks = accounts.Select(async account =>
                {
                    for (int i = 0; i < numberOfTransactions; i++)
                    {
                        double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                        try
                        {
                            account.Authenticate(account.Username, account.Password); // Authenticate before transaction
                            if (transactionAmount >= 0)
                            {
                                account.Credit(transactionAmount);
                                Console.WriteLine($"Credit: {transactionAmount}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                            }
                            else
                            {
                                account.Debit(-transactionAmount);
                                Console.WriteLine($"Debit: {transactionAmount}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                            }
                        }
                        catch (InvalidCreditAmountException ex)
                        {
                            Console.WriteLine($"Invalid credit amount: {ex.Message}");
                            LogException(ex);
                        }
                        catch (InvalidDebitAmountException ex)
                        {
                            Console.WriteLine($"Invalid debit amount: {ex.Message}");
                            LogException(ex);
                        }
                        catch (InsufficientFundsException ex)
                        {
                            Console.WriteLine($"Insufficient funds: {ex.Message}");
                            LogException(ex);
                        }
                        catch (AuthenticationException ex)
                        {
                            Console.WriteLine($"Authentication failed: {ex.Message}");
                            LogException(ex);
                        }
                        catch (Exception ex)
                        {
                            Console.WriteLine($"Transaction failed: {ex.Message}");
                            LogException(ex);
                        }
                    }
                    Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                });
                await Task.WhenAll(tasks);
            }
            static async Task SimulateTransfersAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                var tasks = accounts.Select(async account =>
                {
                    for (int i = 0; i < numberOfTransactions; i++)
                    {
                        double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                        try
                        {
                            account.Authenticate(account.Username, account.Password); // Authenticate before transfer
                            BankAccount toAccount = accounts[random.Next(accounts.Count)];
                            toAccount.Authenticate(toAccount.Username, toAccount.Password); // Authenticate target account
                            account.Transfer(toAccount, transactionAmount);
                            Console.WriteLine($"Transfer: {transactionAmount}, From: {account.AccountNumber}, To: {toAccount.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                        }
                        catch (InvalidTransferAmountException ex)
                        {
                            Console.WriteLine($"Invalid transfer amount: {ex.Message}");
                            LogException(ex);
                        }
                        catch (InsufficientFundsException ex)
                        {
                            Console.WriteLine($"Insufficient funds: {ex.Message}");
                            LogException(ex);
                        }
                        catch (AuthenticationException ex)
                        {
                            Console.WriteLine($"Authentication failed: {ex.Message}");
                            LogException(ex);
                        }
                        catch (Exception ex)
                        {
                            Console.WriteLine($"Transfer failed: {ex.Message}");
                            LogException(ex);
                        }
                    }
                    Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                });
                await Task.WhenAll(tasks);
            }
            static double GenerateRandomDollarAmount(bool isAccount, double min, double max)
            {
                if (isAccount)
                {
                    double accountStartingValue = random.NextDouble() * (max - min) + min;
                    return Math.Round(accountStartingValue, 2);
                }
                else
                {
                    double transactionAmount = random.NextDouble() * random.Next((int)min, (int)max) + random.NextDouble();
                    return Math.Round(transactionAmount, 2);
                }
            }
            static string GenerateRandomAccountHolder()
            {
                string[] accountHolderNames = { "John Smith", "Maria Garcia", "Mohammed Khan", "Sophie Dubois", "Liam Johnson", "Emma Martinez", "Noah Lee", "Olivia Kim", "William Chen", "Ava Wang", "James Brown", "Isabella Nguyen", "Benjamin Wilson", "Mia Li", "Lucas Anderson", "Charlotte Liu", "Alexander Taylor", "Amelia Patel", "Daniel Garcia", "Sophia Kim" };
                var accountHolderName = accountHolderNames[random.Next(0, accountHolderNames.Length)];
                return accountHolderName;
            }
            static string GenerateRandomAccountType()
            {
                string[] accountTypes = { "Savings", "Checking", "Money Market", "Certificate of Deposit", "Retirement" };
                return accountTypes[random.Next(0, accountTypes.Length)];
            }
            static DateTime GenerateRandomDateOpened()
            {
                DateTime startDate = new(DateTime.Today.Year - MaxYearsBack, 1, 1);
                int daysRange = (DateTime.Today - startDate).Days;
                DateTime randomDate = startDate.AddDays(random.Next(daysRange));
                if (randomDate.Year == DateTime.Today.Year && randomDate >= DateTime.Today)
                {
                    randomDate = randomDate.AddDays(-1);
                }
                return randomDate;
            }
            static string GenerateSecurePassword()
            {
                const int passwordLength = 12;
                const string validChars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#$%^&*()";
                StringBuilder password = new StringBuilder();
                using (RNGCryptoServiceProvider rng = new RNGCryptoServiceProvider())
                {
                    byte[] uintBuffer = new byte[sizeof(uint)];
                    while (passwordLength > password.Length)
                    {
                        rng.GetBytes(uintBuffer);
                        uint num = BitConverter.ToUInt32(uintBuffer, 0);
                        password.Append(validChars[(int)(num % (uint)validChars.Length)]);
                    }
                }
                return password.ToString();
            }
            static void LogException(Exception ex)
            {
                // Implement a secure logging mechanism here
                // For example, log to a file, database, or external logging service
                Console.WriteLine($"Logged exception: {ex.Message}");
            }
        }
    }

    ```

1. Implementieren Sie die vorgeschlagenen Updates, um die Codesicherheit für Ihre Datei `Program.cs` zu verbessern.

1. Vergewissern Sie sich, dass die Änderungen keine Fehler verursacht haben. Erstellen Sie dazu Ihre Lösung und führen Sie sie aus.

## Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um Vorschläge zur Verbesserung der Codesicherheit in einer Beispielanwendung zu generieren. Sie haben Prompts entwickelt, die den GitHub Copilot anweisen, Vorschläge zur Verbesserung der Authentifizierung, des Datenschutzes, der Protokollierung und anderer sicherheitsrelevanter Themen zu machen. Sie haben die vorgeschlagenen Updates zur Verbesserung der Sicherheit der Klasse BankAccount und der „Program“-Klasse im Projekt **APL2007M5BankAccount-Security** implementiert.
