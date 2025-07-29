---
demo:
  title: "Demo: Erstellen von Komponententests für bestimmte Bedingungen mithilfe von GitHub\_Copilot"
  module: 'Module 4: Develop unit tests using GitHub Copilot tools'
---

# Demo: Erstellen von Komponententests für bestimmte Bedingungen mithilfe von GitHub Copilot

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Die GitHub Copilot-Erweiterungen können Ihnen helfen, Komponententests für bestimmte Bedingungen in Ihrem Code zu erstellen. Sie können beispielsweise GitHub Copilot Chat verwenden, um das Verhalten einer Methode zu testen, wenn sie bestimmte Eingaben empfängt.

In dieser Demo verwenden Sie die GitHub Copilot-Erweiterungen, um Komponententests für bestimmte Bedingungen zu erstellen.

### Erstellen von Komponententests mit GitHub Copilot

Sie können Komponententests mithilfe von Vorschlägen zur automatischen Vervollständigung durch GitHub Copilot erstellen. Das Verwenden von Vorschlägen zur automatischen Vervollständigung kann Ihnen helfen, Komponententests für Ihren Code schnell zu generieren.

In diesem Abschnitt der Demo verwenden Sie GitHub Copilot, um Komponententests für die `IsPrime`-Methode der `PrimeService`-Klasse zu erstellen.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie den Projektordner **APL2007M4PrimeService-UnitTests** in Visual Studio Code.

1. Öffnen Sie die Datei „PrimeServiceTests2.cs“ im Editor.

1. Löschen Sie den gesamten Code in der `PrimeServiceTests`-Klasse.

    Der Inhalt der Datei „PrimeServiceTests.cs“ sollte dem folgenden Codeschnipsel ähneln:

    ```csharp

    namespace System.Numbers.UnitTests;
    public class PrimeServiceTests
    {
    }

    ```

1. Speichern Sie die Datei „PrimeServiceTests.cs“, und erstellen Sie dann die Projektmappe neu.

1. Damit GitHub Copilot eine Inlinevervollständigung generiert, erstellen Sie eine leere Zeile innerhalb der Klasse `PrimeServiceTests`.

    Wenn Sie eine oder zwei Sekunden warten, schlägt GitHub Copilot eine Vervollständigung für die Klasse `PrimeServiceTests` vor.

1. Wählen Sie **Annehmen** aus, und nehmen Sie sich dann eine Minute Zeit, um die von GitHub Copilot generierten Komponententests zu überprüfen.

1. Nehmen Sie sich eine Minute Zeit, um die Sammlung der Komponententests zu überprüfen, die GitHub Copilot für die Methode `IsPrime` generiert hat.

    Im nächsten Abschnitt der Demo wird gezeigt, wie Sie GitHub Copilot Chat verwenden, um GitHub Copilot aufzufordern, zusätzliche Grenzfälle vorzuschlagen, die getestet werden sollten.

    ```csharp

    namespace System.Numbers.UnitTests
    {
        public class PrimeServiceTests
        {
            private readonly PrimeService _primeService;
            public PrimeServiceTests()
            {
                _primeService = new PrimeService();
            }
            [Fact]
            public void IsPrime_ReturnsFalse_ForNegativeNumbers()
            {
                // Arrange
                int candidate = -5;
                // Act
                bool result = _primeService.IsPrime(candidate);
                // Assert
                Assert.False(result);
            }
            [Fact]
            public void IsPrime_ReturnsFalse_ForZero()
            {
                // Arrange
                int candidate = 0;
                // Act
                bool result = _primeService.IsPrime(candidate);
                // Assert
                Assert.False(result);
            }
            [Fact]
            public void IsPrime_ReturnsFalse_ForOne()
            {
                // Arrange
                int candidate = 1;
                // Act
                bool result = _primeService.IsPrime(candidate);
                // Assert
                Assert.False(result);
            }
            [Fact]
            public void IsPrime_ReturnsTrue_ForPrimeNumbers()
            {
                // Arrange
                int candidate = 7;
                // Act
                bool result = _primeService.IsPrime(candidate);
                // Assert
                Assert.True(result);
            }
        }
    }

    ```

### Erstellen von Komponententests für bestimmte Bedingungen mithilfe von GitHub Copilot und GitHub Copilot Chat.

1. Wählen Sie den Inhalt der `PrimeServiceTests`-Klasse aus.

1. Öffnen Sie die Chatansicht.

1. Wenn Sie die Datei „PrimeService.cs“ zum Kontext der Chatansicht hinzufügen möchten, ziehen Sie die Datei „PrimeService.cs“ aus der Explorer-Ansicht in die Chatansicht.

1. Geben Sie in der Chatansicht den folgenden Prompt ein:

    ```plaintext
    @workspace #selection are there any edge cases that should also be tested 
    ```

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Vorschläge zu überprüfen.

    ```plaintext
    Yes, there are a few edge cases that should also be tested:
    
    1. Large Prime Numbers: Ensure the function can handle large prime numbers.

    2. Large Non-Prime Numbers: Ensure the function can handle large non-prime numbers.

    3. Even Numbers Greater Than 2: Ensure the function returns false for even numbers greater than 2.

    4. Small Prime Numbers: Ensure the function correctly identifies small prime numbers like 2 and 3.

    Here are the additional test cases:
    ```

    ```csharp

    [Fact]
    public void IsPrime_ReturnsTrue_ForTwo()
    {
        // Arrange
        int candidate = 2;
        // Act
        bool result = _primeService.IsPrime(candidate);
        // Assert
        Assert.True(result);
    }
    [Fact]
    public void IsPrime_ReturnsTrue_ForThree()
    {
        // Arrange
        int candidate = 3;
        // Act
        bool result = _primeService.IsPrime(candidate);
        // Assert
        Assert.True(result);
    }
    [Fact]
    public void IsPrime_ReturnsFalse_ForEvenNumbersGreaterThanTwo()
    {
        // Arrange
        int candidate = 4;
        // Act
        bool result = _primeService.IsPrime(candidate);
        // Assert
        Assert.False(result);
    }
    [Fact]
    public void IsPrime_ReturnsTrue_ForLargePrimeNumber()
    {
        // Arrange
        int candidate = 7919;
        // Act
        bool result = _primeService.IsPrime(candidate);
        // Assert
        Assert.True(result);
    }
    [Fact]
    public void IsPrime_ReturnsFalse_ForLargeNonPrimeNumber()
    {
        // Arrange
        int candidate = 8000;
        // Act
        bool result = _primeService.IsPrime(candidate);
        // Assert
        Assert.False(result);
    }

    ```

1. Erstellen Sie eine leere Zeile nach der letzten Testmethode in der Klasse `PrimeServiceTests`.

1. Zeigen Sie in der Chatansicht mit der Maus auf den Codeausschnitt, und wählen Sie dann **Beim Cursor einfügen** aus.

1. Speichern Sie die Datei „PrimeServiceTests.cs“, und erstellen Sie dann die Projektmappe neu.

1. Nehmen Sie sich eine Minute Zeit, um die Sammlung der Komponententests zu überprüfen, die GitHub Copilot für die Methode `IsPrime` generiert hat.

    Wie immer ist es wichtig, die von GitHub Copilot abgeschlossenen Arbeiten zu überprüfen, um sicherzustellen, dass die Tests gültig sind und dass sie die Randfälle abdecken, die Sie testen möchten. Sobald Sie mit den Tests zufrieden sind, können Sie sie ausführen, um zu überprüfen, ob sie erfolgreich waren.

1. Zeigen Sie mit dem Mauszeiger auf einen der grünen „Testpfeile“.

    Beachten Sie die QuickInfo, die Sie darauf hinweist, dass Sie entweder klicken können, um den Test auszuführen, oder mit der rechten Maustaste klicken können, um weitere Optionen anzuzeigen.

1. Klicken Sie mit der rechten Maustaste auf einen der grünen „Testpfeile“.

1. Wählen Sie **Im Test-Explorer anzeigen** aus.

    Die Test-Explorer-Ansicht wird geöffnet. Die Test-Explorer-Ansicht kann zum Ausführen und Debuggen von Tests und zum Anzeigen der Ergebnisse von Testläufen verwendet werden. Um die Test-Explorer-Ansicht manuell zu öffnen, wählen Sie **Testen** in der Aktivitätsleiste auf der linken Seite des Visual Studio Code-Fensters aus. Das Symbol für die Ansicht **Testen** ist das Symbol, das wie ein Glaskolben aus einem Labor aussieht.

1. Wählen Sie oben in der Test-Explorer-Ansicht **Tests ausführen** aus.

    Nach ein paar Sekunden zeigt der Test-Explorer die Ergebnisse des Testlaufs an. Sie sollten sehen, dass alle Tests erfolgreich waren. Grüne Häkchen im Test-Explorer und links neben den Komponententests im Editor geben an, dass der Test erfolgreich war.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot und GitHub Copilot Chat verwendet, um Komponententests für bestimmte Bedingungen in der Klasse `PrimeService` zu erstellen. Sie haben Codezeilenvervollständigung verwendet, um Assertionen zu generieren, um sicherzustellen, dass Funktionseingabeparameter gültig sind, und Sie haben die Chatansicht verwendet, um GitHub Copilot aufzufordern, zusätzliche Randfälle vorzuschlagen, die getestet werden sollten. Sie haben die von GitHub Copilot bereitgestellten Vorschläge überprüft und die Tests ausgeführt, um zu überprüfen, ob sie erfolgreich sind. Außerdem haben Sie erfahren, wie Sie den Test-Explorer in Visual Studio Code verwenden, um Testläufen auszuführen und die Ergebnisse anzuzeigen.
