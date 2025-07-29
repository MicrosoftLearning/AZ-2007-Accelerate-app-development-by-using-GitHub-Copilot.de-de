---
demo:
  title: 'Demo: Generieren von Codeerklärungen mithilfe von GitHub Copilot Chat'
  module: 'Module 2: Generate documentation using GitHub Copilot tools'
---

# Demo: Generieren von Codeerklärungen mithilfe von GitHub Copilot Chat

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

GitHub Copilot Chat verwendet unterhaltungsbezogene KI-Unterstützung und intelligente Befehle, um Sie bei Codierungsaufgaben zu unterstützen. Ein Beispiel ist die Möglichkeit, unbekannten und komplexen Code zu erläutern.

Sie können GitHub Copilot Chat zum Generieren von Erklärungen für zahlreiche Gründe verwenden. Zum Beispiel:

- GitHub Copilot Chat kann einen gesamten Arbeitsbereich oder bestimmte Projektdateien erklären, wenn Sie einem vorhandenen Projekt beitreten.
- GitHub Copilot Chat kann bestimmte Codezeilen oder Abschnitte erläutern, wenn Code komplex oder schwer zu verstehen ist.
- GitHub Copilot Chat kann Fehler in Ihrem Code erklären und Möglichkeiten zur Behebung vorschlagen.
- GitHub Copilot Chat kann erläutern, wie Sie Ihrem Projekt Features hinzufügen und Codeausschnitte bereitstellen, die veranschaulichen, wie der neue Code implementiert wird.

### Erläuterungen zu Arbeitsbereichen und Projektdateien

GitHub Copilot Chat kann Ihnen helfen, neue Projekte oder bestimmte Projektdateien zu verstehen. Sie können eine Kombination aus `@workspace`, `/explain` und `#file` in der Chatansicht oder im Schnellchatfenster verwenden, um eine Erklärung für Ihr Projekt oder bestimmte Projektdateien zu generieren.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie den Ordner **APL2007M2Sample1** in Visual Studio Code.

    1. Öffnen Sie Visual Studio Code auf Ihrem PC.
    1. Wählen Sie in Visual Studio Code im Menü **Datei** die Option **Ordner öffnen** aus.
    1. Navigieren Sie zum Windows Desktop-Ordner, öffnen Sie den Ordner **SampleApps**, und suchen Sie den Ordner **APL2007M2Sample1**.
    1. Wählen Sie zunächst **APL2007M2Sample1** und dann **Ordner auswählen** aus.

    In der Visual Studio Code-Ansicht „EXPLORER“ sollte ein APL2007M2Sample1-Codeprojekt mit den folgenden Dateien angezeigt werden:

    - APL2007M2Sample1.csproj
    - APL2007M2Sample1.sln
    - App.xaml
    - App.xaml.cs
    - MainWindow.xaml
    - MainWindow.xaml.cs

1. Wählen Sie **Chat öffnen** auf der oberen Menüleiste von Visual Studio Code aus.

    Die Schaltfläche „Chat öffnen“ befindet sich auf der Menüleiste oben im Visual Studio Code-Fenster, direkt rechts neben dem Suchfeld. Es zeigt ein kleines GitHub Copilot-Logo an.

1. Verwenden Sie den folgenden Befehl, um Copilot Chat aufzufordern, das Projekt `APL2007M2Sample1` zu erläutern:

    ```plaintext
    @workspace Explain this project
    ```

1. Nehmen Sie sich kurz Zeit, um die Antwort in der Chatansicht zu überprüfen.

    GitHub Copilot Chat generiert eine Erläuterung eines APL2007M2Sample1-Projekts, die der folgenden Antwort ähnelt:

    > [!IMPORTANT]
    > GitHub Copilot Chat verwendet ein KI-Modell, um Antworten zu generieren. Die Antworten, die Sie erhalten, ähneln den Antworten, die in dieser Schulung angezeigt werden, sind aber nicht identisch.

1. Beachten Sie unten in der Chatansicht, dass GitHub Copilot Chat eine Folgefrage vorgeschlagen hat.

    Die Antwort, die Sie erhalten, kann eine andere Folgefrage enthalten.

    GitHub Copilot Chat erstellt einen Verlauf Ihrer Chatunterhaltung. Der Verlauf hilft GitHub Copilot Chat, Ihre Interessen zu verstehen. Während Sie einen Chatverlauf erstellen, lernt das KI-Modell aus Ihren Interaktionen und stellt relevantere Folgefragen bereit. „Zufällige“ Folgefragen zu untersuchen, wird nicht empfohlen.

1. Öffnen Sie die Datei `MainWindow.xaml.cs` im Editor.

1. Verwenden Sie den folgenden Befehl, um Copilot aufzufordern, die Datei `MainWindow.xaml.cs` zu erläutern:

    ```plaintext
    @workspace /explain #file:MainWindow.xaml.cs
    ```

1. Nehmen Sie sich kurz Zeit, um die Antwort in der Chatansicht zu überprüfen.

    Beachten Sie, dass GitHub Copilot Chat eine detaillierte Erläuterung der Datei `MainWindow.xaml.cs` generiert. Die Erläuterung enthält Informationen zu Zweck, Struktur und Schlüsselkomponenten der Datei. Möglicherweise ist auch ein Abschnitt vorhanden, in dem potenzielle Probleme und Verbesserungen beschrieben werden.

    GitHub Copilot Chat schlägt erneut eine Folgefrage vor.

    > [!IMPORTANT]
    > GitHub Copilot Chat speichert den Verlauf Ihrer Chatunterhaltung. Wenn Sie weiterhin Fragen stellen, werden die Antworten entsprechend optimiert. Der Kontext Ihrer Fragen (insbesondere in Bezug auf Ihr Codeprojekt) beeinflusst die nachfolgenden Antworten von GitHub Copilot Chat. Auf diese Weise können genauere und relevantere Antworten bereitgestellt werden. Es bedeutet auch, dass die Antwort, die Sie für eine bestimmte Frage erhalten, je nach Unterhaltungsverlauf variieren kann.

### Ausgewählte Codeerklärungen

Selbst erfahrene Entwickler stoßen auf Code, der schwer zu verstehen ist. Anstatt Zeit damit zu verbringen, komplexen Code zu entschlüsseln, können Sie GitHub Copilot Chat auffordern, eine Erklärung bereitzustellen. Die Chatansicht, der Inlinechat und intelligente Aktionen können jeweils verwendet werden, um Erklärungen für ausgewählte Codezeilen oder -abschnitte zu generieren.

In diesem Abschnitt der Demo verwenden Sie die intelligente Aktion **Erklären**, um eine Erläuterung ausgewählter Codezeilen zu generieren.

1. Stellen Sie sicher, dass Sie im Editor die Datei `MainWindow.xaml.cs` geöffnet haben.

1. Scrollen Sie nach unten bis zur `SumPageSizesAsync()`-Methode.

    ```csharp

    private async Task SumPageSizesAsync()
    {
        var stopwatch = Stopwatch.StartNew();
        IEnumerable<Task<int>> downloadTasksQuery =
            from url in _urlList
            select ProcessUrlAsync(url, _client);
        Task<int>[] downloadTasks = downloadTasksQuery.ToArray();
        int[] lengths = Task.WhenAll(downloadTasks);
        int total = lengths.Sum();
        await Dispatcher.BeginInvoke(() =>
        {
            stopwatch.Stop();
    
            _resultsTextBox.Text += $"\nTotal bytes returned:  {total:#,#}";
            _resultsTextBox.Text += $"\nElapsed time:          {stopwatch.Elapsed}\n";
        });
    }

    ```

1. Wählen Sie die folgenden Codezeilen aus, und verwenden Sie dann die intelligente Aktion **Erklären**, um eine Erläuterung zu generieren.

    Klicken Sie zur Auswahl der intelligenten Aktion **Erklären** mit der rechten Maustaste auf die ausgewählten Codezeilen, und wählen Sie **Copilot** und dann im Kontextmenü **Erklären** aus.

    ```csharp

    IEnumerable<Task<int>> downloadTasksQuery =
        from url in _urlList
        select ProcessUrlAsync(url, _client);
    Task<int>[] downloadTasks = downloadTasksQuery.ToArray();

    ```

1. Nehmen Sie sich kurz Zeit, um die Antwort in der Chatansicht zu überprüfen.

1. Beachten Sie die Detailstufe der Erklärung.

    GitHub Copilot Chat generiert detaillierte Erklärungen, die Informationen zu den ausgewählten Codezeilen, ihrem Zweck und ihrer Funktionsweise enthalten. Antworten umfassen Codeausschnitte und Beschreibungen in natürlicher Sprache, die Ihnen helfen, den Code zu verstehen.

### Erklärungen von Fehlern

Das Verwalten von Fehlern ist ein wesentlicher Aspekt der Softwareentwicklung. Einige Fehler sind leicht zu erkennen und zu beheben, während sich dies bei anderen schwieriger gestaltet. Wenn in Ihrem Code ein Fehler auftritt, der schwer zu verstehen ist, können Sie GitHub Copilot Chat auffordern, eine Erklärung bereitzustellen. Sie können GitHub Copilot Chat beispielsweise auffordern, zu erläutern, warum eine bestimmte Codezeile einen Fehler verursacht.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Stellen Sie sicher, dass Sie im Editor `MainWindow.xaml.cs` geöffnet haben.

1. Suchen Sie in der `SumPageSizesAsync()`-Methode die folgende Codezeile:

    ```csharp
    int[] lengths = Task.WhenAll(downloadTasks);
    ```

1. Zeigen Sie mit dem Mauszeiger auf `downloadTasks`, um die Fehlermeldung anzuzeigen.

    Fehlermeldungen enthalten nicht immer eine Erklärung dazu, wie Codierungsprobleme behoben werden können. Wenn die Lösung nicht offensichtlich ist, können Sie in GitHub Copilot Chat eine Frage stellen, um sich den Fehler erklären und Möglichkeiten zur Behebung vorschlagen zu lassen.

1. Wählen Sie die Codezeile mit dem Fehler aus, und drücken Sie dann **STRG+I**, um einen Inlinechat zu öffnen.

1. Geben Sie den folgenden Prompt ein, um eine Erklärung für den Fehler zu generieren:

    ```plaintext
    /explain why is the selection causing an error
    ```

1. Nehmen Sie sich kurz Zeit, um die Antwort in der Chatansicht zu überprüfen.

    Beachten Sie, dass die Antwort Informationen zum Fehler und Vorschläge zum Beheben enthält. In diesem Fall erklärt GitHub Copilot Chat, dass die Zeile `Task.WhenAll(downloadTasks)` einen Fehler verursacht, da das Schlüsselwort `await` fehlt. Die Antwort enthält auch einen Codeschnipsel, der zeigt, wie der Fehler behoben wird, indem das Schlüsselwort `await` vor Zeile `Task.WhenAll(downloadTasks)` hinzugefügt wird.

1. Verwenden Sie die von GitHub Copilot Chat bereitgestellte Erklärung, um den Fehler in Ihrem Code zu beheben.

    Fügen Sie wie im folgenden Codeausschnitt gezeigt das Schlüsselwort `await` vor der Zeile `Task.WhenAll(downloadTasks)` hinzu:

    ```csharp
    int[] lengths = await Task.WhenAll(downloadTasks);
    ```

    Nachdem Sie diese Änderung vorgenommen haben, sollte der Fehler behoben sein.

### Erläuterungen zu neuen Features oder Funktionen

GitHub Copilot Chat kann erklären, wie sie dem Projekt neue Features oder Funktionen hinzufügen.

Betrachten Sie das APL2007M2Sample1-Projekt. Ihr Code lädt Webseiten herunter und berechnet die Gesamtgröße der heruntergeladenen Seiten. Angenommen, Sie müssen der Anwendung eine Ausnahmebehandlung hinzufügen. In diesem Abschnitt der Demo verwenden Sie GitHub Copilot Chat, um zu erläutern, wie Ausnahmen während des Downloadvorgangs verwaltet werden.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Wählen Sie die Codezeilen aus, die die Methoden `SumPageSizesAsync` und `ProcessUrlAsync` enthalten.

1. Wenn GitHub Copilot Chat in der Chatansicht erläutern soll, wie Ausnahmen behandelt werden, die während des Downloadvorgangs ausgelöst werden, geben Sie die folgende Frage ein:

    ```plaintext
    @workspace /explain #MainWindow.xaml.cs How can I handle exceptions thrown during the download process?
    ```

1. Nehmen Sie sich kurz Zeit, um die Antwort in der Chatansicht zu überprüfen.

    Copilot Chat generiert eine Antwort, die der folgenden Erklärung ähnelt:

    Die Antwort enthält eine ausführliche Erläuterung zur Behandlung von Ausnahmen, die während des Downloadvorgangs ausgelöst werden. Außerdem erhalten Sie einen Codeausschnitt, der den vorgeschlagenen Ausnahmebehandlungscode implementiert. Sie können den Codeausschnitt kopieren oder an der Position des Cursors in Ihr Codeprojekt einfügen.

    Anstatt den Codeausschnitt aus der Chatansicht zu kopieren oder einzufügen, untersucht der nächste Schritt die Verwendung des Inlinechats, um den vorgeschlagenen Ausnahmebehandlungscode zu implementieren.

1. Wenn Sie den Inlinechat nach der Implementierung der Ausnahmebehandlung fragen möchten, wählen Sie die `ProcessUrlAsync`-Methode aus, drücken Sie **STRG+I**, und geben Sie dann den folgenden Prompt ein:

    ```plaintext
    How can I handle exceptions thrown during the download process?
    ```

1. Nehmen Sie sich kurz Zeit, um die Inlineantwort zu überprüfen.

1. Um den vorgeschlagenen Fehlerbehandlungscode zu akzeptieren, wählen Sie **Annehmen** aus.

    Beachten Sie, dass der vorgeschlagene `try-catch`-Block implementiert wird.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um Erklärungen für Codezeilen, Fehler und neue Features zu generieren. GitHub Copilot Chat bietet leistungsstarke Features, die Ihnen helfen können, schnell ein neues Projekt aufzubauen. Über den Inlinechat und die Chatansicht können Sie Hilfe von GitHub Copilot Chat erhalten, ohne die Visual Studio Code-Umgebung verlassen zu müssen. Das KI-Modell von GitHub Copilot Chat generiert genaue und nützliche Antworten, die Ihnen dabei helfen, effizienter und effektiver zu werden.
