---
demo:
  title: 'Demo: Generieren einer Inlinecodedokumentation mithilfe von GitHub Copilot Chat'
  module: 'Module 2: Generate documentation using GitHub Copilot tools'
---

# Demo: Generieren einer Inlinecodedokumentation mithilfe von GitHub Copilot Chat

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Das Dokumentieren Ihres Codes ist ein wichtiger Teil der Softwareentwicklung. Eine Inlinedokumentation (Codekommentare) unterstützt Entwickler dabei, die Codebasis, ihren Zweck und ihre Verwendung besser zu verstehen.

GitHub Copilot Chat kann Ihnen dabei helfen, Ihren Code schnell und präzise zu dokumentieren. Für die Generierung einer Inlinedokumentation mit GitHub Copilot Chat stehen mehrere Optionen zur Verfügung:

- Erstellen Sie einen eigenen Prompt in natürlicher Sprache, der zum Generieren einer spezifischen Dokumentation verwendet werden kann.
- Verwenden Sie den Befehl `/doc` während einer Inlinechatsitzung, um Kommentare für ausgewählten Code zu generieren.
- Verwenden Sie die intelligente Aktion **Dokumentation generieren**, um Kommentare für ausgewählten Code zu generieren.

Durch eine ordnungsgemäße Dokumentation des Codes wird eine besser les- und verwaltbare Codebasis erstellt, die andere Entwickler leichter verstehen und mit der sie einfacher arbeiten können.

### Generieren der Inlinecodedokumentation mithilfe der Chatansicht

In dieser Demo verwenden Sie GitHub Copilot Chat, um eine Inlinecodedokumentation für das `APL2007M2Sample1`-Projekt zu erstellen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Stellen Sie sicher, dass das `APL2007M2Sample1`-Projekt in Visual Studio Code geöffnet ist.

1. Öffnen Sie die Datei `MainWindow.xaml.cs` .

1. Wählen Sie den gesamten Code ab der Namespacedeklaration bis zum Ende der Datei aus.

1. Öffnen Sie die Chatansicht.

1. Um zu sehen, wie GitHub Copilot Chat den ausgewählten Code dokumentiert hat, geben Sie die folgende Eingabeaufforderung ein:

    ```output
    @workspace #selection generate inline code documentation for the selected code
    ```

1. Nehmen Sie sich eine Minute Zeit, um die vorgeschlagene Codedokumentation zu überprüfen.

    Die generierte Antwort sollte etwa wie folgendes Codebeispiel aussehen:

    ```csharp

    namespace ParallelAsyncExample
    {
        public partial class MainWindow : Window
        {
            // HttpClient instance with a maximum response content buffer size of 1,000,000 bytes
            private readonly HttpClient _client = new HttpClient { MaxResponseContentBufferSize = 1_000_000 };
            // List of URLs to download content from
            private readonly IEnumerable<string> _urlList = new string[]
            {
                "https://docs.microsoft.com",
                "https://docs.microsoft.com/azure",
                "https://docs.microsoft.com/powershell",
                "https://docs.microsoft.com/dotnet",
                "https://docs.microsoft.com/aspnet/core",
                "https://docs.microsoft.com/windows",
                "https://docs.microsoft.com/office",
                "https://docs.microsoft.com/enterprise-mobility-security",
                "https://docs.microsoft.com/visualstudio",
                "https://docs.microsoft.com/microsoft-365",
                "https://docs.microsoft.com/sql",
                "https://docs.microsoft.com/dynamics365",
                "https://docs.microsoft.com/surface",
                "https://docs.microsoft.com/xamarin",
                "https://docs.microsoft.com/azure/devops",
                "https://docs.microsoft.com/system-center",
                "https://docs.microsoft.com/graph",
                "https://docs.microsoft.com/education",
                "https://docs.microsoft.com/gaming"
            };
            // Event handler for the start button click event
            private void OnStartButtonClick(object sender, RoutedEventArgs e)
            {
                // Disable the start button and clear the results text box
                _startButton.IsEnabled = false;
                _resultsTextBox.Clear();
                // Start the asynchronous operation to sum page sizes
                Task.Run(() => StartSumPageSizesAsync());
            }
            // Starts the asynchronous operation to sum page sizes
            private async Task StartSumPageSizesAsync()
            {
                // Perform the main download operation
                await SumPageSizesAsync();
                // Update the UI to re-enable the start button and indicate that control has returned
                await Dispatcher.BeginInvoke(() =>
                {
                    _resultsTextBox.Text += $"\nControl returned to {nameof(OnStartButtonClick)}.";
                    _startButton.IsEnabled = true;
                });
            }
            // Asynchronously sums the sizes of the pages from the URLs
            private async Task SumPageSizesAsync()
            {
                // Start a stopwatch to measure elapsed time
                var stopwatch = Stopwatch.StartNew();
                // Create tasks to download content from each URL
                IEnumerable<Task<int>> downloadTasksQuery =
                    from url in _urlList
                    select ProcessUrlAsync(url, _client);
                // Convert the sequence of tasks into an array
                Task<int>[] downloadTasks = downloadTasksQuery.ToArray();
                // Wait for all tasks to complete and sum the lengths of the downloaded content
                int[] lengths = await Task.WhenAll(downloadTasks);
                int total = lengths.Sum();
                // Update the UI with the total bytes and elapsed time
                await Dispatcher.BeginInvoke(() =>
                {
                    stopwatch.Stop();
                    _resultsTextBox.Text += $"\nTotal bytes returned:  {total:#,#}";
                    _resultsTextBox.Text += $"\nElapsed time:          {stopwatch.Elapsed}\n";
                });
            }
            // Asynchronously processes a URL by downloading its content and returning the length of the content
            private async Task<int> ProcessUrlAsync(string url, HttpClient client)
            {
                try
                {
                    // Download the content of the URL
                    byte[] byteArray = await client.GetByteArrayAsync(url);
                    // Update the UI with the URL and content length
                    await DisplayResultsAsync(url, byteArray);
                    // Return the length of the downloaded content
                    return byteArray.Length;
                }
                catch (HttpRequestException e)
                {
                    // Handle HTTP request exceptions by updating the UI with an error message
                    await Dispatcher.BeginInvoke(() =>
                    {
                        _resultsTextBox.Text += $"{url,-60} {"Error",-10}\n";
                        _resultsTextBox.Text += $"Exception: {e.Message}\n";
                    });
                    // Return 0 to indicate failure
                    return 0;
                }
            }
            // Updates the UI with the URL and the length of the downloaded content
            private Task DisplayResultsAsync(string url, byte[] content) =>
                Dispatcher.BeginInvoke(() =>
                    _resultsTextBox.Text += $"{url,-60} {content.Length,10:#,#}\n")
                          .Task;
            // Disposes of the HttpClient instance when the window is closed to free up resources
            protected override void OnClosed(EventArgs e) => _client.Dispose();
        }
    }

    ```

    Die Antwort enthält vorgeschlagene Codekommentare und *einen Teil* des zugeordneten Codes. Teile Ihres Codes wird möglicherweise aus Platzgründen weggelassen. Sie könnten Codekommentare manuell in die eigentliche Codedatei verschieben.

    Inlinechat bietet einen direkteren Ansatz für das Hinzufügen von Kommentaren zu Ihrem Code.

### Generieren der Inlinecodedokumentation mithilfe von Inlinechat

1. Scrollen Sie zum Anfang der `MainWindow.xaml.cs`-Datei.

1. Wählen Sie die `OnStartButtonClick`-Methode aus.

1. Um einen Inlinechat zu öffnen, drücken Sie **STRG+I**.

1. Um die Inlinedokumentation für die `OnStartButtonClick`-Methode zu generieren, geben Sie die folgende Eingabeaufforderung ein:

    ```output
    /doc
    ```

1. Nehmen Sie sich eine Minute Zeit, um die generierte Codedokumentation zu überprüfen.

    Beachten Sie, dass die vorgeschlagene Dokumentation für die `OnStartButtonClick`-Methode eine Zusammenfassung und Beschreibungen der beiden Parameter enthält. Wenn eine Methode einen Rückgabewert enthält, ist auch eine Beschreibung des Rückgabewerts eingeschlossen.

    > [!IMPORTANT]
    > Überprüfen Sie vor der Annahme immer die vorgeschlagenen Updates von GitHub Copilot. Wenn Sie ein Problem in einer vorgeschlagenen Codeaktualisierung feststellen, können Sie entweder das Update verwerfen oder versuchen, das Problem zu beheben, bevor Sie das vorgeschlagene Codeupdate akzeptieren.

1. Um das vorgeschlagene Update zu verwerfen, wählen Sie **Verwerfen** aus.

    Im nächsten Abschnitt generieren Sie Dokumentationen für alle Methoden gleichzeitig.

### Generieren der Inlinecodedokumentation mithilfe der intelligenten Aktion **Dokumentation generieren**

Die intelligente Aktion **Dokumentation generieren** ist eine weitere Möglichkeit, Inline-Codedokumentation zu generieren. Sie können die intelligente Aktion verwenden, um Kommentare zu generieren, die den ausgewählten Code beschreiben.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Wählen Sie im Visual Studio Code-Editor alle Methoden *innerhalb* der `MainWindow`-Klasse aus.

1. Klicken Sie mit der rechten Maustaste auf den ausgewählten Code, wählen Sie **Copilot** aus, und wählen Sie dann **Dokumentation generieren** aus.

    Warten Sie, bis die Dokumentation generiert wird.

1. Überprüfen Sie die vorgeschlagenen Änderungen.

    > [!IMPORTANT]
    > Wenn Sie Probleme in der generierten Dokumentation finden, ändern Sie die vorgeschlagenen Änderungen, bevor Sie fortfahren.

1. Wählen Sie **Akzeptieren** aus.

    Jede der Methoden in der `MainWindow`-Klasse enthält jetzt generierte Kommentare.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um eine Inlinecodedokumentation für die App `APL2007M2Sample1` zu erstellen. Sie haben erfahren, wie Sie die Inlinecodedokumentation mithilfe der Chatansicht, Inlinechats und der intelligenten Aktion **Dokumentation generieren** generieren. Durch das Generieren von Codekommentaren können Sie eine besser lesbare und verwendbare Codebasis erstellen, die für andere Entwickler einfacher zu verstehen und zu verwenden ist. Inlinecodedokumentation ist ein wesentlicher Teil der Softwareentwicklung, die Entwickler dabei unterstützt, die Codebasis, ihren Zweck und ihre Verwendung zu verstehen.
