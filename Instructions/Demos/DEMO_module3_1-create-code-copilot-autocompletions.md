---
demo:
  title: 'Demo: Erstellen von Code mithilfe von Codezeilenvervollständigungen'
  module: 'Module 3: Develop code features using GitHub Copilot tools'
---

# Demo: Erstellen von Code mithilfe von Codezeilenvervollständigungen

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

GitHub Copilot kann Codevervollständigungsvorschläge für zahlreiche Programmiersprachen und eine Vielzahl von Frameworks bereitstellen, eignet sich jedoch besonders gut für Python, JavaScript, TypeScript, Ruby, Go, C# und C++. Codezeilenvervollständigungen werden basierend auf dem Kontext des Codes generiert, den Sie schreiben. Sie können die von GitHub Copilot bereitgestellten Vorschläge annehmen, ablehnen oder teilweise annehmen.

GitHub Copilot bietet zwei Möglichkeiten zum Generieren von Codezeilenvervollständigungen:

- **Aus einem Kommentar**: Sie können Codezeilenvervollständigungen generieren, indem Sie einen Kommentar schreiben, der den Code beschreibt, den Sie generieren möchten. GitHub Copilot bietet Codevervollständigungsvorschläge basierend auf dem Kommentar, den Sie schreiben.

- **Aus dem Code**: Sie können Codezeilenvervollständigungen generieren, indem Sie eine Codezeile starten oder die EINGABETASTE nach einer abgeschlossenen Codezeile drücken. GitHub Copilot bietet Codevervollständigungsvorschläge basierend auf dem Code, den Sie schreiben.

In dieser Demo verwenden Sie GitHub Copilot, um Codezeilenvervollständigungen in Ihrer Visual Studio Code-Umgebung zu generieren.

### Erstellen einer Konsolen-App in Ihrer Visual Studio Code-Umgebung

In dieser Demo erstellen Sie eine Konsolen-App mithilfe von GitHub Copilot-Tools.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Öffnen Sie eine neue Instanz von Visual Studio Code, und öffnen Sie dann die Chatansicht.

    Sie können die Chatansicht öffnen, indem Sie im Visual Studio Code Command Center **Chat öffnen** auswählen oder die Tastenkombination **STRG+ALT+I** verwenden.

1. Geben Sie in der Chatansicht die folgende Eingabeaufforderung ein:

    ```plaintext
    @workspace /new console application named APL2007M3. Use C# LangVersion 12 and NET8.0. Only .cs and .csproj files. Enable ImplicitUsings and Nullable
    ```

1. Wählen Sie in der Chatansicht **Arbeitsbereich erstellen** aus.

    GitHub Copilot verwendet Ihren Prompt, um den Arbeitsbereich für eine neue Konsolenanwendung zu erstellen. Die Anwendung verwendet `C#` und `.NET8.0`. Das Codeprojekt heißt `APL2007M3` und enthält die Dateien `.cs` und `.csproj`. Die Datei `APL2007M3.csproj` gibt C# `LangVersion 12` an und ermöglicht die Verwendung von `ImplicitUsings` und `Nullable`.

1. Navigieren Sie im Dialogfeld "Ordner auswählen" zu Ihrem Desktopordner, wählen Sie **Desktop** und dann **Als übergeordneter Ordner auswählen** aus.

    Sie werden aufgefordert, einen übergeordneten Ordner für den neuen Arbeitsbereich auszuwählen. Das Auswählen des Desktopordners ist eine gute Wahl für diese Demo. Der Desktopordner ist leicht zu finden. Räumen Sie auf, wenn Sie diese Schulung abschließen.

1. Wenn Sie aufgefordert werden, das neue Projekt zu öffnen, wählen Sie **Öffnen** aus.

1. Wählen Sie in der Ansicht Explorer die Datei **Program.cs** aus.

1. Ersetzen Sie den Inhalt der Datei Program.cs durch den folgenden Code:

    ```csharp

    namespace ReportGenerator
    {
        class QuarterlyIncomeReport
        {
            static void Main(string[] args)
            {
                // create a new instance of the class
                QuarterlyIncomeReport report = new QuarterlyIncomeReport();
                // call the GenerateSalesData method
                // call the QuarterlySalesReport method
            }
            public void QuarterlySalesReport()
            {
                Console.WriteLine("Quarterly Sales Report");
            }
        }    
    }

    ```

Die Einrichtungsanforderungen sind abgeschlossen, und Sie können die Demo fortsetzen.

### Verwenden von GitHub Copilot zum Generieren von Codezeilenvervollständigungen aus einem Kommentar

GitHub Copilot generiert Codevervollständigungsvorschläge basierend auf dem Kommentar und dem vorhandenen Kontext Ihrer App. Sie können Kommentare verwenden, um Codeschipsel, Methoden, Datenstrukturen und andere Codeelemente zu beschreiben.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Erstellen Sie in der Datei **Program.cs** unterhalb der `Main`-Methode zwei leere Codezeilen.

1. Um eine Datenstruktur zu erstellen, die zum Generieren von Testdaten verwendet werden kann, erstellen Sie den folgenden Codekommentar, und drücken Sie dann die EINGABETASTE:

    ```C#
    // public struct SalesData. Include the following fields: date sold, department name, product ID, quantity sold, unit price
    ```

    GitHub Copilot generiert einen oder mehrere Codevervollständigungsvorschläge basierend auf Ihrem Codekommentar und vorhandenem Code, der in Ihrer App gefunden wird.

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Codevervollständigungsvorschläge zu überprüfen.

    > [!NOTE]
    > Wenn GitHub Copilot Vorschläge für eine Methode anstelle einer Datenstruktur generiert, geben Sie **public str** ein, und warten Sie, bis der Codeabschlussvorschlag aktualisiert wird. GitHub Copilot verwendet die zusätzlichen Informationen, um seine Vorschläge zu verbessern.

    Beachten Sie die Datentypen, die zum Deklarieren der Felder der Datenstruktur verwendet werden. GitHub Copilot wählt Datentypen und Variablennamen basierend auf Ihrem vorhandenen Code und dem Codekommentar aus. GitHub Copilot versucht zu bestimmen, wie die Anwendung Variablen verwendet, und definiert die Datentypen entsprechend.

    Wenn GitHub Copilot mehrere Vorschläge generiert, können Sie die Vorschläge durchlaufen, indem Sie die nach links oder rechts weisenden Pfeile (`>` oder `<`) links neben der Schaltfläche **Annehmen** auswählen. Auf diese Weise können Sie den Vorschlag überprüfen und auswählen, der Ihren Anforderungen am besten entspricht.

    Es ist in Ordnung, einen Codeabschlussvorschlag zu akzeptieren, der nicht genau mit dem gewünschten Ergebnis übereinstimmt. Die Änderungen, die zum „Beheben“ des Vorschlags erforderlich sind, sollten jedoch klar sein. In diesem Fall sind einige der Datentypen nicht die gewünschten, aber Sie können diese anpassen, nachdem Sie die vorgeschlagene automatische Vervollständigung akzeptiert haben.

    Wenn keine der vorgeschlagenen Optionen Ihren Anforderungen ähnelt, gibt es zwei Möglichkeiten, die Sie testen können. Um eine neue Editor-Registerkarte mit einer Liste anderer Vorschläge zu öffnen, drücken Sie die Taste **STRG** + **EINGABETASTE**. Diese Tastenkombination öffnet eine neue Registerkarte mit bis zu 10 weiteren Vorschlägen. Auf jeden Vorschlag folgt eine Schaltfläche, mit der Sie den Vorschlag annehmen können. Die Registerkarte wird automatisch geschlossen, nachdem Sie einen Vorschlag angenommen haben. Die andere Option besteht darin, die **ESC**-TASTE zu drücken, um die Vorschläge zu schließen und es erneut zu versuchen. Sie können den Codekommentar anpassen, um mehr Kontext zum Arbeiten für GitHub Copilot bereitzustellen.

    > [!NOTE]
    > GitHub Copilot kann gelegentlich einen Vorschlag in Phasen machen. In diesem Fall können Sie die EINGABETASTE drücken, um weitere Phasen des Vorschlags nach Drücken der TAB-Taste anzuzeigen.

1. Um eine vorgeschlagene Datenstruktur zu akzeptieren, drücken Sie die TAB-Taste, oder wählen Sie **Annehmen** aus.

1. Aktualisieren Sie den Code wie folgt, um die Felddatentypen zu ändern:

    ```csharp

    public struct SalesData
    {
        public DateOnly dateSold;
        public string departmentName;
        public int productID;
        public int quantitySold;
        public double unitPrice;
    }

    ```

    Durch schnelle Anpassungen an Codeabschlussvorschlägen können Sie sicherstellen, dass Sie den gewünschten Code erstellen. Es ist besonders wichtig, früh im Entwicklungsprozess Korrekturen vorzunehmen, wenn immer noch große Teile Ihrer Codebasis entwickelt werden müssen. Nachfolgende Codevervollständigungen basieren auf dem Code, den Sie bereits geschrieben haben. Daher ist es wichtig, sicherzustellen, dass Ihr Code möglichst präzise ist.

1. Erstellen Sie zwei leere Codezeilen unterhalb der `SalesData`-Datenstruktur.

1. Um eine Methode zu erstellen, die Testdaten mithilfe der `SalesData` Datenstruktur generiert, schreiben Sie den folgenden Codekommentar, und drücken Sie dann die EINGABETASTE:

    ```C#
    /* the GenerateSalesData method returns 1000 SalesData records. It assigns random values to each field of the data structure */
    ```

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Codevervollständigungsvorschläge zu überprüfen.

    Beachten Sie, dass die `GenerateSalesData` Methode so konzipiert ist, dass ein Array von `SalesData` Objekten zurückgegeben wird. Die Methode generiert 1.000 Datensätze mit Testdaten, wobei Zufallswerte jedem Feld der `SalesData`-Datenstruktur zugewiesen sind.

    Sie sollten die Vorschläge von GitHub Copilot und GitHub Copilot Chat immer überprüfen, auch wenn sie korrekt erscheinen.

    > [!NOTE]
    > Wenn GitHub Copilot eine einzelne Codezeile anstelle einer abgeschlossenen `GenerateSalesData`-Methode vorschlägt, drücken Sie **STRG+EINGABETASTE**, um die Registerkarte „GitHub Copilot-Vorschläge“ zu öffnen. Überprüfen Sie die Vorschläge auf der neuen Registerkarte. Verwenden Sie im nächsten Schritt die Schaltfläche „Vorschlagnr. akzeptieren“, um den Vorschlag anzunehmen. GitHub Copilot präsentiert Vorschläge gelegentlich inkrementell. Obwohl Sie die Codeabschlusse inkrementell akzeptieren können, ist es besser, die Registerkarte „GitHub Copilot-Vorschläge“ zu verwenden, um den vollständigen Vorschlag zu überprüfen, bevor Sie eine Entscheidung treffen, ihn anzunehmen oder zu verwerfen.

1. Scrollen Sie durch die Vorschläge für die Codevervollständigung, und wählen Sie die beste Übereinstimmung für die Anforderungen aus.

1. Um die Codevervollständigung zu akzeptieren, drücken Sie die TAB-Taste.

    Beachten Sie, dass der Codeabschlussvorschlag einen Syntaxfehler im Code enthält, der zum Generieren des Felds `DateSold` verwendet wird. `DateOnly` akzeptiert drei ganzzahlige Werte, die in der richtigen Reihenfolge aufgeführt werden müssen: **Jahr**, **Monat**, **Tag**.

1. Um ein einzelnes Jahr für den Code anzugeben, der zum Generieren des `DateSold` Felds verwendet wird, aktualisieren Sie die Codezeile wie folgt:

    ```C#
    salesData[i].DateSold = new DateOnly(2023, random.Next(1, 13), random.Next(1, 29));
    ```

1. Passen Sie bei Bedarf die anderen Codezeilen an den folgenden Codeschnipsel an:

    ```csharp

    public SalesData[] GenerateSalesData()
    {
        SalesData[] salesData = new SalesData[1000];
        Random random = new Random();
        for (int i = 0; i < salesData.Length; i++)
        {
            salesData[i].dateSold = new DateOnly(2023, random.Next(1, 13), random.Next(1, 29));
            salesData[i].departmentName = "Department " + random.Next(1, 11);
            salesData[i].productID = random.Next(1, 101);
            salesData[i].quantitySold = random.Next(1, 101);
            salesData[i].unitPrice = random.NextDouble() * 100;
        }
        return salesData;
    }

    ```

Die Möglichkeit, Code aus Codekommentaren zu generieren, ist ein leistungsfähiges Feature von GitHub Copilot. Mit nur zwei Kommentaren konnten Sie eine Datenstruktur und eine Methode generieren, die Testdaten generiert.

### Verwenden von GitHub Copilot zum Generieren von Codezeilenvervollständigungen

GitHub Copilot kann Codezeilenvervollständigungen basierend auf dem eingegebenen Code generieren. Sie können Codezeilenvervollständigungen auf zwei Arten generieren:

- Beginnen Sie mit der Eingabe einer Codezeile, und warten Sie dann, bis GitHub Copilot eine Autovervollständigung für Ihre nicht fertige Codezeile vorschlägt.
- Geben Sie eine vollständige Codezeile ein, drücken Sie die **EINGABETASTE**, und warten Sie dann, bis GitHub Copilot eine automatische Vervollständigung für die nächste Codezeile vorschlägt.

> [!NOTE]
> GitHub Copilot generiert vorgeschlagene Codevervollständigungen basierend auf dem eingegebenen Code und dem vom Code in Ihrer App definierten Kontext. Je mehr Code Sie in Ihrer App haben, vorausgesetzt, es ist guter Qualitätscode, desto mehr Kontext hat GitHub Copilot verfügbar. Mit zunehmender Menge und Qualität des vorhandenen Codes steigt auch die Qualität und Zuverlässigkeit der von GitHub Copilot vorgeschlagenen Codezeilenvervollständigungen. GitHub Copilot ist sehr gut beim Generieren von Codezeilenvervollständigungen für gängige Programmieraufgaben und Muster geeignet, insbesondere, wenn eine Abfolge verwandter Komponenten generiert werden muss.

In diesem Teil der Demo arbeiten Sie an der `QuarterlySalesReport`-Methode.

Hier sind die Aufgaben, die Sie ausführen müssen:

- Aktualisieren Sie den Methodenkonstruktor mit einem Parameter, der die Auflistung von `SalesData` Objekten akzeptiert.
- Verwenden Sie GitHub Copilot, um Codezeilenvervollständigungen zu generieren, die Umsatzdaten für den Quartalsbericht verarbeiten.
- Führen Sie nun die App aus, und überprüfen Sie den vierteljährlichen Umsatzbericht.

Führen Sie die folgenden Schritte aus, um diesen Abschnitt der Demo zu absolvieren:

1. Aktualisieren Sie den Methodenkonstruktor für `QuarterlySalesReport` wie folgt:

    ```C#
    public void QuarterlySalesReport(SalesData[] salesData)
    ```

1. Nehmen Sie sich eine Minute Zeit, um den Code zu berücksichtigen, den Sie entwickeln müssen.

    Das Konzept ist recht klar. Sie möchten, dass ihr Code vierteljährliche Umsätze basierend auf Ihren Umsatzdaten berechnet und dann einen Bericht schreibt. Dazu muss Ihr Code folgendes tun:

    - Die Sammlung `salesData` durchlaufen.
    - Den Wert jedes Verkaufs basierend auf der verkauften Menge und dem Einzelpreis berechnen.
    - Das Verkaufsdatum verwenden, um zu bestimmen, zu welchem Quartal ein Verkauf gehört.
    - Den Umsatz für jedes Quartal summieren.
    - Einen Bericht über den Umsatz nach Quartal schreiben.

    Eine Option besteht darin, mit der Eingabe des Codes für eine `foreach` Schleife zu beginnen und dann zu sehen, was GitHub Copilot vorschlägt.

1. Erstellen Sie in der `QuarterlySalesReport`-Methode eine neue Codezeile oben im Codeblock.

    Zwischen der neuen Codezeile und der Codezeile, die `Console.WriteLine()` enthält, muss sich mindestens eine leere Codezeile befinden.

1. Um eine Codezeilenvervollständigung zu generieren, geben Sie `foreach (` ein, und warten Sie dann, bis GitHub Copilot Optionen für die Codezeilenvervollständigung vorschlägt.

1. Überprüfen Sie die von GitHub Copilot vorgeschlagene Codevervollständigung.

    Der vorgeschlagene Codeabschluss ist nicht der, den Sie wollten.

    Obwohl GitHub Copilot eine `foreach` Schleife vorschlägt, die `salesData` durchläuft, gibt es keine Analysen oder Berechnungen innerhalb der Schleife. Jede der vorgeschlagenen Optionen enthält `Console.WriteLine`-Anweisungen, die Sie nicht möchten oder benötigen.

1. Nehmen Sie sich eine Minute Zeit, um zu überlegen, warum GitHub Copilot `Console.WriteLine` Anweisungen vorschlägt.

    Erinnern Sie sich, dass GitHub Copilot Vorschläge für die Codevervollständigung basierend auf dem Kontext Ihres Codes generiert. In diesem Fall hat GitHub Copilot nicht wirklich viel Code zu berücksichtigen. Und die Situation wird schlimmer.

    Der Code, den GitHub Copilot in Ihrer Methode sieht, ist eine `Console.WriteLine`-Anweisung. Da innerhalb der Methode kein anderer Kontext verfügbar ist und keine ähnlichen Methoden in Ihrer Codebasis zur Verfügung stehen, kommt GitHub Copilot zu dem Schluss, dass Sie *möglicherweise* `Console.WriteLine`-Anweisungen innerhalb der `foreach`-Schleife benötigen.

    GitHub Copilot funktioniert am besten, wenn Ihr Code sauber und fokussiert ist. Wenn Sie überflüssige Codekommentare oder Anweisungen in Ihrem Code entdecken, sollten Sie sie entfernen, bevor Sie versuchen, GitHub Copilot-Codevervollständigungen zu verwenden.

1. Führen Sie die folgenden Schritte aus, um Ihren Code zu bereinigen, bevor Sie GitHub Copilot einen weiteren Versuch ausführen lassen:

    - Brechen Sie die vorgeschlagene `foreach (` Codevervollständigung ab.
    - Löschen Sie die von Ihnen eingegebene partielle `foreach (` Anweisung.
    - Löschen Sie die `Console.WriteLine` Anweisung aus Ihrer `QuarterlySalesReport` Methode.

    Jetzt sollten Sie bereit sein, GitHub Copilot erneut zu versuchen.

1. Stellen Sie sicher, dass die `QuarterlySalesReport` Methode dem folgenden Code ähnelt:

    ```C#
    public void QuarterlySalesReport(SalesData[] salesData)
    {


    }
    ```

1. Positionieren Sie den Cursor in einer leeren Codezeile innerhalb der `QuarterlySalesReport` Methode, und drücken Sie dann die EINGABETASTE.

    Es kann einen Moment dauern, bis GitHub Copilot die vorgeschlagene Codevervollständigung generiert.

1. Nehmen Sie sich eine Minute Zeit, um die vorgeschlagenen Codevervollständigungen zu überprüfen.

    > [!NOTE]
    > Obwohl GitHub Copilot nur über einen Methodennamen und Parameter verfügt, mit dem gearbeitet werden kann, kann dies ausreichen, um nützliche Vorschläge zu generieren. Es sollten Vorschläge zum Berechnen von Umsätzen nach Quartal angezeigt werden. Wenn Sie die Vorschläge ablehnen und es erneut versuchen, können unterschiedliche Ergebnisse erzielt werden.

    Sie können die Vorschläge durchlaufen, indem Sie `>` oder `<` auswählen.

    Beachten Sie, dass die vorgeschlagene Codevervollständigung die Umsatzdaten durchläuft und vierteljährliche Umsatzberechnungen durchführt.

1. Um die vorgeschlagene Codevervollständigung zu akzeptieren, drücken Sie die TAB-Taste.

    Die vorgeschlagene Codevervollständigung berechnet und zeigt das Quartalseinkommen basierend auf Umsatzdaten an.

    ```csharp

    // create a dictionary to store the quarterly sales data
    Dictionary<string, double> quarterlySales = new Dictionary<string, double>();
    // iterate through the sales data
    foreach (SalesData data in salesData)
    {
        // calculate the total sales for each quarter
        string quarter = GetQuarter(data.dateSold.Month);
        double totalSales = data.quantitySold * data.unitPrice;
        if (quarterlySales.ContainsKey(quarter))
        {
            quarterlySales[quarter] += totalSales;
        }
        else
        {
            quarterlySales.Add(quarter, totalSales);
        }
    }
    // display the quarterly sales report
    Console.WriteLine("Quarterly Sales Report");
    Console.WriteLine("----------------------");
    foreach (KeyValuePair<string, double> quarter in quarterlySales)
    {
        Console.WriteLine(entry.Key + ": $" + entry.Value);
    }

    ```

1. Beachten Sie, dass die `GetQuarter` Methode verwendet wird, um das Quartal basierend auf dem Monat des Verkaufs zu bestimmen.

    Diese Methode wird nicht in Ihrem Code implementiert, ist jedoch erforderlich, damit der Code erstellt und ausgeführt werden kann.

1. Erstellen Sie zwei leere Codezeilen unterhalb der `QuarterlySalesReport`-Methode.

1. Beachten Sie, dass GitHub Copilot eine Codevervollständigung für die `GetQuarter` Methode vorschlägt.

    Mit dem von der `QuarterlySalesReport` Methode bereitgestellten Kontext kann GitHub Copilot problemlos eine Codevervollständigung für die `GetQuarter` Methode generieren, die das Quartal basierend auf dem Monat des Verkaufs bestimmt.

1. Nehmen Sie sich eine Minute Zeit, um die vorgeschlagene Codezeilenvervollständigung für die `GetQuarter` Methode zu überprüfen.

1. Um die vorgeschlagene Codevervollständigung zu akzeptieren, drücken Sie die TAB-Taste.

    ```csharp

    public string GetQuarter(int month)
    {
        if (month >= 1 && month <= 3)
        {
            return "Q1";
        }
        else if (month >= 4 && month <= 6)
        {
            return "Q2";
        }
        else if (month >= 7 && month <= 9)
        {
            return "Q3";
        }
        else
        {
            return "Q4";
        }
    }

    ```

1. Beachten Sie, dass die `Main` Methode abgeschlossen werden muss, bevor Sie den Code ausführen können.

    Sie können die Kommentare in der `Main` Methode verwenden, um Ihren Code zu aktualisieren.

1. Positionieren Sie den Cursor am Ende des `// call the GenerateSalesData method` Codekommentars, und drücken Sie dann die EINGABETASTE.

    GitHub Copilot verwendet den Kommentar, um eine aufrufende Anweisung für die Methode vorzuschlagen.

1. Überprüfen und akzeptieren Sie dann die von GitHub Copilot vorgeschlagene Codevervollständigung.

1. Wiederholen Sie den Vorgang für den `// call the QuarterlySalesReport method` Codekommentar.

1. Ihre `Main`-Methode sollte den folgenden Code enthalten:

    ```csharp

    static void Main(string[] args)
    {
        // create a new instance of the class
        QuarterlyIncomeReport report = new QuarterlyIncomeReport();
        // call the GenerateSalesData method
        SalesData[] salesData = report.GenerateSalesData();
        // call the QuarterlySalesReport method
        report.QuarterlySalesReport(salesData);
    }

    ```

1. Nehmen Sie sich eine Minute Zeit, um den Code in Ihrem `QuarterlyIncomeReport` Kurs zu überprüfen.

    ```csharp

    namespace ReportGenerator
    {
        class QuarterlyIncomeReport
        {
            static void Main(string[] args)
            {
                // create a new instance of the class
                QuarterlyIncomeReport report = new QuarterlyIncomeReport();
                // call the GenerateSalesData method
                SalesData[] salesData = report.GenerateSalesData();
                // call the QuarterlySalesReport method
                report.QuarterlySalesReport(salesData);
            }
            /* public struct SalesData includes the following fields: date sold, department name, product ID, quantity sold, unit price */
            public struct SalesData
            {
                public DateOnly dateSold;
                public string departmentName;
                public int productID;
                public int quantitySold;
                public double unitPrice;
            }
            /* the GenerateSalesData method returns 1000 SalesData records. It assigns random values to each field of the data structure */
            public SalesData[] GenerateSalesData()
            {
                SalesData[] salesData = new SalesData[1000];
                Random random = new Random();
                for (int i = 0; i < 1000; i++)
                {
                    salesData[i].dateSold = new DateOnly(2023, random.Next(1, 13), random.Next(1, 29));
                    salesData[i].departmentName = "Department " + random.Next(1, 11);
                    salesData[i].productID = random.Next(1, 101);
                    salesData[i].quantitySold = random.Next(1, 101);
                    salesData[i].unitPrice = random.NextDouble() * 100;
                }
                return salesData;
            }
            public void QuarterlySalesReport(SalesData[] salesData)
            {
                // create a dictionary to store the quarterly sales data
                Dictionary<string, double> quarterlySales = new Dictionary<string, double>();
                // iterate through the sales data
                foreach (SalesData data in salesData)
                {
                    // calculate the total sales for each quarter
                    string quarter = GetQuarter(data.dateSold.Month);
                    double totalSales = data.quantitySold * data.unitPrice;
                    if (quarterlySales.ContainsKey(quarter))
                    {
                        quarterlySales[quarter] += totalSales;
                    }
                    else
                    {
                        quarterlySales.Add(quarter, totalSales);
                    }
                }
                // display the quarterly sales report
                Console.WriteLine("Quarterly Sales Report");
                Console.WriteLine("----------------------");
                foreach (KeyValuePair<string, double> quarter in quarterlySales)
                {
                    Console.WriteLine(entry.Key + ": $" + entry.Value);
                }
            }
            public string GetQuarter(int month)
            {
                if (month >= 1 && month <= 3)
                {
                    return "Q1";
                }
                else if (month >= 4 && month <= 6)
                {
                    return "Q2";
                }
                else if (month >= 7 && month <= 9)
                {
                    return "Q3";
                }
                else
                {
                    return "Q4";
                }
            }
        }
    }
    
    ```

    Dieser Code wurde fast vollständig mit Codezeilenvervollständigungen erstellt, die von GitHub Copilot generiert wurden. Ihre Überprüfung von Codevorschlägen ist jedoch wichtig, und Korrekturen waren erforderlich. Sie sollten immer die von GitHub Copilot vorgeschlagenen Codevervollständigungen überprüfen, um sicherzustellen, dass der Code Ihre Anforderungen erfüllt.

1. Führen Sie die App aus, um die Berichtsausgabe zu überprüfen.

    Öffnen Sie ein Terminalfenster in Visual Studio Code, und geben Sie dann den folgenden Befehl ein:

    ```bash
    dotnet run
    ```

    Die Ausgabe sollte den Quartalseinkommensbericht anzeigen, der den Abteilungsnamen, das Quartal und das Einkommen für jede Abteilung und jedes Quartal anzeigt, die in den Testdaten dargestellt sind.

1. Überprüfen Sie die Ausgabe im Fenster „Terminal“.

    Obwohl die Quartalsergebnisse auf zufälligen numerischen Werten basieren, sollte ein Bericht angezeigt werden, der der folgenden Ausgabe ähnelt:

    ```output

    Quarterly Sales Report
    ----------------------
    Q3: $635637.5019563352
    Q4: $672247.315297204
    Q2: $667269.194630603
    Q1: $642769.2700531208

    ```

    Es sind noch weitere Schritte erforderlich, um den Kurs zu `QuarterlyIncomeReport` abzuschließen. In der nächsten Einheit verwenden Sie GitHub Copilot Chat, um Ihre App zu erweitern und zu aktualisieren.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot verwendet, um Codezeilenvervollständigungen in Ihrer Visual Studio Code-Umgebung zu generieren. Sie haben Codekommentare verwendet, um eine Datenstruktur und eine Methode zu generieren, die Testdaten generiert. Sie haben auch Codezeilenvervollständigungen verwendet, um den Code zu generieren, der Verkaufsdaten für einen Quartalseinkommensbericht verarbeitet.
