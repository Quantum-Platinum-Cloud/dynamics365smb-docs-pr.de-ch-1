---
title: Verwalten von Benutzern und Rollen
description: 'Erfahren Sie, wie Sie Benutzerprofile und Rollen in Business Central verwalten können. Profile erlauben es Administratoren, zentral zu definieren und zu verwalten, was Benutzer sehen und tun können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# <a name="manage-user-profiles" />Verwalten von Benutzerprofilen

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Weisen Sie allen Benutzern Profile zu, die Folgendes widerspiegeln:

* ihre geschäftliche Rolle
* die Abteilung, in der sie arbeiten
* einen weiteren Kategorisierungstyp

Mithilfe von Profilen können Administratoren zentral definieren und verwalten, welche unterschiedlichen Benutzertypen auf [!INCLUDE[prod_short](includes/prod_short.md)] zugreifen können.

> [!NOTE]
> Die typische geschäftliche Verwendung eines Profils ist eine Rolle. Ein Profil wird daher *Profil (Rolle)* benannt in der Benutzeroberfläche.

Als Administrator erstellen und verwalten Sie Profile auf der **Profile (Rollen)** Seite. Jedes Profil verfügt über eine Karte, auf der die Einstellungen für die zugehörige Rolle verwaltet werden. Die Karte enthält beispielsweise folgende Informationen:

* Name der Rolle
* Benutzereinstellungen
* Das vom Profil genutzte Rollencenter

Weitere Informationen zu Benutzereinstellungen und Rollencentern finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md).

Bevor Sie Benutzerprofile verwalten können, müssen Sie die Benutzer erstellen und über das Microsoft 365 Admin Center hinzufügen. Anschliessend können Sie jedem Benutzer oder jeder Benutzergruppe Berechtigungen zuweisen. Berechtigungen definieren die Funktionen, auf die Benutzer zugreifen können. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

## <a name="page-customization" />Seiten-Anpassung

Sie können die Seitenlayouts für ein Profil so anpassen, dass alle Benutzer, denen das Profil zugewiesen wurde, die angepassten Seiten sehen. Als Administrator passen Sie Seiten an, indem Sie dieselben Funktionen verwenden wie Benutzer, wenn sie Personalisierungen vornehmen. Weitere Informationen finden Sie unter [Gewusst wie: Seiten für Profile anpassen](ui-personalization-manage.md).

## <a name="to-create-a-profile" />So erstellen Sie ein Profil

Wenn Sie ein vorhandenes Profil nicht kopieren können, können Sie manuell ein neues Profil erstellen.

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Suche nach Seiten- oder Berichtssymbolen") Symbol. Geben Sie **Profile (Rollen)** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Profile (Rollen)** wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Wenn Sie möchten, dass ein bestimmtes Profil nur ganz bestimmten Benutzern zur Verfügung steht, können Sie das Feld **Beschreibung** auf `Navigation menu only.` festlegen. Auf diese Weise wird das Profil aus der Liste der verfügbaren Rollen in **Meine Einstellungen** ausgeschlossen.

## <a name="to-copy-a-profile" />So kopieren Sie ein Profil

Um Zeit zu sparen, können Sie ein neues Profil erstellen, indem Sie ein vorhandenes kopieren. Kopieren Sie eines mit ähnlichen Einstellungen wie das, das Sie erstellen möchten.

> [!NOTE]
> Wenn Sie ein Profil kopieren, werden auch alle beteiligten Seitenanpassungen kopiert, sowohl die vom Benutzer erstellten als auch die von Erweiterungen abgeleiteten.

1. Wählen Sie auf der Seite **Profile (Rollen)** die Zeile für das Profil aus, das Sie kopieren möchten, und wählen Sie dann die Aktion **Profil kopieren**.
2. Füllen Sie die **Profil ID** und **Anzeigename** Felder, und wählen Sie dann die Schaltfläche **OK**.
3. Auf der **Profile (Rollen)** Seite, öffnen Sie die neu erstellte Profilkarte und bearbeiten Sie die anderen Felder nach Bedarf.

## <a name="to-edit-a-profile" />So bearbeiten Sie ein Profil

Sie können ein Profil bearbeiten, indem Sie die Felder auf der Seite **Profil (Rolle)** ändern. Die Änderungen sind jedoch für den Benutzer, dem das Profil zugewiesen wurde, erst nach dem Abmelden und Wiedereintritt sichtbar.

> [!Caution]
> Benennen Sie ein Profil nicht um, während die Benutzer, denen das Profil zugewiesen wurde, angemeldet sind, da es bei Benutzern zu einem Einfrieren des Produkts kommen kann und ein Neustart erforderlich ist.

## <a name="to-assign-a-profile-to-a-user" />So ordnen Sie ein Profil einem Benutzer zu

Benutzer können sich selbst eine Rolle zuweisen (die ein Profil darstellt), indem Sie das Feld **Rolle** auf der Seite **Meine Einstellungen** auswählen. Als Administrator können Sie dasselbe über die Seite **Profile (Rollen)** tun.

1. Auf der Seite **Profile (Rollen)** wählen Sie die Zeile für das Profil, das Sie zuweisen möchten, und wählen die **Benutzer-Personalisierungsliste** Aktion aus.
2. Auf der Seite **Benutzerpersonalisierungen** wählen Sie den Benutzer, den Sie dem Profil zuweisen möchten und wählen Sie die Aktion **bearbeiten** aus.
3. In dem **Profil ID** Feld wählen Sie das entsprechende Profil aus.

> [!NOTE]
> Wenn Sie einem Benutzer ein anderes Profil zuweisen, bleiben alle vom Benutzer mit dem vorherigen Profil vorgenommenen Personalisierungen erhalten.

## <a name="to-define-user-settings-for-a-profile" />So definieren Sie Benutzereinstellungen für ein Profil

Auf der Seite **Meine Einstellungen** können Benutzer das grundlegende Verhalten ihres Kontos definieren, z. B. das Rollencenter, die Sprache und die Benachrichtigungen, die sie erhalten. Weitere Informationen finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md).

Als Administrator können Sie die Einstellungen für ein Profil definieren. Die Einstellungen gelten für alle Benutzer, die der Rolle zugewiesen sind.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Profile (Rollen)** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile für das Profil aus, für das Sie die Benutzereinstellungen ändern möchten, und wählen Sie Aktion **Benutzerpersonalisierungsliste**.
3. Auf der Seite **Benutzeranpassungen** öffnen Sie die Karte für den Benutzer, dessen Einstellungen Sie ändern möchten.
4. Füllen Sie auf der Seite **Benutzerpersonalisierungskarte** die Felder nach Bedarf aus.

## <a name="to-activate-a-profile" />So aktivieren Sie ein Profil

Wenn Sie ein Profil erstellen, können Sie definieren, ob, wo und wie das Profil und seine Informationen den Benutzern zur Verfügung gestellt werden.

Aktivieren Sie auf der Seite **Profile (Rollen)** die folgenden Kontrollkästchen:

* **aktiviert** um anzugeben, ob die zugehörige Rolle in der Liste angezeigt wird **Verfügbare Rollen** Seite für Benutzer zur Auswahl.  
* **Als Standardprofil verwenden** um das Profil anzugeben, das für Benutzer gilt, denen keine bestimmte Rolle zugewiesen wurde.
* **Deaktivieren Sie die Personalisierung** um anzugeben, ob Benutzer der entsprechenden Rolle ihren Arbeitsbereich personalisieren können.
* **Zeige im Rollen-Explorer**, um festzulegen, ob Aktionen für Geschäftsfunktionen, die im Profil enthalten sind, in der erweiterten Ansicht des Rollen-Explorers, einer Feature-Übersicht, angezeigt werden. Weitere Informationen finden Sie unter [Suchen von Seiten mit dem Rollen-Explorer](ui-role-explorer.md).

## <a name="to-export-profiles" />So exportieren Sie Profile

Sie können Profile aus [!INCLUDE[prod_short](includes/prod_short.md)] exportieren, z.B. um sie in einem anderen Mandanten wiederzuverwenden. Die Profile werden in eine .zip-Datei eportiert, die die .al-Dateien enthält. Sie können die .al-Dateien zum Entwickeln von Erweiterungen wiederverwenden. Weitere Informationen finden Sie unter [Client zum Erstellen von Profilen und Seitenanpassungen verwenden](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Wählen Sie auf der Seite **Profile (Rollen)** die Aktion **Profile exportieren**.

    Diese Aktion exportiert eine .zip-Datei, die .al-Dateien für alle Profile enthält.

## <a name="to-import-profiles" />So importieren Sie Profile

Sie können Profile importieren, die aus [!INCLUDE[prod_short](includes/prod_short.md)] exportiert wurden. Die Schritte sind mehr oder weniger das Gegenteil der Schritte zum Exportieren von Profilen. Weitere Informationen finden Sie unter [Profile exportieren](admin-users-profiles-roles.md#to-export-profiles).

1. Wählen Sie auf der Seite **Profile (Rollen)** die Aktion **Profile importieren**.
2. Folgen Sie den Schritten des Assistenten **Importprofile**.

    Wenn Sie nur ausgewählte Profile importieren möchten, verwenden Sie das Kontrollkästchen **Ausgewählt**, um anzugeben, welche importiert werden sollen.
3. Wählen Sie die Aktion **Ausgewählte importieren**.

    Diese Aktion importiert eine .zip-Datei, die die .al-Dateien der ausgewählten Profile enthält.

## <a name="to-delete-a-profile" />So löschen Sie ein Profil

Sie können ein Profil löschen, indem Sie auf die Schaltfläche **Löschen** klicken auf der **Profile (Rollen)** Seite. Es gelten jedoch folgende Einschränkungen:

* Sie können ein Profil, das einem Benutzer oder einer Benutzergruppe zugeordnet ist, nicht löschen.
*-* Sie können keine Profile löschen, die aus Erweiterungen stammen. Die Erweiterung muss zuerst deinstalliert werden.
*-* Sie können jeweils nur ein Profil löschen.

## <a name="to-delete-all-personalizations-made-by-a-user" />Löscht alle von einem Benutzer vorgenommenen Anpassungen.

Sie können alle Änderungen löschen, die ein Benutzer an Seiten vorgenommen hat. Das Löschen von Änderungen ist nützlich, wenn beispielsweise ein Mitarbeiter die Rolle gewechselt hat und sie nicht mehr benötigt. Durch das Löschen wird das Seitenlayout wieder auf das im Profil definierte Layout zurückgesetzt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Benutzeranpassungen** ein und wählen Sie dann den zugehörigen Link.

    Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise Personalisierungen vorgenommen haben.

2. Öffnen Sie die Karte für einen Benutzer, dessen Personalisierungen Sie löschen möchten.
3. Auf der **Benutzer-Personalisierungskarte** Seite, wählen Sie die **Personalisierte Seiten löschen** Aktion, und akzeptieren Sie dann die Meldung, die angezeigt wird.

Der Benutzer sieht die Änderungen das nächste Mal bei seiner Anmeldung.

Sie können auch alle Seitenanpassungen für ein Profil löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Anpassungen für ein Profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages" />So löschen Sie Personalisierungen für bestimmte Seiten

Sie können Personalisierungen löschen, die ein oder mehrere Benutzer an bestimmten Seiten vorgenommen haben. Das Löschen von Personalisierungen ist nützlich, wenn beispielsweise ein geänderter Geschäftsprozess dazu führt, dass eine Personalisierung nicht mehr verwendet werden kann. Durch das Löschen wird das Seitenlayout wieder auf das im Profil definierte Layout zurückgesetzt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Benutzerseitenpersonalisierungen** ein und wählen Sie dann den zugehörigen Link.

    Die Seite **Benutzerseiten-Personalisierungen** listet alle Seiten auf, die personalisiert wurden, und den Benutzer, zu dem sie gehören.

    > [!Note]
    > Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich war, die die Personalisierung unterschiedlich bearbeitete. Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite. Weitere Informationen finden Sie unter [Warum eine Seite für die Personalisierung gesperrt ist](ui-personalization-locked.md).

2. Wählen Sie dir Zeile für die Personalisierungsseite, die Sie löschen möchten, und wählen die Aktion **Löschen** aus.

Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.  

Sie können auch alle individuellen Seitenanpassungen für ein Profil löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Anpassungen für eine bestimmte Seite für ein Profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions" />Verwalten von Benutzersitzungen

Als Administrator von [!INCLUDE[prod_short](includes/prod_short.md)] Online können Sie Benutzersitzungen im Administration Center verwalten. Weitere Informationen finden Sie unter [Sitzungen verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions) im Verwaltungsinhalt.  

Für [!INCLUDE[prod_short](includes/prod_short.md)] (lokal) können Sie Sitzungen beispielsweise mit SQL Server Management Studio verwalten. Weitere Informationen finden Sie unter [Technische Dokumentation zu SQL Server](/sql/sql-server).  

## <a name="see-related-microsoft-trainingtrainingmodulesusers-security-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/users-security-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
