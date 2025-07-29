---
demo:
  title: 'Demo: Erstellen von Komponententests mit GitHub Copilot Chat'
  module: 'Module 4: Develop unit tests using GitHub Copilot tools'
---

# Demo: Erstellen von Komponententests mit GitHub Copilot Chat

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Visual Studio Code und das C#-Dev Kit bieten eine Vielzahl von Features, mit denen Sie Komponententests für Ihre C#-Projekte erstellen und verwalten können. Mithilfe des C#-Dev Kit können Sie Tests für Ihr Projekt aktivieren, Testframeworkpakete hinzufügen, Komponententests ausführen und verwalten sowie Komponententestfälle generieren.

GitHub Copilot kann Inlinechatvorschläge bereitstellen, um Sie beim Generieren von Komponententests für Ihren Code zu unterstützen.

In dieser Demo erstellen Sie Komponententests für ein Codeprojekt, indem Sie GitHub Copilot Chat in Visual Studio Code verwenden.

### Erstellen eines xUnit-Testprojekts für Ihre Komponententests

Komponententestprojekte werden in der Regel in einem Ordner erstellt, der von dem Projekt getrennt ist, das Sie testen. Diese Trennung trägt dazu bei, den Testcode vom Produktionscode getrennt zu halten. In dieser Demo erstellen Sie ein xUnit-Testprojekt für das Projekt „APL2007M4PrimeService“.

Führen Sie die folgenden Schritte aus, um ein neues xUnit-Testprojekt zu erstellen:

1. Öffnen Sie den Ordner **APL2007M4PrimeService** in Visual Studio Code.

1. Öffnen Sie in Visual Studio Code die Ansicht „Projektmappen-Explorer“.

    Auf die Projektmappen-Explorer-Ansicht kann über das Fenster „Seitenleiste“ von Visual Studio Code zugegriffen werden. Der Projektmappen-Explorer ähnelt der Explorer-Ansicht, ist jedoch speziell für die Arbeit mit Visual Studio Code-Projekten und nicht mit allgemeinen Dateisystemen konzipiert.

1. Klicken Sie in der Ansicht „Projektmappen-Explorer“ mit der rechten Maustaste auf den Ordner **APL2007M4PrimeService**, und wählen Sie dann **Neues Projekt** aus.

    Wenn die Option **Neues Projekt** nicht angezeigt wird, stellen Sie sicher, dass Sie in der Ansicht *Projektmappen-Explorer* arbeiten, nicht in der Ansicht *Explorer*.

1. Wenn die Liste der Projekttypen angezeigt wird, wählen Sie **xUnit-Testprojekt** aus.

1. Geben Sie für den Projektnamen **PrimeService.UnitTests** ein, und drücken Sie dann die EINGABETASTE.

    Der Projektname sollte den Namen der Klasse widerspiegeln, die Sie testen, und innerhalb der Projektmappe eindeutig sein. In diesem Fall lautet der Name der Klasse `PrimeService`, sodass das Testprojekt als `PrimeService.UnitTests` benannt wird.

1. Wählen Sie den Standardspeicherort für das Verzeichnis aus.

    Sie könnten das xUnit-Testprojekt auch im Visual Studio Code-Terminal erstellen. Öffnen Sie ein Terminal, navigieren Sie zum Ordner „Numbers“, und führen Sie den folgenden Befehl aus:

    ```plaintext
    dotnet new xunit -n PrimeService.UnitTests
    ```

1. Wählen Sie **Projekt erstellen** aus, und erweitern Sie dann den Ordner „PrimeService.UnitTests“.

1. Löschen Sie die Datei „UnitTest1.cs“, die mit dem Projekt „PrimeService.UnitTests“ erstellt wurde.

    Bevor Sie einen neuen Komponententest erstellen, müssen Sie dem Komponententestprojekt einen Verweis hinzufügen, der auf das Klassenprojekt zeigt, das Sie testen möchten.

1. Um Ihrem Codeprojekt einen Verweis hinzuzufügen, klicken Sie mit der rechten Maustaste auf **PrimeService.UnitTests**, wählen Sie **Projektverweis hinzufügen** aus, und wählen Sie dann **Zahlen** aus.

1. Um eine Klasse für Ihre Komponententests zu erstellen, klicken Sie mit der rechten Maustaste auf **PrimeService.UnitTests**, wählen Sie **Neue Datei** aus, wählen Sie **Klasse** aus, geben Sie **PrimeServiceTests** ein, und drücken Sie dann die EINGABETASTE.

    Visual Studio Code sollte die Datei „PrimeServiceTests.cs“ für Sie öffnen.

1. Nehmen Sie sich eine Minute Zeit, um die Datei „PrimeServiceTests.cs“ zu untersuchen.

    Ihre Datei sollte in etwa wie der folgende Codeschnipsel aussehen:

    ```csharp

    namespace PrimeService.UnitTests;
    public class PrimeServiceTests
    {
    }

    ```

1. Um Probleme mit den Namespaces beim Erstellen des Projekts zu vermeiden, aktualisieren Sie die Datei „PrimeServiceTests.cs“ wie folgt:

    ```csharp

    namespace System.Numbers.UnitTests;
    public class PrimeServiceTests
    {
    }

    ```

    Ein Namespace in C# wird verwendet, um verwandte Klassen und Typen zu organisieren. Es ist eine Möglichkeit, Namenskonflikte zu vermeiden und die Organisation des Codes leichter zu verstehen. Das `.UnitTests`-Suffix im Namespace des Testprojekts ist eine allgemeine Konvention, um anzugeben, dass der Code in diesem Namespace den Code im System.Numbers-Namespace testet. Dies macht beim Betrachten der Projektstruktur deutlich, welcher Code Produktionscode ist und welcher Code Testcode ist.

1. Nehmen Sie sich eine Minute Zeit, um die Datei „PrimeService.UnitTests.csproj“ zu untersuchen.

    Die Datei „PrimeService.UnitTests.csproj“ sollte eine `<ItemGroup>` mit den folgenden `<PackageReference />`-Elementen enthalten:

    ```xml

    <PackageReference Include="coverlet.collector" Version="6.0.0" />
    <PackageReference Include="Microsoft.NET.Test.Sdk" Version="17.8.0" />
    <PackageReference Include="xunit" Version="2.5.3" />
    <PackageReference Include="xunit.runner.visualstudio" Version="2.5.3" />

    ```

    Diese Paketverweise sind erforderlich, um xUnit als Testbibliothek zu verwenden und Test Runner zu konfigurieren. Außerdem sollten die folgenden `<ItemGroup>`-Elemente in der Datei „PrimeService.UnitTests.csproj“ sehen:

    ```xml

    <ItemGroup>
        <Using Include="Xunit" />
    </ItemGroup>
    <ItemGroup>
        <ProjectReference Include="..\Numbers\Numbers.csproj" />
    </ItemGroup>

    ```

    Diese Elemente sind erforderlich, um auf das Projekt „Numbers“ zu verweisen und das xUnit-Testframework zu verwenden.

1. Um die Lösung zu erstellen, drücken Sie **STRG+UMSCHALT+B** und wählen Sie dann **dotnet: build** aus.

    Sie können die Lösung auch mit einem .NET CLI-Befehl (Dotnet Build) erstellen oder mit der rechten Maustaste auf den Lösungsknoten in der Projektmappen-Explorer-Ansicht klicken und **Erstellen** auswählen.

    > [!NOTE]
    > Wenn **Buildfehler** angezeigt werden, beheben Sie die Fehler, bevor Sie die Demo fortsetzen. Sie müssen über einen erfolgreichen Build verfügen, bevor Sie fortfahren.

Nun können Sie einen Komponententest mit GitHub Copilot Chat erstellen.

### Erstellen von Komponententests mithilfe der Chatansicht

GitHub Copilot und GitHub Copilot Chat können basierend auf dem Kontext Ihrer Codebasis Vorschläge bereitstellen, um Sie beim Generieren von Komponententests für Ihren Code zu unterstützen. Sie können GitHub Copilot Chat verwenden, um Komponententests für bestimmte Methoden oder Klassen in Ihrem Code zu generieren.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie in der Ansicht „Projektmappen-Explorer“ in „Numbers“ die Datei „PrimeService.cs“.

1. Wählen Sie die **IsPrime**-Methode aus.

1. Öffnen Sie die Chatansicht.

1. Wählen Sie die Schaltfläche **Kontext anfügen** aus.

    Die Schaltfläche **Kontext anfügen** (Büroklammersymbol) wird verwendet, um GitHub Copilot über den relevanten Kontext in Ihrer Codebasis zu informieren. Der zusätzliche Kontext hilft GitHub Copilot Chat, korrektere Vorschläge bereitzustellen. In diesem Fall soll GitHub Copilot Ihre PrimeServiceTests.cs Datei verwenden, um die Komponententests vorzuschlagen.

1. Wählen Sie in der Dropdownliste **Anlagen durchsuchen** im Abschnitt **zuletzt geöffnet** **PrimeServiceTests.cs** aus.

    Das Dropdownmenü **Anlagen suchen** enthält einige Standardoptionen, aus denen Sie auswählen können. Außerdem enthält es eine Liste der zuletzt geöffneten Dateien. Die PrimeServiceTests.cs Datei sollte im Abschnitt „zuletzt geöffnet“ aufgeführt sein.

    Zu den Optionen zum Suchen von Anlagen gehören

1. Wählen Sie die Schaltfläche **Kontext anfügen** erneut aus.

1. Geben Sie im Textfeld „Anlagen suchen“ **PrimeService.Unit** ein und wählen Sie dann **PrimeService.UnitTests.csproj** aus.

    > [!NOTE]
    > Veranschaulichen Sie, wie Sie eine Datei aus der Explorer-Ansicht ziehen und in der Chatansicht ablegen. In vielen Fällen ist dies eine schnellere Möglichkeit zum Anfügen von Kontext.

1. Beachten Sie, dass die Chatansicht mit dem zusätzlichen Kontext aktualisiert wird.

1. Wählen Sie in der Chatansicht **/tests Komponententests für meinen Code hinzufügen**.

    Die Option **/tests Komponententests für meine Codeoption** wird verwendet, um Komponententests für den im Editor ausgewählten Code zu generieren. In diesem Fall haben Sie die **IsPrime**-Methode in der Datei PrimeService.cs ausgewählt.

1. Nehmen Sie sich eine Minute Zeit, um die Vorschläge von GitHub Copilot zu überprüfen.

    Der Vorschlag von GitHub Copilot enthält zwei Abschnitte, einen „Plan“ und ein Codebeispiel mit Komponententests.

    Der Plan schlägt vor, eine neue PrimeServiceTest.cs-Datei für die Komponententests zu erstellen. Außerdem wird empfohlen, die Datei im Projektordner „Zahlen“ zu erstellen.

1. Wählen Sie in der Chatansicht **Bearbeitungen übernehmen** aus.

1. Beachten Sie, dass die Schaltfläche „Bearbeitungen anwenden“ den Komponententestcode auf einer neuen Registerkarte im Editor platziert.

    Sie können diesen Code verwenden, um die PrimeServiceTests.cs-Datei in Ihrem PrimeService.UnitTests-Projekt zu aktualisieren.

1. Wählen Sie im Menü **Datei** **Speichern unter** aus und navigieren Sie dann zum Ordner „PrimeService.UnitTests“.

1. Wählen Sie **PrimeServiceTests.cs** und dann **Speichern** aus.

1. Wenn Sie aufgefordert werden, die vorhandene Datei zu überschreiben, wählen Sie **Ja** aus.

1. Nehmen Sie sich eine Minute Zeit, um die aktualisierte Datei „PrimeServiceTests.cs“ zu überprüfen.

    Der von GitHub Copilot Chat vorgeschlagene Code sollte Tests für bestimmte Prime- und Non-Prime-Nummern enthalten. Der vorgeschlagene Code kann parametrisierte Tests (mit `[Theory]`- and `[InlineData]`-Attributen) enthalten, um mehrere Datasets präziser zu testen.

    Der bereitgestellte Codeschnipsel sollte in etwa wie der folgende Codeschnipsel aussehen:

    ```csharp

    using Xunit;
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
            public void IsPrime_InputIs1_ReturnsFalse()
            {
                var result = _primeService.IsPrime(1);
                Assert.False(result, "1 should not be prime");
            }
            [Fact]
            public void IsPrime_InputIs2_ReturnsTrue()
            {
                var result = _primeService.IsPrime(2);
                Assert.True(result, "2 should be prime");
            }
            [Fact]
            public void IsPrime_InputIs3_ReturnsTrue()
            {
                var result = _primeService.IsPrime(3);
                Assert.True(result, "3 should be prime");
            }
            [Fact]
            public void IsPrime_InputIs4_ReturnsFalse()
            {
                var result = _primeService.IsPrime(4);
                Assert.False(result, "4 should not be prime");
            }
            [Theory]
            [InlineData(5, true)]
            [InlineData(6, false)]
            [InlineData(7, true)]
            [InlineData(8, false)]
            [InlineData(9, false)]
            [InlineData(10, false)]
            public void IsPrime_Values_ReturnExpectedResult(int value, bool expected)
            {
                var result = _primeService.IsPrime(value);
                Assert.Equal(expected, result);
            }
        }
    }

    ```

    Beachten Sie, dass für die Komponententests eine Instanz der PrimeService-Klasse erforderlich ist.

    ```csharp

    private readonly PrimeService _primeService;
    public PrimeServiceTests()
    {
        _primeService = new PrimeService();
    }

    ```

1. Erstellen Sie die Lösung neu.

    Sie sollten neben jedem Komponententest grüne „Testpfeile“ sehen, wenn der Build erfolgreich ist.

    Sie erstellen weitere Komponententests im nächsten Abschnitt, sodass zurzeit keine Tests ausgeführt werden müssen.

    Es gibt jedoch mehrere Methoden, die Tests auszuführen. Zum Beispiel:

    - Sie können die Tests im Visual Studio Code-Terminal mithilfe des `dotnet test`-Befehls ausführen.
    - Sie können die Tests in der Test-Explorer-Ansicht in Visual Studio Code ausführen.
    - Sie können die Tests über die Visual Studio Code-Befehlspalette mit dem Befehl **Test: Alle Tests ausführen** ausführen.
    - Sie können die Tests im Visual Studio Code-Editor ausführen, indem Sie im Kontextmenü die Option **Tests in aktueller Datei ausführen** auswählen.

    Die Tests, die Sie in diesem Abschnitt der Demo erstellt haben, sollten erfolgreich ausgeführt werden. Die grünen „Testpfeile“ neben dem Komponententest werden grüne Kreise mit einem Häkchen.

### Erstellen von Komponententests mithilfe des Inlinechats

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie in der Ansicht „Projektmappen-Explorer“ die Datei „PrimeService.cs“.

    Die Datei „PrimeService.cs“ befindet sich im Ordner „Numbers“.

1. Wählen Sie die IsPrime-Methode aus.

1. Öffnen Sie eine Inlinechatsitzung, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```plaintext
    Create unit tests for the IsPrime method using the xUnit framework.
    ```

1. Nehmen Sie sich eine Minute Zeit, um die vom Inlinechat bereitgestellten Vorschläge zu überprüfen.

    ```csharp

    using Xunit;
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
            public void IsPrime_InputIs1_ReturnsFalse()
            {
                var result = _primeService.IsPrime(1);
                Assert.False(result, "1 should not be prime");
            }
            [Fact]
            public void IsPrime_InputIs2_ReturnsTrue()
            {
                var result = _primeService.IsPrime(2);
                Assert.True(result, "2 should be prime");
            }
            [Fact]
            public void IsPrime_InputIs3_ReturnsTrue()
            {
                var result = _primeService.IsPrime(3);
                Assert.True(result, "3 should be prime");
            }
            [Fact]
            public void IsPrime_InputIs4_ReturnsFalse()
            {
                var result = _primeService.IsPrime(4);
                Assert.False(result, "4 should not be prime");
            }
            [Theory]
            [InlineData(5, true)]
            [InlineData(6, false)]
            [InlineData(7, true)]
            [InlineData(8, false)]
            [InlineData(9, false)]
            [InlineData(10, false)]
            public void IsPrime_Values_ReturnExpectedResult(int value, bool expected)
            {
                var result = _primeService.IsPrime(value);
                Assert.Equal(expected, result);
            }
        }
    }

    ```

1. Beachten Sie, dass die Chatansicht und der Inlinechat eine ähnliche Testabdeckung erzeugen.

1. Um den Inlinechatvorschlag zu verwerfen, wählen Sie **Verwerfen** aus, und schließen Sie dann die Dateiregisterkarte, die vom Inlinechat erstellt wurde.

    Beachten Sie, dass die von GitHub Copilot während dieser Demo vorgeschlagenen Komponententests unvollständig sein können. In der nächsten Demo werden zusätzliche Grenzfälle untersucht, die Sie möglicherweise testen sollten.

### Zusammenfassung

In dieser Demo haben Sie mithilfe von GitHub Copilot Chat in Visual Studio Code Komponententests für ein Codeprojekt erstellt. Sie haben ein xUnit-Testprojekt erstellt, dem Projekt, das Sie testen wollten, einen Verweis hinzugefügt und Komponententests für die `IsPrime`-Methode in der `PrimeService`-Klasse generiert. Sie haben GitHub Copilot Chat verwendet, um Komponententests in der Chatansicht und im Inlinechat zu generieren.
