---
demo:
  title: 'Demo: Erstellen von Code mithilfe von GitHub Copilot Inline Chat'
  module: 'Module 3: Develop code features using GitHub Copilot tools'
---

# Demo: Erstellen von Code mithilfe von GitHub Copilot Inline Chat

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Die GitHub Copilot Chat-Erweiterung für Visual Studio Code enthält drei Chatschnittstellen:

- Die **Chatansicht** bietet einen KI-Assistenten, der Ihnen jederzeit helfen kann.
- Ein **Quick Chat**-Fenster kann verwendet werden, um eine schnelle Frage zu stellen und dann wieder zu dem zurückzugehen, was Sie tun.
- Die **Inlinechat**-Schnittstelle wird direkt im Editor für kontextbezogene Interaktionen geöffnet, während Sie codieren.

Die Chatansicht und das Quick Chat-Fenster ermöglichen interaktive Konversationen mit Mehrfachdurchläufen mit der KI. Beide Schnittstellen bieten eine Möglichkeit, Fragen zu stellen, Hilfe zu einem Codierungsproblem zu erhalten und Code zu generieren. Während einer Unterhaltung enthalten GitHub Copilot-Antworten Text in natürlicher Sprache, Codeblöcke und andere Elemente. Wenn Codeblöcke in einer Antwort bereitgestellt werden, können Sie sie kopieren oder direkt in Ihren Code-Editor einfügen.

Die Inlinechat-Schnittstelle wurde entwickelt, um kontextbezogene Hilfe und Codevorschläge bereitzustellen, während Sie codieren.

In dieser Demo verwenden Sie das Inlinechatfeature von GitHub Copilot, um neue Codefeatures zu generieren. Die Demo ist eine Fortsetzung des Projektszenarios in der vorherigen Demo. Verwenden Sie die vorbereitete Beispiel-App `APL2007M3SalesReport-InlineChat`, um die Demo zu starten. Während der Demo aktualisieren Sie die `SalesData`-Datenstruktur und die `GenerateSalesData`-Methode. Außerdem aktualisieren Sie die `QuarterlySalesReport`-Methode so, dass sie zusätzliche Berechnungen und Anzeigeoptionen enthält.

#### Überprüfen der Codierungsaufgaben und Projektziele

Diese Demo konzentriert sich auf die Verwendung von GitHub Copilot, um die folgenden Aufgaben zu beschleunigen:

1. Sie aktualisieren die `SalesData`-Datenstruktur und die `GenerateSalesData`-Methode, um ein Datenbeispiel zu erzeugen, das tatsächlichen Daten ähnelt.

    - dateSold: Es sind keine Änderungen erforderlich.
    - departmentName: Die Zeichenfolgenwerte sollten zufällig aus einer Liste von 8 Abteilungen ausgewählt werden. Erstellen Sie für jeden Abteilungsnamen eine 4-stellige Abkürzung, die in der productID enthalten sein kann.
    - productID: Wechseln sie von Datentyp `int` zu `string`. Die productID-Werte sollten mithilfe des Musters „`DDDD-###-SS-CC-MMM`“ formatiert werden, wobei die Komponenten der ID wie folgt definiert sind:

        - ein 4-stelliger Code, der die Abteilung darstellt.
        - eine 3-stellige Zahl, die das Produkt darstellt.
        - ein 2-stelliger Code, der die Produktgröße darstellt.
        - ein 2-stelliger Code, der die Produktfarbe darstellt.
        - ein 3-stelliger Code, der die Fertigungsstätte darstellt (zufällig aus einer Liste von 10 Fertigungsstandorten ausgewählt). Bei den Codes sollte es sich um eine 2-Buchstaben-ISO-Landeskennzahl handeln, gefolgt von einer Ziffer (z. B. US1, CA2, MX3 usw.).

    - quantitySold: Es sind keine Änderungen erforderlich.
    - unitPrice: Erhöhen Sie die untere Grenze des Preisbereichs auf 25 und die obere Grenze auf 300.
    - baseCost: Fügen Sie ein Feld für die Herstellungskosten des Elements hinzu. Die baseCost-Werte sollten mit zufällig generierten Rabatten vom unitPrice (5 bis 20 Prozent) generiert werden.
    - volumeDiscount: Fügen Sie ein Feld für einen Volumenrabattprozentsatz hinzu. Der Wert, der volumeDiscount zugewiesen ist, sollte die ganzzahlige Komponente von 10 Prozent der quantitySold sein (10% von 19 Einheiten = 1% volumeDiscount).
    - Erhöhen Sie die Anzahl der Datensätze, die generiert wurden, auf 10.000.

1. Sie aktualisieren die `QuarterlySalesReport`-Methode wie folgt:

    1. Beim Anzeigen der Verkaufsergebnisse listen Sie die Ergebnisse in einer logischen Reihenfolge auf. Wenn Sie beispielsweise den Gesamtverkauf nach Quartal auflisten, sollten die Quartale in der Reihenfolge von Q1 bis Q4 aufgeführt werden.
    1. Zeigt Währungswerte mit regionalen Einstellungen an.
    1. Berechnungen für Quartalsgewinn und Gewinnprozentsatz enthalten
    1. Berechnungen für quartalsmäßigen Umsatz, Gewinn und Gewinnprozentsatz nach Abteilung enthalten.

#### Erläutern Ihres Ansatzes bei der Entwicklung von Prompts für GitHub Copilot Chat

Die Inline-Chatfunktion von GitHub Copilot verwendet die Eingabeaufforderung, die Sie übermitteln, um die Aufgaben oder Probleme zu verstehen, die Sie lösen möchten. Ihre Eingabeaufforderungen sollten spezifisch und prägnant sein. Gute Eingabeaufforderungen liefern bessere Antworten.

Berücksichtigen Sie beim Entwickeln von Eingabeaufforderungen für GitHub Copilot die folgenden bewährten Methoden:

- Seien Sie spezifisch, und halten Sie es einfach: Stellen Sie klare und präzise Eingabeaufforderungen bereit, die die Aufgaben oder Probleme beschreiben, die Sie lösen möchten. Vermeiden Sie die Verwendung von komplexer Sprache und Fachausdrücken, die die KI verwirren könnten.
- Verwenden Sie natürliche Sprache: Schreiben Sie Eingabeaufforderungen in einem Unterhaltungston. Verwenden Sie natürliche Sprache, die Sie beim Sprechen mit einem Kollegen oder Teammitglied verwenden würden.
- Schlüsseln Sie komplexe Aufgaben auf: Wenn die Aufgabe komplex ist, unterteilen Sie sie in kleinere Schritte. Geben Sie Eingabeaufforderungen für jeden Schritt an, um GitHub Copilot dabei zu unterstützen, den richtigen Code zu generieren.
- Geben Sie Kontext an: Fügen Sie relevante Informationen hinzu, die GitHub Copilot dabei helfen, die Aufgaben oder Probleme zu verstehen, die Sie lösen möchten. Fügen Sie Details zu den Daten, Variablen oder Codeblöcken hinzu, die für die Eingabeaufforderung relevant sind.
- Verwenden Sie Chatteilnehmer, Schrägstrich-Befehle und Chatvariablen: Die Inlinechatfunktion von GitHub Copilot unterstützt Chatteilnehmer, Schrägstrich-Befehle und Chatvariablen. Verwenden Sie diese Features, um mit GitHub Copilot zu interagieren und zusätzlichen Kontext für Ihre Eingabeaufforderungen bereitzustellen.

### Generieren von Datenstrukturen mithilfe von Inlinechats

Projekte beginnen in der Regel mit den Features oder Parametern, die entweder behoben oder bekannt sind. Das Auswählen einer Datenquelle oder Erstellen von Beispieldaten ist häufig ein guter Ausgangspunkt.

In diesem Abschnitt der Demo verwenden Sie Datenstrukturen, um simulierte Umsatzdaten zu erstellen. Die Daten bieten nützlichen Kontext für GitHub Copilot, wenn Sie die `QuarterlySalesReport`-Methode aktualisieren.

> [!NOTE]
> In einem tatsächlichen Geschäftsprojekt sollten Sie wahrscheinlich historische Daten verwenden, um simulierte Daten zu generieren. In dieser Schulung bietet das Generieren simulierter Daten die Möglichkeit, die Verwendung der GitHub Copilot-Tools zu üben. Das Simulieren von Daten wird nicht als bewährte Methode für Geschäftsprojekte vorgeschlagen.

Ihre Projektziele geben an, dass Sie an den folgenden Datenstrukturen arbeiten müssen:

- Sie benötigen eine Liste mit 8 Abteilungsnamen. Jeder Abteilungsname sollte mit einer 4-stelligen Zeichenfolge abgekürzt werden. Wählen Sie eine Branche für Ihr fiktives Unternehmen wie Kleidung oder Sportausrüstung aus und lassen Sie GitHub Copilot dann ein Wörterbuch mit Abteilungsnamen und 4-Zeichen-Codes generieren.
- Sie benötigen eine Liste von 10 Produktionsstandorten. Jede Website sollte durch einen 3-stelligen Code dargestellt werden. Bei den Codes kann es sich um eine 2-Buchstaben-ISO-Landeskennzahl handeln, gefolgt von einer Ziffer (z. B. US1, CA2, MX3 usw.). Lassen Sie GitHub Copilot ein Wörterbuch von 10 Produktionsstandorten mit 3-4 Landeskennzahlen generieren.
- Sie müssen die `SalesData`-Datenstruktur aktualisieren. Sie müssen die folgenden neuen Felder einbinden: Abteilungscode, Produktionsstandortcode. Sie müssen auch den Datentyp für productID von `int` zu `string` ändern.

Führen Sie die folgenden Schritte aus, um die Datenstruktur zu erstellen und zu aktualisieren:

1. Öffnen Sie den Projektordner **APL2007M3SalesReport-InlineChat** in Visual Studio Code.

1. Stellen Sie sicher, dass die Anwendung ausgeführt wird und einen Bericht erzeugt, der der folgenden Ausgabe ähnelt:

    ```plaintext
    Quarterly Sales Report
    ----------------------
    Q3: $690095.7142725277
    Q4: $600536.3320750712
    Q2: $678194.7943550209
    Q1: $595963.0477790226
    ```

    Da die Daten zufällig generiert werden, variieren die numerischen Werte mit jeder Ausführung.

1. Öffnen Sie die Datei Program.cs.

1. Positionieren Sie den Cursor in einer leeren Zeile unterhalb der `SalesData`-Datenstruktur.

1. Um die Inlinechatschnittstelle zu öffnen, drücken Sie **STRG+I** auf der Tastatur.

1. Geben Sie den folgenden Prompt ein:

    ```output
    I need a public struct ProdDepartments that contains a static string array for 8 clothing industry departments. Create separate string array containing 4-character abbreviations for each department name. The abbreviation must be unique. The department names should represent real department names for the clothing industry.
    ```

    Wenn Sie eine bestimmte Liste mit Feldnamen haben, könnten Sie diese in der Eingabeaufforderung angeben. Beispielsweise können tatsächliche Unternehmensdaten verwendet werden, um die Abteilungsnamen anzugeben.

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge.

    Solange die Aufforderung klar und spezifisch ist, sollte GitHub Copilot einen nützlichen Vorschlag bereitstellen. Wenn der Vorschlag nicht ihren Erwartungen entspricht, können Sie ihn ablehnen und es erneut versuchen. In diesem Fall sind die Namen der Abteilungen nicht wichtig, sodass Sie den Vorschlag wahrscheinlich annehmen können.

    Ihre Datenstruktur sollte so ähnlich wie im folgenden Code aussehen:

    ```csharp

    public struct ProdDepartments
    {
        public static string[] DepartmentNames =  ["Men's Clothing", "Women's Clothing", "Children's Clothing", "Accessories", "Footwear", "Outerwear", "Sportswear", "Undergarments"];
        public static string[] DepartmentAbbreviations =  ["MENS", "WOMN", "CHLD", "ACCS", "FOOT", "OUTR", "SPRT", "UNDR" ];
    }

    ```

1. Um den Vorschlag anzunehmen, drücken Sie die TAB-Taste, oder wählen Sie **Annehmen** aus.

    Sie können auch die Inlinechatfunktion verwenden, um den neuen Code zu dokumentieren. Wählen Sie den Code aus, drücken Sie **STRG+I**, um den Inlinechat zu öffnen, geben Sie `/doc` ein, überprüfen Sie die vorgeschlagene Inlinedokumentation, und nehmen Sie dann das Update an.

1. Positionieren Sie den Cursor in einer leeren Zeile unterhalb der `ProdDepartments`-Datenstruktur.

1. Um die Inlinechatschnittstelle zu öffnen, drücken Sie **STRG+I** auf der Tastatur.

1. Geben Sie den folgenden Prompt ein:

    ```output
    I need a public struct ManufacturingSites that contains a static string array for 10 manSites. Manufacturing sites should be represented by a 3-character code that includes a 2-letter ISO country code followed by a digit. Use 3 ISO country codes.
    ```

    Wenn Sie eine bestimmte Liste mit Feldnamen haben, könnten Sie diese in der Eingabeaufforderung angeben. Beispielsweise können tatsächliche Unternehmensdaten verwendet werden, um die Feldnamen anzugeben.

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge.

    Ihre Datenstrukturen sollten so ähnlich wie im folgenden Code aussehen:

    ```csharp

    public struct ManufacturingSites
    {
        public static string[] manSites = [ "US1", "US2", "US3", "UK1", "UK2", "UK3", "JP1", "JP2", "JP3", "MX1" ];
    }

    ```

1. Um den Vorschlag anzunehmen, drücken Sie die TAB-Taste, oder wählen Sie **Annehmen** aus.

1. Wählen Sie die `SalesData`-Datenstruktur aus, und drücken Sie dann **STRG+I**, um die Inlinechatoberfläche zu öffnen.

    Sie müssen der `SalesData`-Datenstruktur (`double` und `int`) Felder für `baseCost` und `volumeDiscount` hinzufügen. Sie müssen auch den Datentyp für `productID` von `int` in `string` ändern.

1. Geben Sie den folgenden Prompt ein:

    ```output
    add double field baseCost and int field volumeDiscount to SalesData. Change productID from int to string.
    ```

    In der Praxis ist es möglicherweise einfacher, diese Änderungen manuell vorzunehmen. Mithilfe von GitHub Copilot können Sie jedoch lernen, wie Sie Ihre Aufforderungen strukturieren, um bessere Ergebnisse zu erzielen.

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

    Ihre aktualisierten SalesData-Datenstrukturen sollten so ähnlich wie im folgenden Code aussehen:

    ```csharp

    public struct SalesData
    {
        public DateOnly dateSold;
        public string departmentName;
        public string productID;
        public int quantitySold;
        public double unitPrice;
        public double baseCost;
        public int volumeDiscount;
    }

    ```

Mit den neuen und aktualisierten Datenstrukturen können Sie jetzt an der Aktualisierung der `GenerateSalesData`-Methode arbeiten.

### Aktualisieren der GenerateSalesData-Methode mithilfe von Inlinechats

Ihre Projektziele geben an, dass Sie die `GenerateSalesData`-Methode aktualisieren müssen, um ein Datenbeispiel zu erstellen, das „tatsächlichen“ Daten ähnelt. Sie haben die `SalesData`-Datenstruktur bereits aktualisiert, um neue Felder für Abteilungscode und Produktionsstandortcode einzubinden. Sie haben auch den Datentyp für `productID` von `int` zu `string`geändert. Jetzt müssen Sie die `GenerateSalesData`-Methode aktualisieren, um Daten für die aktualisierten Felder zu generieren.

Sie müssen die folgenden Updates implementieren:

- departmentName: Aktualisieren Sie den zugewiesenen Wert. Weisen Sie einen zufällig ausgewählten Abteilungsnamen aus der `ProdDepartments`-Datenstruktur zu.
- productID: Aktualisieren Sie den zugewiesenen Wert. Formatieren Sie die productID mithilfe des Musters „`DDDD-###-SS-CC-MMM`“, in dem die Komponenten der ID wie folgt definiert sind:

    - ein 4-stelliger Code, der die Abteilung darstellt. Verwenden Sie die Abkürzung aus der `ProdDepartments`-Datenstruktur, die dem zugewiesenen Abteilungsnamen entspricht.
    - eine 3-stellige Zahl, die das Produkt darstellt. Die erste Ziffer sollte die Indexnummer der zufällig ausgewählten Abteilung sein. Die nächsten beiden Ziffern sollten eine Zufallszahl zwischen 1 und 99 sein, aber beginnende Nullen enthalten. Beispielsweise sollte 1 als 01 formatiert werden.
    - ein 2-stelliger Code, der die Produktgröße darstellt. Wählen Sie zufällig eine Produktgröße aus einer Liste von 5 Größen aus: XS, S, M, L, XL.
    - ein 2-stelliger Code, der die Produktfarbe darstellt. Wählen Sie zufällig eine Produktfarbe aus einer Liste von 8 2-stelligen Farbkürzeln aus: BK, BL, GR, RD, YL, OR, WT, GY.
    - ein 3-stelliger Code, der die Fertigungsstätte darstellt. Wählen Sie zufällig einen Fertigungsstandort aus der `ManufacturingSites`-Datenstruktur aus.

- unitPrice: Erhöhen Sie die untere Grenze des Preisbereichs auf 25 und die obere Grenze auf 300. Gehen Sie davon aus, dass Größe und Farbe sich nicht auf den Einzelpreis auswirken.
- baseCost: Weisen Sie baseCost einen Wert zu, der die Herstellungskosten darstellt. Werte können mit zufällig generierten Rabatten (5 bis 20 Prozent) vom unitPrice generiert werden. Nicht realistisch, aber für diese Demo akzeptabel.
- volumeDiscount: Weisen Sie dem volumeDiscount einen Wert zu, der einen Prozentualen Rabatt darstellt, der dem Einzelhandelskäufer gewährt wird. Der Wert, der volumeDiscount zugewiesen ist, sollte die ganzzahlige Komponente von 10 Prozent der quantitySold sein (10% von 19 Einheiten = 1% volumeDiscount).

Führen Sie die folgenden Schritte aus, um die `GenerateSalesData`-Methode zu aktualisieren:

1. Suchen Sie die `GenerateSalesData`-Methode in der Datei Program.cs.

1. Wählen Sie die Codezeile aus, die zum Zuweisen des `departmentName`-Werts verwendet wird.

1. Um die Inlinechatschnittstelle zu öffnen, drücken Sie **STRG+I** auf der Tastatur.

1. Geben Sie den folgenden Prompt ein:

    ```output
    Update the departmentName assignment to randomly select a department name. Use the ProdDepartments data structure. 
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Erstellen Sie nach der `departmentName`-Zuweisung drei leere Codezeilen.

1. Nehmen Sie sich eine Minute Zeit, um zu überlegen, wie Sie den Wert erstellen möchten, der `productID` zugewiesen ist.

    Die productID-Werte sollten als „`DDDD-###-SS-CC-MMM`“ formatiert werden, wobei die Komponenten der ID wie folgt definiert sind:

    - `DDDD` ist ein 4-stelligen Code, der die Abteilung darstellt. Verwenden Sie die Abkürzung aus der `ProdDepartments`-Datenstruktur, die dem zugewiesenen Abteilungsnamen entspricht.
    - `###` ist 3 numerische Zeichen, die ein Produkt darstellen. Die erste Ziffer ist die Indexnummer der Abteilung. Als Nächstes kommt eine Zufallszahl zwischen 1-99 mit vorangestellter 0 (z. B.: 07).
    - `SS` ist ein 2-stelliger Code, der die Produktgröße darstellt. Wählen Sie zufällig eine Produktgröße aus einer Liste von 5 Größen aus: XS, S, M, L, XL.
    - `CC` ist ein 2-stelliger Code, der die Produktfarbe darstellt. Wählen Sie zufällig eine Produktfarbe aus einer Liste von 8 2-stelligen Farbkürzeln aus: BK, BL, GR, RD, YL, OR, WT, GY.
    - `MMM` ist ein 3-stelliger Code, der die Produktionsstätte darstellt. Wählen Sie zufällig einen Fertigungsstandort aus der `ManufacturingSites`-Datenstruktur aus.

    Diese Formatierungsspezifikation ist zu komplex, um sie als einzelne Eingabeaufforderung zu beschreiben. Sie sollte in kleinere Schritte unterteilt werden.

    Beachten Sie, dass die Indexnummer des ausgewählten departmentName verwendet werden kann, um die departmentAbbreviation auszuwählen und die erste Ziffer der Produktnummer zu berechnen.

1. Kopieren Sie die folgenden Variablendeklarationen und fügen Sie sie an der Stelle der von Ihnen erstellten zweiten leeren Codezeile ein.

    ```csharp

    int indexOfDept = 0;
    string deptAbb = "";
    string firstDigit = "";
    string nextTwoDigits = "";
    string sizeCode = "";
    string colorCode = "";
    string manufacturingSite = "";

    ```

    Sie sollten vor und nach den Variablendeklarationen eine leere Codezeile haben.

    Variablendeklarationen sind für Inlinechats nicht erforderlich, um Codeaktualisierungsvorschläge aus einem Prompt zu generieren. Sie helfen jedoch, GitHub Copilot in einer bestimmten Codezeile zu verankern, in die die Aktualisierung gehört.

1. Wählen Sie die `int indexOfDept = 0;`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Assign the array index for departmentName to indexOfDept.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge.

    Es sollte ein Vorschlag angezeigt werden, der die Arrayindexnummer zuweist, die dem ausgewählten departmentName entspricht, zu indexOfDept.

    Wenn Sie den erwarteten Vorschlag nicht erhalten, können Sie **Verwerfen** auswählen, um den Vorschlag abzulehnen, und es erneut versuchen. Die folgende Eingabeaufforderung bietet zusätzlichen Kontext für die Zuordnung:

    ```output
    Create an int named indexOfDept. Assign the array index number corresponding to the selected departmentName to indexOfDept.
    ```

    Diese Eingabeaufforderung gibt das Erstellen einer ganzzahligen Variablen namens `indexOfDept` sowie das Zuweisen eines Werts an. Sie können diese Eingabeaufforderung ausführen, ohne die Variable-Deklaration zu erstellen/auszuwählen, aber GitHub Copilot kann gelegentlich seinen Ankerpunkt verlieren, wenn Sie den Inlinechat ohne ausgewählten Code öffnen.

    > [!NOTE]
    > Die Schaltfläche **Änderungen umschalten** (auf die über das Dropdownmenü **Weitere Aktionen** rechts neben den Schaltflächen **Annehmen** und **Verwerfen** zugegriffen werden kann) kann verwendet werden, um den von der vorgeschlagenen Aktualisierung gelöschten Code ein-/auszublenden. Dies kann nützlich sein, wenn Sie den ursprünglichen Code und das vorgeschlagene Codeupdate anzeigen möchten.

1. Um den von GitHub Copilot bereitgestellten Vorschlag anzunehmen, wählen Sie **Annehmen** aus.

1. Wählen Sie die `string deptAbb = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Use indexOfDept to assign a department abbreviation to deptAbb.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge.

    Es sollte ein Vorschlag angezeigt werden, der die Arrayindexnummer zuweist, die dem ausgewählten departmentName entspricht, zu indexOfDept.

1. Um den von GitHub Copilot bereitgestellten Vorschlag anzunehmen, wählen Sie **Annehmen** aus.

1. Wählen Sie die `string firstDigit = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Assign indexOfDept + 1 to firstDigit.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Wählen Sie die `string string nextTwoDigits = ""; = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Assign a random number 1-99 to nextTwoDigits. Include a leading 0 for numbers less than 10.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Wählen Sie die `string sizeCode = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    From the list {XS, S, M, L, XL}, randomly select a product size and assign it to sizeCode.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

    In diesem Fall sollte ein Vorschlag angezeigt werden, welcher der `sizeCode`-Variablen eine zufällig ausgewählte Produktgröße zuweist. GitHub Copilot könnte die Verwendung einer oder mehrerer Codezeilen vorschlagen, um diesen Prompt zu erfüllen. So oder so wird es wahrscheinlich vorschlagen, ein Zeichenfolgenarray mit Produktgrößen zu erstellen und dann mithilfe von `random` eine der Größen zu `sizeCode` zuzuweisen.

1. Wählen Sie die `string colorCode = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    From the list {BK, BL, GR, RD, YL, OR, WT, GY}, randomly select a product color and assign it to colorCode.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Wählen Sie die `string manufacturingSite = "";`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Assign a randomly selected manufacturing site to manufacturingSite.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Nehmen Sie sich einen Moment Zeit, um den Code zu überprüfen.

    Sie sollten über eine Reihe von Codezeilen verfügen, die den Variablen, die zum Erstellen der productID verwendet werden, Werte zuweisen. Der nächste Schritt besteht darin, den productID-Wert zu erstellen.

    ```csharp

    int indexOfDept = Array.IndexOf(ProdDepartments.departmentNames, salesData[i].departmentName);
    string deptAbb = ProdDepartments.departmentAbbreviations[indexOfDept];
    string firstDigit = (indexOfDept + 1).ToString();
    string nextTwoDigits = random.Next(1, 100).ToString("D2");
    string sizeCode = new string[] { "XS", "S", "M", "L", "XL" }[random.Next(0, 5)];
    string colorCode = new string[] { "BK", "BL", "GR", "RD", "YL", "OR", "WT", "GY" }[random.Next(0, 8)];
    string manufacturingSite = ManufacturingSites.manufacturingSites[random.Next(0, ManufacturingSites.manufacturingSites.Length)];

    ```

1. Wählen Sie die `salesData[i].productID = random.Next(1, 101);`-Codezeile aus, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Add a "-" to deptAbb, nextTwoDigits, sizeCode, and colorCode. Combine deptAbb, firstDigit, nextTwoDigits, sizeCode, colorCode, and manufacturingSite to create the productID.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

    Es sollte ein Vorschlag angezeigt werden, der den productID-Wert mithilfe der zuvor zugewiesenen Variablen erstellt. Der Vorschlag sollte den erforderlichen Code enthalten, um die productID als „`DDDD-###-SS-CC-MMM`“ zu formatieren.

1. Aktualisieren Sie die `unitPrice`-Zuordnung manuell so, dass sie einen Bereich von 25 bis 300 wie folgt verwendet:

    ```csharp
    salesData[i].unitPrice = random.Next(25, 300) + random.NextDouble();
    ```

1. Erstellen Sie nach der `unitPrice`-Zuordnung eine leere Zeile.

1. Akzeptieren Sie den Codezeilenabschluss, der angezeigt wird:

    GitHub Copilot sollte einen Vorschlag bereitstellen, der `baseCost` einen Wert zuweist, welcher der folgenden Codezeile ähnelt:

    ```csharp
    salesData[i].baseCost = random.Next(10, 100) + random.NextDouble();
    ```

1. Wählen Sie die Codezeile aus, die zum Zuweisen eines Werts zu `salesData[i].baseCost` verwendet wird, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Discount the unitPrice by a random percentage between 5 and 20. Assign the result to baseCost.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Erstellen Sie eine leere Zeile nach der `baseCost`-Zuweisung, und akzeptieren Sie den Codezeilenabschluss, der angezeigt wird.

    GitHub Copilot sollte einen Vorschlag bereitstellen, der `volumeDiscount` einen Wert zuweist.

1. Wählen Sie die Codezeile aus, die zum Zuweisen eines Werts zu `salesData[i].volumeDiscount` verwendet wird, öffnen Sie den Inlinechat, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Assign 10 percent of quantitySold to volumeDiscount. Truncate any fractional values.
    ```

1. Überprüfen Sie die von GitHub Copilot bereitgestellten Vorschläge und wählen Sie dann **Annehmen** aus.

1. Die aktualisierte GenerateSalesData-Methode sollte nun dem folgenden Codeausschnitt ähneln:

    ```csharp

    public SalesData[] GenerateSalesData()
    {
        SalesData[] salesData = new SalesData[1000];
        Random random = new Random();
        for (int i = 0; i < 1000; i++)
        {
            salesData[i].dateSold = new DateOnly(2023, random.Next(1, 13), random.Next(1, 29));
            salesData[i].departmentName = ProdDepartments.departmentNames[random.Next(0, ProdDepartments.departmentNames.Length)];
            int indexOfDept = Array.IndexOf(ProdDepartments.departmentNames, salesData[i].departmentName);
            string deptAbb = ProdDepartments.departmentAbbreviations[indexOfDept];
            string firstDigit = (indexOfDept + 1).ToString();
            string nextTwoDigits = random.Next(1, 100).ToString("D2");
            string sizeCode = new string[] { "XS", "S", "M", "L", "XL" }[random.Next(0, 5)];
            string colorCode = new string[] { "BK", "BL", "GR", "RD", "YL", "OR", "WT", "GY" }[random.Next(0, 8)];
            string manufacturingSite = ManufacturingSites.manufacturingSites[random.Next(0, ManufacturingSites.manufacturingSites.Length)];
            salesData[i].productID = $"{deptAbb}-{firstDigit}{nextTwoDigits}-{sizeCode}-{colorCode}-{manufacturingSite}";
            salesData[i].quantitySold = random.Next(1, 101);
            salesData[i].unitPrice = random.Next(25, 300) + random.NextDouble();
            salesData[i].baseCost = salesData[i].unitPrice * (1 - (random.Next(5, 21) / 100.0));
            salesData[i].volumeDiscount = (int)(salesData[i].quantitySold * 0.1);
        }
        return salesData;
    }

    ```

1. Speichern Sie die Änderungen.

### Aktualisieren der QuarterlySalesReport-Methode mithilfe von Inlinechats

Sie müssen die `QuarterlySalesReport`-Methode aktualisieren. Basierend auf den Projektzielen müssen Sie die folgenden Updates implementieren:

- Beim Anzeigen der Verkaufsergebnisse listen Sie die Ergebnisse in einer logischen Reihenfolge auf. Wenn Sie beispielsweise den Gesamtverkauf nach Quartal auflisten, sollten die Quartale in der Reihenfolge von Q1 bis Q4 aufgeführt werden.
- Zeigt Währungswerte mit regionalen Einstellungen an.
- Addieren von Berechnungen für Quartalsgewinn und Gewinnprozentsatz
- Fügen Sie Berechnungen spezifisch für individuelle Abteilungen hinzu: Quartalsverkäufe, Gewinn und Gewinnprozentsatz.
- Fügen Sie Berechnungen für spezifische Fertigungsstätten hinzu: Quartalsverkäufe, Gewinn und Gewinnprozentsatz.

Jetzt sollte Ihre `QuarterlySalesReport`-Methode dem folgenden Codeausschnitt ähneln:

```csharp

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
        Console.WriteLine("{0}: ${1}", quarter.Key, quarter.Value);
    }
}

```

Führen Sie die folgenden Schritte aus, um die `QuarterlySalesReport`-Methode zu aktualisieren:

1. Führen Sie die Anwendung aus, um die aktuelle Ausgabe des Quartalsumsatzes zu überprüfen.

    Im Konsolenfenster sollte eine Liste der Quartalsumsatzergebnisse angezeigt werden. Zufallswerte werden verwendet, sodass numerische Daten bei jeder Ausführung variieren.

    Die Ausgabe des Quartalsumsatzberichts sollte wie folgt aussehen:

    ```output
    Quarterly Sales Report
    ----------------------
    Q3: $2060165.1045630067
    Q2: $2000706.5521363618
    Q4: $2168920.603583816
    Q1: $2174302.3663762277
    ```

    Beachten Sie, dass die Quartale nicht in der Reihenfolge aufgeführt sind und die Währungswerte nicht ordnungsgemäß formatiert sind.

    Ihre erste Aufgabe besteht darin, diese Probleme zu beheben.

1. Suchen Sie die `QuarterlySalesReport`-Methode in der Datei Program.cs.

1. Wählen Sie die gesamte Methode aus.

1. Öffnen Sie die Inlinechatschnittstelle, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Update the QuarterlySalesReport method to display quarterly results in order. Format currency using regional settings. 
    ```

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Vorschläge zu überprüfen.

    Es sollte ein Vorschlag angezeigt werden, der den erforderlichen Code zum Berechnen des Quartalsgewinns und des Gewinnprozentsatzes enthält. Der Vorschlag sollte den erforderlichen Code enthalten, um den Gewinn- und Gewinnprozentsatz für jedes Quartal zu berechnen.

1. Um den von GitHub Copilot bereitgestellten Vorschlag anzunehmen, wählen Sie **Annehmen** aus.

1. Speichern Sie die Änderungen.

1. Führen Sie die Anwendung aus und überprüfen Sie, ob die Quartalsumsatzergebnisse jetzt in der Reihenfolge angezeigt werden und dass die Währungswerte ordnungsgemäß formatiert sind.

    Obwohl die numerischen Werte unterschiedlich sind, sollte die Ausgabe des Quartalsumsatzberichts nun ähnlich wie die folgende Ausgabe formatiert sein:

    ```output
    Quarterly Sales Report
    ----------------------
    Q1: $2,174,302.37
    Q2: $2,000,706.55
    Q3: $2,060,165.10
    Q4: $2,168,920.60

    ```

    Der nächste Schritt besteht darin, Berechnungen für Quartalsgewinn und Gewinnprozentsatz hinzuzufügen.

1. Suchen Sie die `QuarterlySalesReport`-Methode in der Datei Program.cs.

1. Wählen Sie die gesamte Methode aus.

1. Öffnen Sie die Inlinechatschnittstelle, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```output
    Update the QuarterlySalesReport method to include calculations for quarterly profit and profit percentage. Include the new calculations in the report output.
    ```

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Vorschläge zu überprüfen.

    Es sollte ein Vorschlag angezeigt werden, der den erforderlichen Code zum Berechnen des Quartalsgewinns und des Gewinnprozentsatzes enthält. Der Vorschlag sollte den erforderlichen Code enthalten, um den Gewinn- und Gewinnprozentsatz für jedes Quartal zu berechnen.

1. Um den von GitHub Copilot bereitgestellten Vorschlag anzunehmen, wählen Sie **Annehmen** aus.

1. Wählen Sie **Annehmen** für die verbleibenden Vorschläge aus.

1. Speichern Sie die Änderungen.

1. Führen Sie die Anwendung aus und überprüfen Sie, ob die Quartalsumsatzergebnisse jetzt Berechnungen für Gewinn und Gewinnprozentsatz enthalten.

    Obwohl die numerischen Werte unterschiedlich sind, sollte die Ausgabe des Quartalsumsatzberichts nun ähnlich wie die folgende Ausgabe formatiert sein:

    ```output
    Quarterly Sales Report
    ----------------------
    Q1: Sales: $1,881,091.17, Profit: $231,351.24, Profit Percentage: 12.00%
    Q2: Sales: $1,949,240.91, Profit: $244,649.35, Profit Percentage: 11.00%
    Q3: Sales: $2,298,017.35, Profit: $273,622.53, Profit Percentage: 5.00%
    Q4: Sales: $2,279,185.96, Profit: $272,548.80, Profit Percentage: 16.00%    

    ```

    Der nächste Schritt besteht darin, Berechnungen für Quartalsumsatz, Gewinn und Gewinnprozentsatz nach Abteilung hinzuzufügen.

1. Wählen Sie die gesamte Methode aus.

1. So öffnen Sie die Inlinechatschnittstelle und geben dann die folgende Eingabeaufforderung ein:

    ```output
    Update the QuarterlySalesReport method to include calculations for quarterly sales, profit, and profit percentage by department. Include the new calculations in the report output. 
    ```

1. Nehmen Sie sich eine Minute Zeit, um die von GitHub Copilot bereitgestellten Vorschläge zu überprüfen.

    Es sollte ein Vorschlag angezeigt werden, der den erforderlichen Code zum Berechnen des Quartalsgewinns und des Gewinnprozentsatzes enthält. Der Vorschlag sollte den erforderlichen Code enthalten, um den Gewinn- und Gewinnprozentsatz für jedes Quartal zu berechnen.

1. Um den von GitHub Copilot bereitgestellten Vorschlag anzunehmen, wählen Sie **Annehmen** aus.

1. Wählen Sie **Annehmen** für die verbleibenden Vorschläge aus.

1. Speichern Sie die Änderungen.

1. Führen Sie die Anwendung aus und überprüfen Sie, ob die Quartalsumsatzergebnisse jetzt Berechnungen für Gewinn und Gewinnprozentsatz enthalten.

    Obwohl die numerischen Werte unterschiedlich sind, sollte die Ausgabe des Quartalsumsatzberichts nun ähnlich wie die folgende Ausgabe formatiert sein:

    ```output
    Quarterly Sales Report
    ----------------------
    Q1: Sales: $2,043,493.57, Profit: $262,571.72, Profit Percentage: 14.00%
    By Department:
    Department: Accessories, Sales: $188,977.90, Profit: $25,229.53, Profit Percentage: 14.00%
    Department: Children's Clothing, Sales: $186,552.49, Profit: $25,511.74, Profit Percentage: 13.00%
    Department: Footwear, Sales: $293,706.49, Profit: $39,224.99, Profit Percentage: 19.00%
    Department: Men's Clothing, Sales: $301,385.47, Profit: $36,756.06, Profit Percentage: 19.00%
    Department: Outerwear, Sales: $238,099.65, Profit: $24,371.92, Profit Percentage: 15.00%
    Department: Sportswear, Sales: $251,349.38, Profit: $34,142.40, Profit Percentage: 8.00%
    Department: Undergarments, Sales: $297,690.60, Profit: $35,305.13, Profit Percentage: 9.00%
    Department: Women's Clothing, Sales: $285,731.58, Profit: $42,029.95, Profit Percentage: 19.00%
    
    Q2: Sales: $1,925,948.90, Profit: $232,929.95, Profit Percentage: 17.00%
    By Department:
    Department: Accessories, Sales: $251,572.42, Profit: $33,250.17, Profit Percentage: 11.00%
    Department: Children's Clothing, Sales: $311,862.99, Profit: $36,537.33, Profit Percentage: 8.00%
    Department: Footwear, Sales: $203,148.87, Profit: $23,041.46, Profit Percentage: 11.00%
    Department: Men's Clothing, Sales: $229,781.14, Profit: $26,226.68, Profit Percentage: 9.00%
    Department: Outerwear, Sales: $211,610.47, Profit: $23,684.65, Profit Percentage: 9.00%
    Department: Sportswear, Sales: $204,083.63, Profit: $20,750.56, Profit Percentage: 8.00%
    Department: Undergarments, Sales: $264,733.26, Profit: $35,155.66, Profit Percentage: 15.00%
    Department: Women's Clothing, Sales: $249,156.13, Profit: $34,283.45, Profit Percentage: 17.00%
    
    Q3: Sales: $2,113,223.50, Profit: $256,591.16, Profit Percentage: 7.00%
    By Department:
    Department: Accessories, Sales: $288,161.91, Profit: $32,279.54, Profit Percentage: 10.00%
    Department: Children's Clothing, Sales: $198,313.55, Profit: $24,146.72, Profit Percentage: 7.00%
    Department: Footwear, Sales: $205,840.60, Profit: $27,630.49, Profit Percentage: 5.00%
    Department: Men's Clothing, Sales: $229,279.26, Profit: $26,618.62, Profit Percentage: 13.00%
    Department: Outerwear, Sales: $353,696.46, Profit: $44,634.82, Profit Percentage: 14.00%
    Department: Sportswear, Sales: $229,490.12, Profit: $27,697.91, Profit Percentage: 5.00%
    Department: Undergarments, Sales: $316,942.44, Profit: $40,518.71, Profit Percentage: 5.00%
    Department: Women's Clothing, Sales: $291,499.15, Profit: $33,064.35, Profit Percentage: 10.00%
    
    Q4: Sales: $1,896,279.88, Profit: $248,226.28, Profit Percentage: 15.00%
    By Department:
    Department: Accessories, Sales: $336,698.68, Profit: $44,714.55, Profit Percentage: 11.00%
    Department: Children's Clothing, Sales: $193,345.18, Profit: $23,261.33, Profit Percentage: 13.00%
    Department: Footwear, Sales: $215,183.23, Profit: $29,616.00, Profit Percentage: 15.00%
    Department: Men's Clothing, Sales: $171,663.38, Profit: $24,299.37, Profit Percentage: 5.00%
    Department: Outerwear, Sales: $229,791.52, Profit: $28,211.17, Profit Percentage: 15.00%
    Department: Sportswear, Sales: $230,031.90, Profit: $32,732.40, Profit Percentage: 8.00%
    Department: Undergarments, Sales: $300,824.19, Profit: $34,649.79, Profit Percentage: 6.00%
    Department: Women's Clothing, Sales: $218,741.80, Profit: $30,741.67, Profit Percentage: 20.00%

    ```

### Zusammenfassung

In dieser Demo haben Sie die Inlinechatfunktion verwendet, um die `GenerateSalesData`- und `QuarterlySalesReport`-Methoden zu aktualisieren. Sie haben der `SalesData`-Datenstruktur neue Felder hinzugefügt und dann die `GenerateSalesData`-Methode aktualisiert, um Daten für die neuen Felder zu generieren. Außerdem haben Sie die `QuarterlySalesReport`-Methode aktualisiert, um Berechnungen für Quartalsgewinn und Gewinnprozentsatz einzuschließen. Darüber hinaus haben Sie Berechnungen für Quartalsumsatz, Gewinn und Gewinnprozentsatz nach Abteilung hinzugefügt.
