# hello-world

1.a) 	-Luft ist schlechtes Übertragungsmedium
	-Paketverluste
	-Abschirmung (Stahlbeton o.ä.)
	-Überlastung
b)	-Übertragungsrate
	-Ping
	-Pakteverlustrate
c)	-Das Codemultiplexverfahren (Code Division Multiplex, CDM oder Code Division Multiple Access,
	 CDMA) ist ein Multiplexverfahren, das die gleichzeitige Übertragung verschiedener 
	 Nutzdatenströme auf einem gemeinsamen Frequenzbereich ermöglicht.
		-jeder Datenstrom bekommt eigenen Spreizcode
		-mehr Nutzer - weniger Datenrate
	-Collision Detect Multiple Access
		-geläufiger mit Carrier Sense Multiple Access/Collision Detection (CSMA/CD) 
		bezeichnet, ein Zugriffsverfahren für Multi-Master-Systeme, wie es zum 
		Beispiel vom Ethernet verwendet wird
2.a)	-802.11b
		2.4-2.5 Ghz
		bis 11Mb/s
		Modulation: Direct Sequence spread Spectrum (DSSS) (Frequenzspreizverfahren)
			Alle Engeräte haben gleichen Chipping Code (Bits werden in Chips aufgeteilt. CC = Bitfolge)
	-802.11a
		5-6 Ghz
		bis 54 Mb/s
	-802.11g
		2.4-5 Ghz
		bis 54 Mb/s
	-alle drei nutzen CSMA/CA zum Medienzugriff (Mehrfachzugriff mit Trägerprüfung und Kollisionsvermeidung)
	1 Zuerst wird das Medium abgehört („horcht“, „Carrier Sense“).
	2 Ist das Medium für die Dauer eines DIFS frei, wird eine Backoffzeit aus dem Contention Window ausgewürfelt und nach Ablauf dieser gesendet.
	3 Ist das Medium belegt, wird der Backoff bis zum Ablauf des Network Allocation Vectors (NAV) gestoppt, bevor er nach einem weiteren DIFS entsprechend weiter läuft.
	4 Nach vollständigem Empfang des Paketes wartet der Empfänger ein SIFS, bevor das ACK gesendet wird.
	5 Eine Kollision durch gleichzeitigen Ablauf des Backoffs führt zu einem ACK-Timeout – nach welchem ein EIFS gewartet wird bevor sich der gesamte Vorgang wiederholen kann ( DIFS → BO .. ).
	-alle drei unterstützen Ad-Hoc und Infrastruktur (Router)  Modus

	-802.11n
		Datenraten bis 600 Mbit/s
		MRC,STBC und SDM
		Channel Bonding
		Frame Aggregation
b)	-802.11ac
		Spatial Division Multiplexing (SDM) 8 parallele Streams (Übertragen mehrerer Nachrichten über parallele Übertragungswege)
		Erster Standard mti Multi User MIMO
		(Multiple Input und Multiple Output)
			Access Point kann gleichzeitig Daten an mehrere Clients verschicken
			parallel und auf selber Frequenz	
			bis 4 Clients
		Datenraten bis 6.93 Gbit/s
		nur 5Ghz-Band
		
c)	-weniger Overhead
	-kombiniert Pakete der höheren Schichten zu einem MAC Frame
	-Effizientere Nutzung des drahtlosen Mediums
	-RTS/CTS Overhead nur einmal pro Frame
	-Backoff nur einmal pro Frame
d)	-Überlappung
	-Channel Bonding
	-nur unter geeigneten Bedingungen Durchsatzsteigerung möglich
	-Paketverluste

3.a)	-Medium Access Control
	-Multiplexing
b)	-Knoten B kann sowohl mit A als auch C kommunizieren
	-A und C können sich gegenseitig nicht hören
	-Wenn A zu B sendet kann C die Übertragung mit Hilfe des carrier sense
	Mechanismus nicht erkennen
	-Falls C sendet kommt es zur Kollision bei Knoten B
c)	-die Geräte müssen gleichzeitig senden und empfangen können
	-Mobile Endgeräte wechseln häufig den "Server/Router"
	-->Handover benötigt
	Ungünstigster Fall: Sender_1 und Sender_2 befinden sich an den äußersten Enden eines maximal langen Mediums, Sender_2 beginnt zu senden, als ihn das Signal von Sender_1 fast erreicht hat.
d)	-Funktionsweise CSMA/CA (Carrier Sense Multiple Access / Collision Acoidance)
		1 Zuerst wird das Medium abgehört („horcht“, „Carrier Sense“).
		2 Ist das Medium für die Dauer eines DIFS(Zeit, die vor dem Senden eines regulären Datenframes vergangen sein muss) frei, wird eine Backoffzeit aus dem Contention Window ausgewürfelt und nach Ablauf dieser gesendet.
		3 Ist das Medium belegt, wird der Backoff bis zum Ablauf des Network Allocation Vectors (NAV) gestoppt, bevor er nach einem weiteren DIFS entsprechend weiter läuft.
		4 Nach vollständigem Empfang des Paketes wartet der Empfänger ein SIFS (Zeit, die vor dem Senden eines Bestätigungsframes, Clear to Send), bevor das ACK gesendet wird.
		5 Eine Kollision durch gleichzeitigen Ablauf des Backoffs führt zu einem ACK-Timeout – nach welchem ein EIFS(Zeit, die vor dem Senden nach einer erkannten Kollision vergangen sein muss) gewartet wird bevor sich der gesamte Vorgang wiederholen kann ( DIFS → BO .. ).
e)	-Stauauflösungsmechanismus im Ethernet
	-wird Kollision erkannt, beenden diese Stationen ihre Sendung und versuchen sofort ODER nach einer Slot-Time erneut ihre Sendung über das Ethernet zu übertragen.
	-Dabei kann es erneut zu einer Kollision kommen, wenn beide Stationen zufällig die gleiche Wahl treffen.
	-Beim nächsten Versuch wird nun jede der beiden Stationen wieder per Zufallsentscheidung einen neuen Starttermin auswählen, diesmal aber aus vier Möglichkeiten
	-geht immer weiter bis 1024
	-Nach insgesamt 16 erfolglosen Übertragungsversuchen mit Kollision wird mit einer Fehlermeldung des Ethernet-Controllers abgebrochen.

	
