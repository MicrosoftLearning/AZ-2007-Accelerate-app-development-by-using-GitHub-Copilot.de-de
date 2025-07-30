---
demo:
  title: 'Demo: Generieren einer Projektdokumentation mithilfe von GitHub Copilot Chat'
  module: 'Module 2: Generate documentation using GitHub Copilot tools'
---

# Demo: Generieren einer Projektdokumentation mithilfe von GitHub Copilot Chat

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

Die Erstellung von Dokumentationen ist ein wichtiger Bestandteil der Softwareentwicklung. Inlinedokumentation unterstützt Entwickler dabei, die Codebasis, ihren Zweck und ihre Verwendung zu verstehen. Die Projektdokumentation bietet Interessierten Informationen, die für das Verständnis des Umfangs und Zwecks des Projekts von wesentlicher Bedeutung sind.

Die Projektdokumentation enthält häufig die folgenden Abschnitte:

- **Projektüberblick**: Eine allgemeine Zusammenfassung des Projekts, seines Zwecks und seiner Ziele.
- **Anforderungen des Projekts** Eine Liste der Anforderungen des Projekts, einschließlich funktionaler und nicht funktionaler Anforderungen.
- **Projekteinschränkungen**: Alle Einschränkungen, die sich auf das Projekt auswirken, z. B. Zeit, Budget oder technische Einschränkungen.
- **Projektabhängigkeiten**: Eine Liste der Projektabhängigkeiten, einschließlich Bibliotheken, Frameworks und anderer Komponenten, auf denen das Projekt basiert.
- **Projektzusammenfassung**: Eine kurze Zusammenfassung des Projekts, seines Zwecks und seiner Ziele.

In dieser Demo verwenden Sie GitHub Copilot Chat, um eine Projektdokumentation für das `APL2007M2Sample1`-Projekt zu erstellen.

> [!IMPORTANT]
> Kursleitende sollten betonen, wie wichtig es ist, die von GitHub Copilot vorgeschlagene Dokumentation zu überprüfen. Entwickelnde müssen die Genauigkeit und Vollständigkeit überprüfen. Die von GitHub Copilot generierte Dokumentation ist ein Ausgangspunkt. Möglicherweise müssen Sie den Inhalt hinzufügen, entfernen oder ändern, um die spezifischen Anforderungen Ihres Projekts zu erfüllen.

### Generieren der Projektdokumentation für das APL2007M2Sample1-Projekt

Die Projektdokumentation kann in Visual Studio Code mithilfe der Chatansicht und des `@workspace`-Teilnehmers generiert werden. Sie können Beschreibungen in natürlicher Sprache einfügen, um bestimmte Abschnitte der Projektdokumentation zu generieren, z. B. die Projektübersicht, Anforderungen, Einschränkungen, Abhängigkeiten sowie die Zusammenfassung. Sie können auch GitHub Copilot Chat verwenden, um bestimmte Arten von Dokumentationsdateien zu generieren, z. B. eine `readme.md`-Datei.

1. Stellen Sie sicher, dass das `APL2007M2Sample1`-Projekt in Visual Studio Code geöffnet ist.

1. Wählen Sie **Chat öffnen** aus, um die Chatansicht zu öffnen.

1. Geben Sie in der Chatansicht zum Generieren der Dokumentation für den Arbeitsbereich die folgende Eingabeaufforderung ein:

    ```output
    @workspace document this project
    ```

1. Nehmen Sie sich eine Minute Zeit, um die für das `APL2007M2Sample1`-Projekt generierte Projektdokumentation zu überprüfen.

    Beachten Sie, dass die vorgeschlagene Projektdokumentation mit der in der vorherigen Einheit generierten Projekterklärung vergleichbar ist.

    Indem Sie Eingabeaufforderungen wie "Projekteinschränkungen dokumentieren" oder "Projektabhängigkeiten dokumentieren" anfügen, erhalten Sie detaillierte Informationen zum Projekt.

1. Geben Sie in der Chatansicht die Dokumentation zur Beschreibung der Projektabhängigkeiten ein:

    ```output
    @workspace document the project dependencies
    ```

1. Nehmen Sie sich eine Minute Zeit, um die Dokumentation zu Projektabhängigkeiten zu überprüfen.

    Die von Copilot Chat generierte Antwort sollte in etwa den folgenden Informationen entsprechen:

    GitHub Copilot Chat kann Ihnen dabei helfen, beliebige Aspekte Ihrer Projekte zu dokumentieren. Sie können die Chatansicht verwenden, um Dokumentationen für bestimmte Dateien, Klassen oder Funktionen innerhalb des Projekts zu generieren. Die Größe und Komplexität des Projekts helfen dabei, den erforderlichen Detailgrad zu bestimmen.

    Wenn die Zeit dies zulässt, verwenden Sie die Chatansicht, um Dokumentationen für die folgenden Projektabschnitte zu generieren:

    - Anforderungen des Projekts
    - Projekteinschränkungen
    - Projektarchitektur
    - Projektentwurf
    - Projekttests
    - Projektbereitstellung
    - Projektzusammenfassung

    Sie können die von Copilot Chat generierte Projektdokumentation an die spezifischen Anforderungen Ihres Projekts und der Projektbeteiligten anpassen.

1. Geben Sie in der Chatansicht zum Generieren einer README-Datei für das `APL2007M2Sample1`-Projekt die folgende Eingabeaufforderung ein:

    ```output
    @workspace generate a readme document that can be used as a repo description
    ```

1. Nehmen Sie sich eine Minute Zeit, um die für das `APL2007M2Sample1`-Projekt generierte README-Datei zu überprüfen.

    Der von Copilot Chat generierte README-Dateiinhalt bietet eine allgemeine Übersicht über das Projekt mit mehreren Abschnitten, die häufig in diesem Dateityp enthalten sind.

    Sie können den Prompt anpassen, um bestimmte Infodateiabschnitte anzugeben. Sie können auch einzelne Eingabeaufforderungen schreiben, um bestimmte Abschnitte eines README-Dokuments zu generieren.

    > [!NOTE]
    > Wenn das Infodateidokument als Markdowndatei formatiert werden soll, können Sie einen Prompt wie den folgenden eingeben: `generate readme project documentation formatted using a raw markdown format`. Wenn GitHub Copilot für die Verwendung von Markdowndateien konfiguriert ist, können Sie das Inlinechatfeature verwenden, um das Infodateidokument als Markdowndatei zu formatieren.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot Chat verwendet, um eine Projektdokumentation für das `APL2007M2Sample1`-Projekt zu erstellen. Mithilfe der Chatansicht und des `@workspace`-Teilnehmers konnten Sie Dokumentationen für die Projektübersicht, Anforderungen, Einschränkungen, Abhängigkeiten und Zusammenfassungen generieren. Sie haben auch eine README-Datei für das `APL2007M2Sample1`-Projekt generiert. Durch das Generieren einer Projektdokumentation mit Copilot Chat können Sie eine allgemeine Übersicht erstellen, die anderen Entwicklern hilft, das Projekt und seine Ziele zu verstehen. Denken Sie daran, die von Copilot Chat generierte Dokumentation zu überprüfen, um Genauigkeit und Vollständigkeit sicherzustellen.
