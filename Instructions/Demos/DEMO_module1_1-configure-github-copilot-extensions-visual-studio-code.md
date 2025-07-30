---
demo:
  title: 'Demo: Konfigurieren von GitHub Copilot Erweiterungen für Visual Studio Code'
  module: 'Module 1: Get started with GitHub Copilot'
---

# Demo: Konfigurieren von GitHub Copilot Erweiterungen für Visual Studio Code

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

GitHub Copilot-Einstellungen werden in Ihrem GitHub.com-Konto und in der Visual Studio Code-Umgebung konfiguriert. In Visual Studio Code greifen Sie mithilfe des GitHub Copilot-Statusmenüs auf Einstellungen für GitHub Copilot und GitHub Copilot Chat zu.

Mit den Einstellungen in Visual Studio Code können Sie GitHub Copilot für bestimmte Sprachen aktivieren oder deaktivieren, das Verhalten von GitHub Copilot Chat konfigurieren und die GitHub Copilot-Erfahrung an Ihre Vorlieben anpassen. Sie können GitHub Copilot-Einstellungen auch auf GitHub.com konfigurieren, um Ihr GitHub Copilot-Abonnement zu verwalten, die Aufbewahrung von Prompts und Vorschlägen zu konfigurieren und Vorschläge zuzulassen oder zu blockieren, die mit öffentlichem Code übereinstimmen.

## Aktivieren oder Deaktivieren von GitHub Copilot

GitHub Copilot ist standardmäßig aktiviert, wenn Sie die Erweiterung in Visual Studio Code installieren. Sie können GitHub Copilot für einen bestimmten Zeitraum deaktivieren, falls erforderlich.

Führen Sie die folgenden Schritte aus, um die Optionen zum Aktivieren und Deaktivieren für die GitHub Copilot-Erweiterung anzuzeigen:

1. Öffnen Sie in Visual Studio Code die Ansicht **Erweiterungen**.

1. Scrollen Sie in der Liste der installierten Erweiterungen nach unten zu **GitHub Copilot**.

1. Wenn Sie ein Dropdownmenü für die GitHub Copilot-Erweiterung anzeigen möchten, das auch die Optionen „Aktivieren“ und „Deaktivieren“ enthält, wählen Sie das Zahnradsymbol neben GitHub Copilot aus.

Wenn Sie die Optionen zum Aktivieren und Deaktivieren veranschaulichen möchten, können Sie die Option „Deaktivieren“ auswählen. Achten Sie jedoch darauf, GitHub Copilot erneut zu aktivieren, bevor Sie mit dieser Demo fortfahren.

## Konfigurieren von GitHub Copilot und Copilot Chat in Visual Studio Code

Die GitHub Copilot-Erweiterungen werden mit Standardeinstellungen konfiguriert, wenn Sie die Erweiterungen in Visual Studio Code installieren. Sie können diese Einstellungen an Ihre Vorlieben anpassen.

Visual Studio Code bietet zwei Möglichkeiten, auf die Einstellungen für die GitHub Copilot-Erweiterungen zuzugreifen:

- Sie können das Symbol `Manage` verwenden, um die Registerkarte „Visual Studio Code-Einstellungen“ zu öffnen. Auf der Registerkarte „Einstellungen“ können Sie **Erweiterungen** und dann **Copilot** auswählen.
- Über das GitHub Copilot-Statussymbol können Sie auf das GitHub Copilot-Statusmenü zugreifen und dann **Einstellungen bearbeiten** auswählen.

Veranschaulichen Sie die Verwendung des GitHub Copilot-Statusmenüs für den Zugriff auf Einstellungen. Dadurch wird die Registerkarte „Visual Studio Code-Einstellungen“ mit Einstellungen geöffnet, die nach GitHub Copilot gefiltert sind. Die Verwendung des Statusmenüs stellt die schnellste Möglichkeit dar, auf die Einstellungen für die GitHub Copilot-Erweiterungen zuzugreifen.

### Konfigurieren von GitHub Copilot-Einstellungen

Führen Sie die folgenden Schritte aus, um die Konfigurationseinstellungen für GitHub Copilot anzuzeigen:

1. Wählen Sie im unteren Bereich des Visual Studio Code-Fensters das GitHub Copilot-Statusmenü und dann das GitHub Copilot-Statussymbol aus.

    Das GitHub Copilot-Statussymbol gibt an, ob GitHub Copilot aktiviert oder deaktiviert ist. Wenn das Tool aktiviert ist, ist die Hintergrundfarbe des Symbols mit der Farbe der Statusleiste identisch. Wenn es deaktiviert ist, kontrastiert die Hintergrundfarbe des Symbols die Farbe der Statusleiste.

1. Wählen Sie im GitHub Copilot-Statusmenü **Einstellungen bearbeiten** aus.

1. Nehmen Sie sich etwas Zeit, um die Liste der verfügbaren Einstellungen zu untersuchen.

    Beachten Sie, dass Einstellungen für GitHub Copilot und GitHub Copilot Chat aufgeführt sind. Außerdem werden beide Erweiterungen unter der Bezeichnung „Erweiterungen“ auf der linken Seite als Copilot bezeichnet. Die erste Copilot-Erweiterung steht für GitHub Copilot und die zweite für GitHub Copilot Chat.

1. Wählen Sie unter der Bezeichnung „Erweiterungen“ die erste Copilot-Erweiterung aus.

    Beachten Sie, dass die Einstellungsliste jetzt ausschließlich nach GitHub Copilot gefiltert ist.

    Folgende Einstellungen sind für GitHub Copilot verfügbar:

    - AutoVervollständigen aktivieren
    - Copilot-Vervollständigung für angegebene Sprachen aktivieren oder deaktivieren

1. Nehmen Sie sich etwas Zeit, um die Einstellungen für **Copilot-Vervollständigung für angegebene Sprachen aktivieren oder deaktivieren** zu untersuchen.

    Beachten Sie, dass die Einstellungen für diese Option anhand einer Liste von Sprachen und dem Wert **true** oder **false** konfiguriert werden, die es ermöglichen, GitHub Copilot für die einzelnen Sprache zu aktivieren oder zu deaktivieren. Standardmäßig ist GitHub Copilot für alle Sprachen aktiviert. Diese Einstellung wird mit dem Platzhalterzeichen `*` in der ersten Zeile und dem Wert **true** angegeben. Die nachfolgenden Zeilen geben Sprachen an, für die GitHub Copilot aktiviert oder deaktiviert ist. Im Beispiel ist GitHub Copilot für **C#**, **JavaScript** und **Python** aktiviert und für **Klartext** und **Markdown** deaktiviert.

1. Wählen Sie unter **Copilot-Vervollständigung für angegebene Sprachen aktivieren oder deaktivieren** die Option **Markdown** aus.

    Beachten Sie, dass der Wert für Markdown auf **false** festgelegt ist. Dies bedeutet, dass GitHub Copilot für Markdown-Dateien deaktiviert ist.

1. Um Copilot für Markdown-Dateien zu aktivieren, wählen Sie **Element bearbeiten** (Stiftsymbol) und anschließend **false** aus, ändern Sie den Wert in **true**, und wählen Sie dann **OK** aus.

    Sie können jetzt GitHub Copilot-Projekte für das Dokumentieren mit Markdown-Dateien verwenden.

1. Wählen Sie unter der Bezeichnung „Erweiterungen“ die zweite Copilot-Erweiterung aus.

    Beachten Sie, dass die Einstellungsliste jetzt ausschließlich nach GitHub Copilot Chat gefiltert ist.

    Die Einstellungen für GitHub Copilot Chat umfassen die Optionen **Vorschau** und **Experimentell**. Einstellungsoptionen umfassen die folgenden Optionen:

    - **Beheben von Testfehlern**: Diese Option ist standardmäßig aktiviert, sodass GitHub Copilot Vorschläge zum Beheben von Testfehlern bereitstellen kann.
    - **Nachfragen**: Diese Einstellung ist standardmäßig auf **FirstOnly** festgelegt, was bedeutet, dass GitHub Copilot erst nach dem ersten Vorschlag weitere Vorschläge bereitstellt. Die anderen Optionen sind **immer** und **nie**.
    - **Lokale Außerkraftsetzung**: Diese Option ist standardmäßig auf **automatisch** festgelegt. Dies bedeutet, dass GitHub Copilot das Gebietsschema der Visual Studio Code-Anzeigesprache verwendet.
    - **Bereichsauswahl**: Diese Option ist standardmäßig deaktiviert. Wenn diese Option aktiviert ist, erfolgt eine Aufforderung zur Eingabe eines Bereichssymbols, wenn `/explain` im Chat ohne eine Auswahl im Editor verwendet wird.
    - **Terminal-Chatstandort**: Die Standardeinstellung ist chatView, welche die Chatansicht festlegt. Die anderen Optionen sind für den Bereich Quick Chat und Terminal.
    - **Projektvorlagen verwenden**: Diese Option ist standardmäßig aktiviert, sodass GitHub Copilot relevante GitHub-Projektvorlagen verwendet, wenn im Chat `/new` verwendet wird.
    - **Codeaktionen aktivieren**: Diese Option ist standardmäßig aktiviert, damit GitHub Copilot Codeaktionen im Editor bereitstellen kann.
    - **Automatisch auslösen**: Diese Option ist standardmäßig aktiviert, sodass GitHub Copilot-Vorschläge während der Eingabe automatisch angezeigt werden.

    Es empfiehlt sich, während dieser Schulung die Standardeinstellungen beizubehalten. Dadurch stellen Sie sicher, dass bei der Arbeit an den Modulen in diesem Lernpfad die erwarteten Aktionen ausgeführt werden. Nach Abschluss der Schulung können Sie mit diesen Einstellungen experimentieren, um Ihre Erfahrung mit GitHub Copilot und Copilot Chat anzupassen.

## Konfigurieren von GitHub Copilot-Einstellungen auf GitHub.com

Ihre GitHub-Kontoeinstellungen auf GitHub.com umfassen auch Optionen zum Konfigurieren von GitHub Copilot. Diese Einstellungen dienen dazu, Ihr GitHub Copilot-Abonnement zu verwalten, die Aufbewahrung von Prompts und Vorschlägen zu konfigurieren und Vorschläge zuzulassen oder zu blockieren, die mit öffentlichem Code übereinstimmen.

GitHub Copilot kann über persönliche Konten bei GitHub Copilot Individual oder über Organisationskonten bei GitHub Copilot Business/Enterprise verwaltet werden.

## Tastenkombinationen für GitHub Copilot

Sie können für die Arbeit mit GitHub Copilot die Standardtastaturkombinationen in Visual Studio Code verwenden. Alternativ kannst du die Tastenkombinationen im Editor für Tastenkombinationen nach deinen Wünschen neu mit einzelnen Befehlen verknüpfen.
