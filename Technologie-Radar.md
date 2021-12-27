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

### User Story 1: Anmelden Technologie-Radar-Administration

Als CTO kann ich mich an der Technologie-Radar-Administration anmelden, damit ich Technologien im Technologie-Radar verwalten kann.

**Akzeptanzkritieren**

* Mittels korrektem Benutzername (E-Mail Adresse) und korrektem Passwort gelange ich zur Technologie-Radar-Administration.
* Mit nicht korrekte Benutzerdaten (Benutzername / Passworter) kann ich mich nicht anmelden.

### User Story 2: Technologie erfassen

Als CTO kann ich eine neue Technologie erfassen, damit ich diese anschliessend publizieren kann.

**Akzeptanzkritieren**

* Für die Erfassung einer neuen Technologie muss ich folgende Felder angeben können:
    * Name (Muss-Feld)
        * z.B. *ArgoCD*
    * Kategorie (Muss-Feld)
        * z.B. *Tools*
    * Ring (Muss-Feld)
        * z.B. *Trial*
    * Beschreibung Technologie (Muss-Feld)
        * z.B. *Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.*
    * Beschreibung Einordnung (Muss-Feld)
        * z.B. *Without making a judgment of the GitOps technique, we'd like to talk about Argo CD within the scope of deploying and monitoring applications in Kubernetes environments. Based on its ability to automate the deployment of the desired application state in the specified target environments in Kubernetes and our good experience with troubleshooting failed deployments, verifying logs and monitoring deployment status, we recommend you give Argo CD a try. You can even see graphically what is going on in the cluster, how a change is propagated and how pods are created and destroyed in real time.*
* Sofern ein Muss-Feld nicht abgefüllt ist, darf die Technologie nicht abgespeichert werden.
* Neben der den Eingaben müssen folgende Felder Informationen hinterlegt werden, bei der Erfassung einer neuen Technologie
    * Informationen zum Erfasser (Link auf Person)
    * Erfassungsdatum