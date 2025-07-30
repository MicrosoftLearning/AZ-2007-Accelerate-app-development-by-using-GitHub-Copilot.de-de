---
demo:
  title: 'Demo: Verbessern der Codesicherheit und -leistung mithilfe von GitHub Copilot Chat'
  module: 'Module 5: Implement code improvements using GitHub Copilot tools'
---

# Demo: Verbessern der Codesicherheit und -leistung mithilfe von GitHub Copilot Chat

## Anweisungen

Die Aktivitäten der Demo sind für eine Umgebung konzipiert, die die folgenden Ressourcen umfasst:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Codezuverlässigkeit und -leistung sind eng verbundene Aspekte der Softwarequalität. Sie hängen wie folgt miteinander zusammen:

- Verbesserungen in einem Bereich können sich positiv auf den anderen Bereich auswirken.
- Mängel in einem Bereich können zu Problemen mit dem anderen Bereich führen.

> [!IMPORTANT]
> Erläutern Sie den Kursteilnehmenden, dass es in dieser Demo nicht um bewährte Methoden für die Entwicklung von zuverlässigem oder leistungsfähigem Code geht. Stattdessen geht es darum, wie GitHub Copilot Chat dazu genutzt werden kann, Verbesserungsvorschläge für die Codezuverlässigkeit und -leistung einer Beispielanwendung zu generieren. Die Vorschläge stellen keine bewährten Methoden oder umfassenden Lösungen für Codezuverlässigkeit und -leistung dar. Fachkräfte in der Entwicklung sollten die Vorschläge von GitHub Copilot Chat nach eigenem Ermessen und auf der Grundlage der eigenen Kompetenzen bewerten und implementieren. Wenn Sie Vorschläge von GitHub Copilot implementieren, heißt das nicht, dass keine gründlichen Codeüberprüfungen und Tests mehr erforderlich sind.

#### Codezuverlässigkeit und -leistung

Fachkräfte in der Entwicklung müssen ein Gleichgewicht zwischen Codezuverlässigkeit und -leistung anstreben. Eine erfolgreiche Balance resultiert in folgenden gegenseitigen Vorteilen:

- Anwendungen, die funktionale Anforderungen erfüllen
- Anwendungen mit einer nahtlosen und effizienten Benutzererfahrung

In den folgenden Abschnitten finden Sie eine Übersicht über die Codezulässigkeit und -leistung sowie andere Faktoren, die Ihre Kursteilnehmenden beachten sollten.

##### Untersuchen der Codezuverlässigkeit

Codezuverlässigkeit bezieht sich auf die Wahrscheinlichkeit, dass Software unter bestimmten Bedingungen und für einen bestimmten Zeitraum ordnungsgemäß funktioniert. Durch die Verbesserung der Codezuverlässigkeit können Sie sicherstellen, dass Ihre Software wie erwartet ausgeführt wird und die Benutzeranforderungen erfüllt.

Fachkräfte in der Entwicklung können folgende Faktoren berücksichtigen, wenn sie an der Verbesserung der Codezuverlässigkeit arbeiten:

- Mögliche Probleme: Die Identifizierung möglicher Probleme im Code kann dazu beitragen, Fehler zu vermeiden. Die Identifizierung möglicher Probleme sollte die Überprüfung des Codes auf häufige Probleme und deren proaktive Behandlung umfassen.
- Tests: Angemessene Tests sind unverzichtbar, um Fehler zu identifizieren und zu beheben, bevor das Produkt veröffentlicht wird. Angemessene Tests sollten Komponententests, Integrationstests, Systemtests und Akzeptanztests umfassen.
- Ausnahmenbehandlung: Mechanismen für eine ordnungsgemäße Ausnahmenbehandlung können verhindern, dass ein System ausfällt, wenn unerwartete Bedingungen auftreten.

> [!NOTE]
> Stellen Sie vor der Arbeit an der Codezuverlässigkeit zunächst eine hohe Codequalität sicher. Eine hohe Codequalität kann durch Code-Refactoring sowie durch Standards und Richtlinien erreicht werden.

Es gibt noch weitere Faktoren, die sich auf die Codezuverlässigkeit auswirken. Einige dieser Faktoren liegen nicht in der Verantwortung von Fachkräften in der Entwicklung, andere sollten vor oder nach der Codezuverlässigkeit berücksichtigt werden. Zu diesen anderen Faktoren zählen folgende:

- Entwicklungsmethoden: Die Einhaltung bewährter Methoden für die Softwareentwicklung (z. B. Codeüberprüfungen, Paarprogrammierung und Einhaltung von Programmierstandards) kann zu zuverlässigerem Code führen.
- Zuverlässigkeitsziele und -metriken: Klare Zuverlässigkeitsziele und entsprechende Metriken können zur Entwicklung zuverlässiger Software beitragen.
- Dokumentation: Eine umfassende Dokumentation kann dabei helfen, das System und seine Komponenten besser zu verstehen, was bei der Wartung und Problembehandlung für das System unerlässlich ist.
- Abhängigkeiten: Externe Bibliotheken und Dienste, von denen der Code abhängig ist, können sich auf die Zuverlässigkeit auswirken. Ein Fehler in einem Drittanbieterdienst kann einen Fehler in einem abhängigen System nach sich ziehen.
- Leistung: Auch Leistungsprobleme können sich auf die Zuverlässigkeit auswirken. Daher muss sichergestellt sein, dass das System unter verschiedenen Lasten gut funktioniert.
- Überwachung und Problembehandlung: Kontinuierliche Überwachung und ein zuverlässiger Leitfaden zur Problembehandlung können dazu beitragen, die Zuverlässigkeit eines Diensts aufrechtzuerhalten, indem Probleme schnell identifiziert und behoben werden.
- Entwurf und Architektur: Ein gut gestaltetes System mit einer soliden Architektur kann Fehler ordnungsgemäß behandeln und trotz Fehlern in einigen Komponenten weiter funktionieren.
- Externe Faktoren: Probleme mit der Zuverlässigkeit nach der Veröffentlichung können durch externe Faktoren wie Hardware- und Betriebssystemupdates bedingt sein, die ggf. zu Kompatibilitätsproblemen oder Systemfehlern führen.

Die Verbesserung der Zuverlässigkeit Ihres Codes kann dazu beitragen, die Wahrscheinlichkeit von Fehlern und unerwartetem Verhalten zu verringern.

##### Untersuchen der Codeleistung

Codeleistung bezieht sich darauf, wie effizient ein Programm oder eine Anwendung ausgeführt wird – insbesondere hinsichtlich Geschwindigkeit, Speicherauslastung und allgemeinem Ressourcenbedarf. Um die Codeleistung sicherzustellen oder zu verbessern, können Fachkräfte in der Entwicklung verschiedene Maßnahmen ergreifen:

Fachkräfte in der Entwicklung sollten folgende Faktoren berücksichtigen, wenn sie an der Verbesserung der Codeleistung arbeiten:

- Optimieren von Algorithmen: Wählen Sie die effizientesten Algorithmen und Datenstrukturen für die jeweilige Aufgabe aus. Selbst kleine Verbesserungen können sich erheblich auf die Leistung auswirken.
- Vermeiden unnötiger Berechnungen: Speichern Sie die Ergebnisse aufwendiger Vorgänge nach Möglichkeit zwischen, und vermeiden Sie redundante Berechnungen.
- Verwenden von Multithreading und asynchroner Programmierung: Nutzen Sie moderne CPU-Architekturen, indem Sie Aufgaben parallelisieren und E/A-Vorgänge asynchron ausführen.
- Minimieren von E/A-Vorgängen: E/A-Vorgänge auf Datenträgern und im Netzwerk können langsam sein. Daher ist es wichtig, diese Vorgänge zu minimieren oder asynchron auszuführen, um den Hauptausführungsthreads möglichst nicht zu blockieren.

> [!NOTE]
> Stellen Sie vor der Arbeit an der Codeleistung zunächst eine hohe Codequalität sicher. Eine hohe Codequalität kann durch Code-Refactoring sowie durch Standards und Richtlinien erreicht werden.

Es gibt noch weitere Faktoren, die sich auf die Codeleistung auswirken. Einige dieser Faktoren liegen nicht in der Verantwortung von Fachkräften in der Entwicklung, andere sollten vor oder nach der Arbeit an der Codeleistung berücksichtigt werden. Zu diesen anderen Faktoren zählen folgende:

- Profilerstellung und Durchführung von Vergleichstests: Verwenden Sie Profilerstellungstools, um Leistungsengpässe zu identifizieren. Vergleichstests vor und nach dem Vornehmen von Änderungen ermöglichen eine Quantifizierung der Auswirkungen von Optimierungen.
- Effiziente Verwaltung des Arbeitsspeichers: Verwenden Sie Profilerstellungstools für den Arbeitsspeicher, um Lecks zu erkennen und sicherzustellen, dass Arbeitsspeicher ordnungsgemäß zugeordnet und die Zuordnung ordnungsgemäß aufgehoben wird.
- Optimierung von Datenbankinteraktionen: Verwenden Sie effiziente Abfragen, eine ordnungsgemäße Indizierung sowie Datenbankzwischenspeicherung, um den Mehraufwand für Datenbankinteraktionen zu minimieren.
- Code Reviews: Überprüfen Sie Code regelmäßig auf Leistungsprobleme. Peer Reviews können dazu beitragen, Ineffizienzen zu erkennen, die die ursprüngliche Fachkraft in der Entwicklung möglicherweise übersehen hat.
- Bleiben Sie auf dem neuesten Stand: Verwenden Sie die neuesten Versionen von Programmiersprachen, Bibliotheken und Frameworks, da sie häufig Leistungsverbesserungen enthalten.
- Weiterbildung und Zusammenarbeit: Informieren Sie sich über bewährte Methoden für die Leistungsoptimierung, und arbeiten Sie mit anderen Fachkräften in der Entwicklung zusammen, um aus deren Erfahrungen zu lernen.

Wenn Fachkräfte in der Entwicklung sich auf diese Bereiche konzentrieren, können sie die Leistung ihres Codes erheblich verbessern, was in schnelleren, reaktionsfähigeren Anwendungen resultiert. Die Leistungsoptimierung ist ein fortlaufender Prozess, und es ist wichtig, die Leistung Ihrer Anwendungen kontinuierlich zu überwachen und zu verbessern.

GitHub Copilot Chat kann Vorschläge zur Optimierung von Algorithmen unterbreiten sowie dazu beitragen, unnötige Berechnungen zu reduzieren, Multithreading und asynchrone Programmierung zu nutzen und E/A-Vorgänge zu minimieren, um die Leistung Ihres Codes zu verbessern.

### Entwickeln von Prompts für GitHub Copilot Chat

Die Prompts, die Sie für GitHub Copilot Chat schreiben, müssen einen klar definierten Kontext und eine klar definierte Absicht haben. Berücksichtigen Sie bei der Entwicklung Ihrer Prompts die folgenden Vorschläge:

- Definieren Sie einen äußeren Kontext, der auf einer höheren Ebene angesiedelt ist als der Code, den Sie aktualisieren möchten. Wenn Sie zum Beispiel eine Methode verbessern möchten, geben Sie die Klasse oder Datei, die die Methode enthält, als äußeren Kontext an. Identifizieren Sie die Methode als inneren Kontext.
- Verwenden Sie Chatteilnehmer und Chatvariablen, um den Kontext anzugeben. Sie können die Chat-Variablen `#file:` und `#selection` verwenden, um den spezifischen Code zu identifizieren, auf den Sie sich konzentrieren. Gegebenenfalls können Sie auch den gesamten Arbeitsbereich (`@workspace`) einschließen. Nehmen Sie im natürlichsprachlichen Teil Ihres Prompts Bezug auf die Datei- oder Codeauswahl.
- Die Absicht muss klar, präzise und spezifisch sein. Ihr Prompt muss die Art der Verbesserung enthalten, die Sie erreichen möchten.

In diesem Teil der Demo überprüfen Sie das Projekt **APL2007M5BankAccount-Reliability** und erstellen drei Prompts für GitHub Copilot Chat. Die Prompts konzentrieren sich auf die Verbesserung der Codezuverlässigkeit und -leistung.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie die Beispiel-App **APL2007M5BankAccount-Reliability** in Visual Studio Code.

1. Öffnen Sie die Ansicht „Projektmappen-Explorer“.

1. Erweitern Sie das Projekt **BankAccount**, und überprüfen Sie dann die Codedateien **BankAccount.cs** und **Program.cs**.

    Die Datei **BankAccount.cs** enthält den Code für die `BankAccount`-Klasse. Diese stellt ein Bankkonto mit Eigenschaften wie „AccountNumber“, „Balance“, „AccountHolderName“, „AccountType“ und „DateOpened“ dar. Sie enthält die folgenden Methoden:

    - Credit(double amount): Diese Methode erhöht den Saldo des Kontos um den angegebenen Betrag.
    - Debit(double amount): Diese Methode verringert den Saldo des Kontos um den angegebenen Betrag. Ist der Saldo kleiner als der Betrag, wird eine Ausnahme mit einer Meldung ausgelöst, die darauf hinweist, dass der Saldo für die Belastung nicht ausreicht.
    - GetBalance(): Diese Methode gibt den aktuellen Saldo des Kontos zurück.
    - Transfer(BankAccount toAccount, double amount): Diese Methode überweist einen angegebenen Betrag vom aktuellen Konto auf das Zielkonto (toAccount). Ist der Saldo kleiner als der Betrag, wird eine Ausnahme mit einer Meldung ausgelöst, die darauf hinweist, dass der Saldo für die Überweisung nicht ausreicht. Wenn der Name der Person im Besitz des Kontos (AccountHolderName) nicht übereinstimmt und der Betrag den Wert 500 übersteigt, wird eine Ausnahme mit einer Meldung ausgelöst, die darauf hinweist, dass der Überweisungsbetrag die Obergrenze für unterschiedliche Kontobesitzende übersteigt.
    - PrintStatement(): Diese Methode gibt die Kontonummer (AccountNumber) und den Saldo in der Konsole aus.
    - CalculateInterest(double interestRate): Diese Methode berechnet die Zinsen für den aktuellen Saldo unter Verwendung des angegebenen Zinssatzes (interestRate).

    Die Datei **Program.cs** enthält eine Konsolenanwendung, die ein Bankensystem simuliert. Sie enthält folgende Methoden:

    - Main-Methode: Der Einstiegspunkt der Anwendung. Sie erstellt eine Liste mit Bankkonten und simuliert Transaktionen und Überweisungen für diese Konten.
    - CreateBankAccounts-Methode: Diese Methode erstellt eine bestimmte Anzahl von Bankkonten mit zufälligen Anfangsguthaben, Kontobesitzernamen, Kontotypen und Eröffnungsdaten. Sie verwendet einen Try-Catch-Block, um Ausnahmen zu behandeln, die ggf. bei der Kontoerstellung auftreten.
    - SimulateTransactions-Methode: Diese Methode simuliert eine bestimmte Anzahl von Transaktionen für die einzelnen Konten in der bereitgestellten Liste. Jede Transaktion wird mit einem zufälligen Dollarbetrag durchgeführt und ist entweder eine Gutschrift (Einzahlung) oder eine Lastschrift (Auszahlung) – je nachdem, ob der Betrag positiv oder negativ ist.
    - SimulateTransfers-Methode: Diese Methode ist identisch mit der SimulateTransactions-Methode. Sie scheint für die Simulation von Überweisungen zwischen Konten gedacht zu sein, dupliziert aber derzeit einfach nur die Funktionalität der SimulateTransactions-Methode.
    - GenerateRandomDollarAmount-Methode: Diese Methode generiert einen zufälligen Dollarbetrag innerhalb eines angegebenen Bereichs. Der Bereich und die Berechnungsmethode hängen davon ab, ob der Betrag für einen Kontensaldo oder für eine Transaktion vorgesehen ist.
    - GenerateRandomAccountHolder-Methode: Diese Methode wählt einen zufälligen Kontobesitzernamen aus einer vordefinierten Liste aus.
    - GenerateRandomAccountType-Methode: Diese Methode wählt einen zufälligen Kontotyp aus einer vordefinierten Liste aus.
    - GenerateRandomDateOpened-Methode: Diese Methode generiert ein zufälliges Datum innerhalb eines angegebenen Bereichs für das Kontoöffnungsdatum.

1. Nehmen Sie sich einen Moment Zeit, um die Prompts zu beschreiben, die Ihnen ggf. dabei helfen können, die Codezuverlässigkeit und -leistung zu verbessern.

    Entwickeln Sie Prompts für die BankAccount-Klasse und die Program-Klasse. Berücksichtigen Sie beim Entwickeln Ihrer Prompts die folgenden Zuverlässigkeits- und Leistungsfaktoren:

    - Mögliche Probleme: Die Identifizierung möglicher Probleme im Code kann dazu beitragen, Fehler zu vermeiden. Dies schließt die Überprüfung des Codes auf häufige Probleme und deren proaktive Behandlung ein.
    - Tests: Angemessene Tests sind unverzichtbar, um Fehler zu identifizieren und zu beheben, bevor das Produkt veröffentlicht wird. Dies schließt Komponententests, Integrationstests, Systemtests und Akzeptanztests ein.
    - Ausnahmenbehandlung: Mechanismen für eine ordnungsgemäße Ausnahmenbehandlung können verhindern, dass ein System ausfällt, wenn unerwartete Bedingungen auftreten.

    - Optimieren von Algorithmen: Wählen Sie die effizientesten Algorithmen und Datenstrukturen für die jeweilige Aufgabe aus. Selbst kleine Verbesserungen können sich erheblich auf die Leistung auswirken.
    - Vermeiden unnötiger Berechnungen: Speichern Sie die Ergebnisse aufwendiger Vorgänge nach Möglichkeit zwischen, und vermeiden Sie redundante Berechnungen.
    - Verwenden von Multithreading und asynchroner Programmierung: Nutzen Sie moderne CPU-Architekturen, indem Sie Aufgaben parallelisieren und E/A-Vorgänge asynchron ausführen.
    - Minimieren von E/A-Vorgängen: E/A-Vorgänge auf Datenträgern und im Netzwerk können langsam sein. Daher ist es wichtig, diese Vorgänge zu minimieren oder asynchron auszuführen, um den Hauptausführungsthreads möglichst nicht zu blockieren.

    Bei diesem Projekt können Sie folgende Prompts verwenden, um Verbesserungsvorschläge für die Codezuverlässigkeit zu generieren:

    Prompt: `@workspace /explain How can I improve exception handling the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I reduce unexpected issues for the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve unit test support for the [selected code]?` (Anfügen von BankAccount.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I avoid future bugs or issues in the [selected code]?` (Anfügen von Program.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve exception handling for the [selected code]?` (Anfügen von Program.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve the efficiency of algorithms or data structures for the [selected code]?` (Anfügen von Program.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve performance with asynchronous tasks or methods in the [selected code]?` (Anfügen von Program.cs an den Chatkontext)

    Prompt: `@workspace /explain How can I improve unit test support for the [selected code]?` (Anfügen von BankAccountTests.cs und BankAccount.cs an den Chatkontext)

1. Wählen Sie zwei Prompts aus, die Sie verwenden können, um die BankAccount-Klasse während dieser Demo zu verbessern.

    Versuchen Sie, für die BankAccount-Klasse Prompts auszuwählen, die sich auf Zuverlässigkeit konzentrieren.

1. Wählen Sie zwei Prompts aus, die Sie verwenden können, um die Program-Klasse während dieser Demo zu verbessern.

    Versuchen Sie, für die Program-Klasse einen Prompt auszuwählen, der sich auf die Zuverlässigkeit konzentriert, und einen Prompt, der sich auf die Leistung konzentriert.

### Verbessern der Codezuverlässigkeit der BankAccount-Klasse mithilfe von GitHub Copilot Chat

Die Gewährleistung der Zuverlässigkeit von Produktionscode ist bei jedem Softwareprojekt unerlässlich. Die Beispiel-App „APL2007M5BankAccount-Reliability“ verwendet die Program-Klasse, um das Bankenszenario zu simulieren, aber es ist die BankAccount-Klasse, die in einer Produktionsumgebung bereitgestellt wird. Die Verbesserung der Zuverlässigkeit der BankAccount-Klasse trägt dazu bei, dass sie wie erwartet funktioniert und die Benutzeranforderungen erfüllt.

GitHub Copilot Chat kann verwendet werden, um die Zuverlässigkeit Ihres Codes zu verbessern. Mit Ihren Prompts können Sie GitHub Copilot anweisen, Vorschläge zu generieren, die die Behandlung von Ausnahmen verbessern, unerwartete Probleme reduzieren und die Unterstützung von Komponententests verbessern. Sie können auch weiter gefasste Prompts erstellen, um allgemeine Vorschläge zur Verbesserung der Zuverlässigkeit des Codes anzufordern. Eine Kombination aus spezifischen und allgemeinen Prompts kann Ihnen dabei helfen, Bereiche mit Verbesserungsbedarf zu identifizieren und die erforderlichen Änderungen zu implementieren.

> [!NOTE]
> Die Implementierung und das Testen vorgeschlagener Aktualisierungen dauert eine gewisse Zeit, und Zeit ist während dieser Demo möglicherweise ein Faktor. Die Wahl von Prompts, die sich auf bestimmte Verbesserungsbereiche konzentrieren, kann Ihnen beim Zeitmanagement helfen. Zu weit gefasste Prompts können eine Vielzahl von Vorschlägen oder komplexe Vorschläge generieren, die sich nur schwer in kurzer Zeit auswerten und implementieren lassen. Sollten Sie feststellen, dass die vorgeschlagenen Aktualisierungen zu weit gefasst oder zu komplex sind, können Sie Ihre Prompts mit spezifischeren Details aktualisieren.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Stellen Sie sicher, dass das Projekt ohne Fehler erstellt und ausgeführt wird.

    Warnungen sind zulässig, solange die Anwendung ausgeführt wird, aber unbehandelte Fehler, die zum Absturz der Anwendung führen, müssen behoben werden, bevor Sie mit der Arbeit mit GitHub Copilot-Chat beginnen.

1. Öffnen Sie die Datei „BankAccount.cs“ in Visual Studio Code, und wählen Sie dann den gesamten Code in der Datei aus.

1. Öffnen Sie die Chatansicht.

1. Fügen Sie in der Chatansicht dem Chatkontext relevante Dateien hinzu, und geben Sie dann Ihren Prompt ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie führen die folgenden Aktionen durch:

    - Sie öffnen die Datei BankAccount.cs und markieren den gesamten Code.
    - Sie wählen den folgenden Prompt: `@workspace /explain How can I improve exception handling in the BankAccount.cs file?`
    - Sie öffnen die Chatansicht und fügen die Dateien BankAccount.cs und Program.cs an den Chatkontext an.
    - Sie geben den Prompt in der Chatansicht ein.

    In diesem Fall schlägt GitHub Copilot-Chat Updates vor, die der folgenden Antwort ähneln:

    *Um die Ausnahmebehandlung in der Datei BankAccount.cs zu verbessern, sollten Sie die folgenden Vorschläge berücksichtigen:*

    *1. **Verwenden spezifischer Ausnahmen:** Verwenden Sie spezifischere Ausnahmen, anstatt die `Exception`-Basisklasse auszulösen. Dadurch wird es für den aufrufenden Code einfacher, bestimmte Fehlertypen zu erkennen und zu behandeln. Sie können beispielsweise eine Ausnahme für einen ungültigen Vorgang (InvalidOperationException) auslösen, wenn versucht wird, eine Lastschrift oder eine Überweisung mit unzureichendem Saldo durchzuführen.*

    *2. **Einschließen weiterer Informationen in Ausnahmemeldungen:** Ausnahmemeldungen können ggf. weitere Details zu dem nicht erfolgreichen Vorgang bereitstellen. In der `Debit`-Methode kann die Ausnahmemeldung beispielsweise den Lastschriftbetrag und den aktuellen Saldo enthalten.*

    *3. **Verwenden benutzerdefinierter Ausnahmen:** Für spezifische, individuelle Fehlerbedingungen Ihrer Anwendung können ggf. benutzerdefinierte Ausnahmeklassen erstellt werden. Durch die Erstellung benutzerdefinierter Ausnahmen können Sie weitere Informationen zu der Fehlerbedingung kapseln und die Selbstdokumentation Ihres Codes verbessern.*

    *Hier erfahren Sie, wie Sie die `Debit`-Methode mit diesen Vorschlägen verbessern können:*

    ```csharp

    public void Debit(double amount)
    {
        if (Balance >= amount)
        {
            Balance -= amount;
        }
        else
        {
            throw new InvalidOperationException($"Insufficient balance for debit. Attempted to debit {amount}, but current balance is {Balance}.");
        }
    }

    ```

    *Und hier finden Sie ein Beispiel für eine benutzerdefinierte Ausnahmeklasse:*

    ```csharp

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

    ```

    *Anschließend können Sie diese benutzerdefinierte Ausnahme in der Debit-Methode auslösen:*

    ```csharp

    public void Debit(double amount)
    {
        if (Balance >= amount)
        {
            Balance -= amount;
        }
        else
        {
            throw new InsufficientFundsException(amount, Balance);
        }
    }

    ```

    *Dadurch kann der aufrufende Code „InsufficientFundsException“ abfangen und auf die Eigenschaften „AttemptedAmount“ und „CurrentBalance“ zugreifen, um die Fehlerbedingung effektiver zu behandeln.*

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, um die Codezuverlässigkeit für die `BankAccount`-Klasse zu verbessern.

1. Vergewissern Sie sich, dass die Änderungen keine Fehler verursacht haben, bevor Sie fortfahren. Erstellen Sie dazu Ihre Lösung, und führen Sie sie aus.

    > [!TIP]
    > Im obigen Beispiel wurden in der Chatansicht Codeschnipsel bereitgestellt, die ein einzelnes Beispiel der vorgeschlagenen Aktualisierung (Verwendung spezifischer Ausnahmen, Einbeziehung weiterer Informationen in die Ausnahmemeldung und Erstellung benutzerdefinierter Ausnahmen) implementieren. Versuchen Sie, nach der Implementierung von Vorschlägen Codezeilenvervollständigungen zu verwenden, um neuen Code zu generieren, der die Aktualisierung dupliziert. In diesem Beispiel können Codezeilenvervollständigungen verwendet werden, um weitere benutzerdefinierte Ausnahmeklassen zu erstellen. Anschließend können Sie Codezeilenvervollständigungen verwenden, um die anderen Methoden mit den neuen benutzerdefinierten Ausnahmen zu aktualisieren. Sie können auch den ursprünglichen Prompt erneut ausführen, um weitere Vorschläge zu erhalten.

1. Wählen Sie den gesamten Code in der Datei BankAccount.cs aus.

1. Öffnen Sie die Chatansicht.

1. Verwenden Sie die Schaltfläche **Kontext anfügen**, um dem Chatkontext relevante Dateien hinzuzufügen, und geben Sie dann Ihren zweiten Prompt „Zuverlässigkeit“ ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Wenn Sie in der Chatansicht beispielsweise `@workspace /explain How can I reduce unexpected issues for the selected code?` eingegeben haben, schlägt GitHub Copilot Chat Aktualisierungen vor, die in etwa wie in der folgenden Antwort aussehen:

    *Um unerwartete Probleme in der Klasse BankAccount zu reduzieren, können Sie die folgenden Verbesserungen implementieren:*

    *1. Verwenden einer Enumeration für den Kontotyp: Anstatt eine Zeichenfolge für den Kontotyp zu verwenden und zu überprüfen, ob es sich um ein Sparkonto oder um ein Kontokorrentkonto handelt, empfiehlt es sich gegebenenfalls, eine Enumeration zu verwenden. Dadurch lassen sich potenzielle Probleme beim Zeichenfolgenvergleich (z. B. Unterscheidung nach Groß-/Kleinschreibung) verhindern, und der Kontotyp kann auf vordefinierte Werte beschränkt werden.*

    ```csharp

    public enum AccountType
    {
        Savings,
        Current
    }

    ```

    *2. Verwenden von Dezimalwerten für geldbezogene Werte: Es wird im Allgemeinen empfohlen, für geldbezogene Werte anstelle des Double-Typs den Dezimaltyp zu verwenden, um Rundungsfehler zu vermeiden.*

    *3. Hinzufügen weiterer Validierungen: Sie können in Ihren Methoden ggf. weitere Validierungen hinzufügen. In der Transfer-Methode können Sie beispielsweise überprüfen, ob das Zielkonto (toAccount) NULL ist, bevor Sie mit der Überweisung fortfahren.*

    *4. Verwenden von Konstanten für magische Zahlen: In Ihrer Transfer-Methode gibt es eine magische Zahl (500). Es wäre besser, sie am Anfang Ihrer Klasse als Konstante mit einem aussagekräftigen Namen zu definieren.*

    ```csharp
    private const double MaxTransferAmountForDifferentOwners = 500;
    ```

    *5. Benutzerdefinierte Ausnahme für den Überweisungsgrenzwert: Anstatt eine allgemeine Ausnahme auszulösen, wenn der Überweisungsbetrag den Grenzwert für unterschiedliche Kontobesitzer überschreitet, sollten Sie eine benutzerdefinierte Ausnahme wie „ExceededTransferLimitException“ erstellen.*

    *6. Protokollierung: Fügen Sie der Anwendung ggf. eine Protokollierung hinzu. Dies kann Ihnen dabei helfen, den Ablauf Ihrer Anwendung besser zu verstehen und Probleme zu diagnostizieren.*

    *7. Komponententests: Schreiben Sie Komponententests für Ihre Methoden, um sicherzustellen, dass sie sich in verschiedenen Szenarien wie erwartet verhalten. Dies kann Ihnen dabei helfen, Probleme frühzeitig im Entwicklungsprozess zu erfassen.*

1. Achten Sie auf den Umfang und die Breite der von GitHub Copilot Chat bereitgestellten Vorschläge.

    Einige Prompts generieren möglicherweise eine große Anzahl von Vorschlägen, die sich auf einen großen Bereich auswirken. Überprüfen Sie in diesem Fall, ob ein einzelnes Vorschlagselement verwendet werden kann, um einen neuen Prompt zu definieren, der eine spezifischere Absicht und/oder einen spezifischeren Kontext bereitstellt.

1. Verwenden Sie die Liste der Vorschläge, um einen Prompt zu erstellen, die eine detailliertere Absicht und/oder einen detaillierteren Kontext enthält.

    Jede der von GitHub Copilot Chat bereitgestellten Vorschläge kann separat untersucht und implementiert werden. Es empfiehlt sich gegebenenfalls, die Liste von oben nach unten abzuarbeiten, um sich jeweils auf eine einzelne Verbesserung zu konzentrieren.

1. Geben Sie Ihren detaillierten Prompt in die Chatansicht ein, und überprüfen Sie dann die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Angenommen, Sie haben das zweite Beispiel für den Zuverlässigkeitsprompt verwendet. Die Antwort von GitHub Copilot Chat enthält das folgende Vorschlagselement:

    *Hinzufügen weiterer Validierungen: Sie können in Ihren Methoden ggf. weitere Validierungen hinzufügen. In der Transfer-Methode können Sie beispielsweise überprüfen, ob das Zielkonto (toAccount) NULL ist, bevor Sie mit der Überweisung fortfahren.*

    Auf der Grundlage dieses Vorschlags können Sie einen neuen Prompt erstellen, der sich auf das Hinzufügen weiterer Validierungen zur Transfer-Methode konzentriert. Sie können die Transfer-Methode auswählen und dann den folgenden Prompt in die Chatansicht eingeben:

    `@workspace /explain #file:BankAccount.cs How can I improve method validations for the selected code?`

    In diesem Fall schlägt GitHub Copilot Chat Aktualisierungen vor, die in etwa wie in der folgenden Antwort aussehen:

    *Der von Ihnen bereitgestellte Code ist gut strukturiert und folgt bewährten Methoden für die Ausnahmenbehandlung. Es gibt jedoch noch ein paar Bereiche, in denen Sie Verbesserungen vornehmen können:*

    *1. Konsolidieren der Validierungslogik: Sie können eine separate Validierungsklasse oder -methode für die gesamte Überprüfungslogik erstellen. Dadurch wäre Ihre BankAccount-Klasse übersichtlicher und stärker auf ihre Hauptaufgaben fokussiert.*

    *2. Verwenden benutzerdefinierter Validierungsattribute: Für einen Teil der Validierung können benutzerdefinierte Validierungsattribute verwendet werden. Dadurch könnten Sie die Eigenschaften kommentieren, die validiert werden müssen, und die Validierungslogik getrennt von der Geschäftslogik behandeln.*

    *3. Verwenden von Fluent Validation: Fluent Validation ist eine .NET-Bibliothek, die eine Fluent-Schnittstelle und Lambda-Ausdrücke für die Erstellung von Validierungsregeln verwendet. Dies kann Ihren Validierungscode intuitiver und besser lesbar machen.*

    *4. Vermeiden magischer Zahlen: Ihre Transfer-Methode enthält den hartcodierten Wert 500. Es empfiehlt sich grundsätzlich, magische Zahlen zu vermeiden und sie stattdessen am Anfang Ihrer Klasse als Konstanten mit aussagekräftigem Namen zu definieren.*

    Hier finden Sie ein Beispiel für die Implementierung einiger dieser Vorschläge:

    ```csharp

    public class BankAccount
    {
        private const double MaxTransferAmountForDifferentOwners = 500;
        // ...
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
            if (AccountHolderName != toAccount.AccountHolderName && amount > MaxTransferAmountForDifferentOwners)
            {
                throw new Exception("Transfer amount exceeds maximum limit for different account owners.");
            }
        }
    }

    ```

    Sie können die Vorschläge von GitHub Copilot Chat weiter durchgehen, bis Sie alle Verbesserungen implementiert haben, die Ihrer Meinung nach erforderlich sind.

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, erstellen Sie Ihre Lösung, und führen Sie sie aus, bevor Sie fortfahren.

    Beheben Sie alle Fehler, die ggf. durch die Änderungen entstanden sind, bevor Sie fortfahren.

### Verbessern der Codezuverlässigkeit und -leistung der Program-Klasse mithilfe von GitHub Copilot Chat

1. Öffnen Sie die Datei „Program.cs“ in Visual Studio Code, und wählen Sie dann den gesamten Code in der Datei aus.

1. Öffnen Sie die Datei „Program.cs“ in Visual Studio Code, und wählen Sie dann den gesamten Code in der Datei aus.

1. Öffnen Sie die Chatansicht.

1. Verwenden Sie in der Chatansicht die Schaltfläche **Kontext anfügen**, um dem Chatkontext relevante Dateien hinzuzufügen, und geben Sie dann Ihren Prompt ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    Wenn Sie in der Chatansicht beispielsweise `@workspace /explain How can I improve performance with asynchronous tasks or methods in the Program.cs file?` eingegeben haben, schlägt GitHub Copilot Chat Aktualisierungen vor, die in etwa wie in der folgenden Antwort aussehen:

    *Um die Leistung mit asynchronen Aufgaben oder Methoden in der Datei „Program.cs“ zu verbessern, können Sie die asynchrone Programmierung mit den Schlüsselwörtern „asynchron“ und „warten“ verwenden. Dadurch kann das Programm E/A-gebundene Vorgänge ausführen, ohne den Hauptthread zu blockieren, wodurch es reaktionsschneller und effizienter wird.*

    *Hier ist eine verbesserte Version der Datei Program.cs mit asynchronen Methoden:*

    ```csharp

    using System;
    using System.Collections.Generic;
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
            static async Task Main(string[] args)
            {
                List<BankAccount> accounts = await CreateBankAccountsAsync(NumberOfAccounts);
                await SimulateTransactionsAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
                await SimulateTransfersAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
            }
            static async Task<List<BankAccount>> CreateBankAccountsAsync(int numberOfAccounts)
            {
                List<BankAccount> accounts = new List<BankAccount>();
                int createdAccounts = 0;
                while (createdAccounts < numberOfAccounts)
                {
                    try
                    {
                        double initialBalance = GenerateRandomDollarAmount(true, minAccountStart, maxAccountStart);
                        string accountHolderName = GenerateRandomAccountHolder();
                        string accountType = GenerateRandomAccountType();
                        DateTime dateOpened = GenerateRandomDateOpened();
                        BankAccount account = new BankAccount($"Account {createdAccounts + 1}", initialBalance, accountHolderName, accountType, dateOpened);
                        accounts.Add(account);
                        createdAccounts++;
                    }
                    catch (Exception ex)
                    {
                        Console.WriteLine($"Account creation failed: {ex.Message}");
                    }
                    await Task.Yield(); // Yield control to allow other tasks to run
                }
                return accounts;
            }
            static async Task SimulateTransactionsAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                List<Task> tasks = new List<Task>();
                foreach (BankAccount account in accounts)
                {
                    tasks.Add(Task.Run(async () =>
                    {
                        for (int i = 0; i < numberOfTransactions; i++)
                        {
                            double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                            try
                            {
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
                            await Task.Yield(); // Yield control to allow other tasks to run
                        }
                        Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                    }));
                }
                await Task.WhenAll(tasks);
            }
            static async Task SimulateTransfersAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                List<Task> tasks = new List<Task>();
                foreach (BankAccount account in accounts)
                {
                    tasks.Add(Task.Run(async () =>
                    {
                        for (int i = 0; i < numberOfTransactions; i++)
                        {
                            double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                            try
                            {
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
                            await Task.Yield(); // Yield control to allow other tasks to run
                        }
                        Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                    }));
                }
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
                DateTime startDate = new DateTime(DateTime.Today.Year - MaxYearsBack, 1, 1);
                int daysRange = (DateTime.Today - startDate).Days;
                DateTime randomDate = startDate.AddDays(random.Next(daysRange));
                if (randomDate.Year == DateTime.Today.Year && randomDate >= DateTime.Today)
                {
                    randomDate = randomDate.AddDays(-1);
                }
                return randomDate;
            }
        }
    }

    ```

1. Implementieren Sie die vorgeschlagenen Aktualisierungen, um die Codeleistung (oder die Codezuverlässigkeit) der `Program`-Klasse zu verbessern.

1. Vergewissern Sie sich, dass die Änderungen keine Fehler verursacht haben, bevor Sie fortfahren. Erstellen Sie dazu Ihre Lösung, und führen Sie sie aus.

1. Wählen Sie den gesamten Code in der Datei „Program.cs“ aus, und geben Sie dann Ihren Zuverlässigkeitsprompt in die Chatansicht ein.

1. Überprüfen Sie die von GitHub Copilot Chat bereitgestellten Vorschläge.

    > [!NOTE]
    > Sie müssen die Aktualisierungsvorschläge, die GitHub Copilot auf der Grundlage dieses vierten Prompts generiert hat, nicht implementieren. Sie sollten sich die Vorschläge allerdings ansehen.

    Wenn Sie in der Chatansicht beispielsweise `@workspace /explain How can I improve exception handling for the selected code?` eingegeben haben, schlägt GitHub Copilot Chat Aktualisierungen vor, die in etwa wie in der folgenden Antwort aussehen:

    *Um die Ausnahmebehandlung in der Datei Program.cs zu verbessern, können Sie die folgenden Vorschläge implementieren:*

    *1. Spezifische Ausnahmetypen verwenden: Anstatt generische Ausnahmen abzufangen, fangen Sie bestimmte Ausnahmen nach Möglichkeit ab.*

    *2. Hinzufügen von weiterem Kontext zu Ausnahmen: Stellen Sie in den Ausnahmemeldungen mehr Kontext bereit, um das Debuggen zu vereinfachen.*

    *3. Protokollieren von Ausnahmen: Anstatt Ausnahmen nur in der Konsole auszugeben, sollten Sie diese zur besseren Rückverfolgbarkeit protokollieren.*

    *Hier ist eine verbesserte Version der Datei Program.cs mit besserer Ausnahmebehandlung:*

    ```csharp

    using System;
    using System.Collections.Generic;
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
            static async Task Main(string[] args)
            {
                List<BankAccount> accounts = await CreateBankAccountsAsync(NumberOfAccounts);
                await SimulateTransactionsAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
                await SimulateTransfersAsync(accounts, NumberOfTransactions, minTransactionAmount, maxTransactionAmount);
            }
            static async Task<List<BankAccount>> CreateBankAccountsAsync(int numberOfAccounts)
            {
                List<BankAccount> accounts = new List<BankAccount>();
                int createdAccounts = 0;
                while (createdAccounts < numberOfAccounts)
                {
                    try
                    {
                        double initialBalance = GenerateRandomDollarAmount(true, minAccountStart, maxAccountStart);
                        string accountHolderName = GenerateRandomAccountHolder();
                        string accountType = GenerateRandomAccountType();
                        DateTime dateOpened = GenerateRandomDateOpened();
                        BankAccount account = new BankAccount($"Account {createdAccounts + 1}", initialBalance, accountHolderName, accountType, dateOpened);
                        accounts.Add(account);
                        createdAccounts++;
                    }
                    catch (ArgumentException ex)
                    {
                        Console.WriteLine($"Account creation failed due to invalid argument: {ex.Message}");
                    }
                    catch (Exception ex)
                    {
                        Console.WriteLine($"Account creation failed: {ex.Message}");
                    }
                    await Task.Yield(); // Yield control to allow other tasks to run
                }
                return accounts;
            }
            static async Task SimulateTransactionsAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                List<Task> tasks = new List<Task>();
                foreach (BankAccount account in accounts)
                {
                    tasks.Add(Task.Run(async () =>
                    {
                        for (int i = 0; i < numberOfTransactions; i++)
                        {
                            double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                            try
                            {
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
                            catch (ArgumentException ex)
                            {
                                Console.WriteLine($"Transaction failed due to invalid argument: {ex.Message}");
                            }
                            catch (InsufficientBalanceException ex)
                            {
                                Console.WriteLine($"Transaction failed due to insufficient balance: {ex.Message}");
                            }
                            catch (Exception ex)
                            {
                                Console.WriteLine($"Transaction failed: {ex.Message}");
                            }
                            await Task.Yield(); // Yield control to allow other tasks to run
                        }
                        Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                    }));
                }
                await Task.WhenAll(tasks);
            }
            static async Task SimulateTransfersAsync(List<BankAccount> accounts, int numberOfTransactions, double minTransactionAmount, double maxTransactionAmount)
            {
                List<Task> tasks = new List<Task>();
                foreach (BankAccount account in accounts)
                {
                    tasks.Add(Task.Run(async () =>
                    {
                        for (int i = 0; i < numberOfTransactions; i++)
                        {
                            double transactionAmount = GenerateRandomDollarAmount(false, minTransactionAmount, maxTransactionAmount);
                            try
                            {
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
                            catch (ArgumentException ex)
                            {
                                Console.WriteLine($"Transaction failed due to invalid argument: {ex.Message}");
                            }
                            catch (InsufficientBalanceException ex)
                            {
                                Console.WriteLine($"Transaction failed due to insufficient balance: {ex.Message}");
                            }
                            catch (Exception ex)
                            {
                                Console.WriteLine($"Transaction failed: {ex.Message}");
                            }
                            await Task.Yield(); // Yield control to allow other tasks to run
                        }
                        Console.WriteLine($"Account: {account.AccountNumber}, Balance: {account.Balance.ToString("C")}, Account Holder: {account.AccountHolderName}, Account Type: {account.AccountType}");
                    }));
                }
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
                DateTime startDate = new DateTime(DateTime.Today.Year - MaxYearsBack, 1, 1);
                int daysRange = (DateTime.Today - startDate).Days;
                DateTime randomDate = startDate.AddDays(random.Next(daysRange));
                if (randomDate.Year == DateTime.Today.Year && randomDate >= DateTime.Today)
                {
                    randomDate = randomDate.AddDays(-1);
                }
                return randomDate;
            }
        }
    }

    ```

## Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um Verbesserungsvorschläge für die Codezuverlässigkeit und -leistung einer Beispielanwendung zu generieren. Sie haben Prompts entwickelt, um von GitHub Copilot Vorschläge anzufordern, die die Behandlung von Ausnahmen verbessern, unerwartete Probleme reduzieren und die Unterstützung von Komponententests verbessern. Außerdem haben Sie Prompts erstellt, bei denen die Verbesserung der Leistung mit asynchronen Aufgaben oder Methoden im Mittelpunkt stand.
