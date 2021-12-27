# Technologie-Radar

## Kontext

Der Technologie-Radar ist ein passendes Werkzeug für Technologie-Management in einem Unternehmen, für ein Produkte-Team oder auch für sich als Software Architekt oder Software Engineer. Es gibt bereits verschiedene Umsetzungen von Technologie-Radare. Das prominenteste Beispiel ist der [Technology Radar](https://www.thoughtworks.com/de-de/radar) von ThoughtWorks.

Dabei werden die einzelnen Technologien jeweils in sogn. vier Quadranten eingeordnet (Kategorien wie z.B. *Techniques*, *Tools*, *Platforms*, *Languages & Frameworks*). Die Maturität wird über sogn. Ringe eingestuft (*Assess*, *Trial*, *Adopt*, *Hold*).

Als Software-Anbieter möchten Sie den Technologie-Radar als Software as a Service anbieten. Der Technologie-Radar besteht aus zwei elementaren Teilen:

* einer Technologie-Radar-Administration, in welcher die Technologien vom *CTO* oder einm *Tech-Lead* verwaltet werden können
* einem Technologie-Radar-Viewer, auf welcher der Technologie-Radar resp. die Technologien allen Mitarbeiter eingesehen werden können.
* einer System-Administration, in welche neue Unternehmen resp. Mandanten erfasst und Personen eingeladen werden können (optional; nicht Teil der Aufgabenstellung)

Sie werden als Software-Architekt und Software Engineer damit beauftragt die folgenden Anforderungen umzusetzen.

## Anforderungen

### User Story 1: Anmelden Technologie-Radar-Administration (Could)

Als CTO oder Tech-Lead kann ich mich an der Technologie-Radar-Administration anmelden, damit ich Technologien im Technologie-Radar verwalten kann.

**Akzeptanzkriterien**

* Mittels korrektem Benutzername (E-Mail Adresse) und korrektem Passwort gelange ich zur Technologie-Radar-Administration.
* Mit nicht korrekte Benutzerdaten (Benutzername / Passworter) kann ich mich nicht anmelden.
* Nur Personen mit der Rolle CTO oder Tech-Lead dürfen sich in der Administration anmelden.

### User Story 2: Technologie erfassen (Must)

Als CTO kann ich eine neue Technologie erfassen, damit ich diese anschliessend publizieren kann.

**Akzeptanzkriterien**

* Für die Erfassung einer neuen Technologie muss ich folgende Felder angeben können:
    * Name (Muss-Feld)
        * z.B. *ArgoCD*
    * Kategorie (Muss-Feld)
        * z.B. *Tools*
    * Ring (Optionales-Feld)
        * z.B. *Trial*
    * Beschreibung Technologie (Muss-Feld)
        * z.B. *Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.*
    * Beschreibung der Einordnung (Optionales-Feld)
        * z.B. *Without making a judgment of the GitOps technique, we'd like to talk about Argo CD within the scope of deploying and monitoring applications in Kubernetes environments. Based on its ability to automate the deployment of the desired application state in the specified target environments in Kubernetes and our good experience with troubleshooting failed deployments, verifying logs and monitoring deployment status, we recommend you give Argo CD a try. You can even see graphically what is going on in the cluster, how a change is propagated and how pods are created and destroyed in real time.*    
* Sofern ein Muss-Feld nicht abgefüllt ist, darf die Technologie nicht abgespeichert werden.
* Neben der den Eingaben müssen folgende Felder Informationen hinterlegt werden, bei der Erfassung einer neuen Technologie
    * Informationen zum Erfasser (Link auf Person)
    * Erfassungsdatum

### User Story 3: Technologie publizieren (Should)

Als CTO kann ich erfasste, aber noch nicht publizierte, Technologien publizieren, damit diese auf dem Technologie-Radar erscheinen und entsprechned für Mitarbeiter einsehbar werden.

**Akzeptanzkriterien**

* Erfasste, aber noch nicht publizierte Technologien werden speziell gekennzeichnet.
* Mit Klick auf *Publizieren* können neue Technologien publiziert werden. Bei der Publizierung müssen aber folgende Eingaben gemacht werden:
       * Einordnung / Ring (Muss-Feld)
        * z.B. *Trial*
        * Wenn bereits ein Ring hinterlegt ist, wird dieser als Standardwert abgefüllt
       * Beschreibung der Einordnung (Muss-Feld)
        * z.B. *Without making a judgment of the GitOps technique, we'd like to talk about Argo CD within the scope of deploying and monitoring applications in Kubernetes environments. Based on its ability to automate the deployment of the desired application state in the specified target environments in Kubernetes and our good experience with troubleshooting failed deployments, verifying logs and monitoring deployment status, we recommend you give Argo CD a try. You can even see graphically what is going on in the cluster, how a change is propagated and how pods are created and destroyed in real time.*
* Bei der Publikation wird das Publikationsdatum entsprechend hinterlegt.

### User Story 4: Technologie ändern (Should)

Als CTO kann ich erfasste Technologien ändern, um z.B. fehlerhafte Daten oder nicht mehr passende Informationen zu ändern.

**Akzeptanzkriterien**

* Folgende Felder können geändert werden:
    * Name (Muss-Feld)
    * Kategorie (Muss-Feld)
    * Beschreibung Technologie (Muss-Feld)
* Mit dem Speichern wird das Änderungsdatum der Technologie sowie die Person geführt.

### User Story 5: Technologie-Einordnung ändern (Should)

Als CTO möchte ich die Einordnung von einer Technologie ändern, um die Relevanz der Technologie für das Unternehmen anders einstufen zu können.

**Akzeptanzkriterien**

* Mit Klick auf "Einordnung ändern", können folgednde Felder einer Technologie geändert werden:
    * Einordnung / Ring (Muss-Feld)
        * z.B. *Adopt*
    * Beschreibung der neuen Einordnung (Muss-Feld)
* Die History der einzelnen Einordnungsänderungen werden beibehalten.
* Mit dem Speichern wird das Änderungsdatum der Technologie sowie die Person geführt.


### User Story 6: Anmelden am Technologie-Radar-Viewer (Could)

Als Mitarbeiter kann ich mich am Technologie-Radar-Viewer anmelden, damit ich die Technologien resp. der Technologie-Radar des Unternehmens einsehen kann.

**Akzeptanzkriterien**

* Mittels korrektem Benutzername (E-Mail Adresse) und korrektem Passwort gelange ich zur Technologie-Radar-Administration.
* Mit nicht korrekte Benutzerdaten (Benutzername / Passworter) kann ich mich nicht anmelden.

### User Story 7: Technologien anzeigen (Must)

Als Mitarbeiter kann ich im Technologie-Radar-Viewer die Technologien resp. der Technologie-Radar einsehen.

**Akzeptanzkriterien**

* Es werden nur publizierte Technologien angezeigt.
* Technologien werden nach ihren Kategorien (*Techniques*, *Platforms*, *Tools*, *Languages & Frameworks*) strukturiert.
* Technologien werden nach ihrer Maturität (*Assess*, *Trial*, *Adopt*, *Hold*) strukturiert.

**Bemerkung**: Die Technologien müssen nicht als *Radar* abgebildet werden, sondern können auch tabellarisch dargestellt werden.