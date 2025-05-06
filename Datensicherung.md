# Datensicherung (Backup) bezeichnet das Kopieren und Archivieren von Daten, um sie bei Datenverlust – z. B. durch Hardwarefehler, versehentliches Löschen, Malware oder Systemabstürze – wiederherstellen zu können.

Es gibt verschiedene Arten von Backups:

Vollbackup: Alle Daten werden komplett gesichert.

Inkrementelles Backup: Nur die seit dem letzten Backup geänderten Daten werden gesichert.

Differenzielles Backup: Es werden alle Änderungen seit dem letzten Vollbackup gesichert.

Backups können lokal (z. B. auf externen Festplatten) oder extern (z. B. in der Cloud oder auf Servern) gespeichert werden. Eine gute Datensicherungsstrategie folgt der 3-2-1-Regel:

3 Kopien der Daten, auf 2 verschiedenen Speichermedien, davon 1 an einem externen Ort.

# Datensicherung mit SQL

In der Arbeit mit Datenbanken ist eine zuverlässige Datensicherung (Backup) unerlässlich, um Datenverluste durch Systemfehler, Benutzereingaben oder Hardwareprobleme zu vermeiden. Besonders bei produktiven Datenbanken sorgt ein durchdachtes Backup-Konzept für Sicherheit und Wiederherstellbarkeit.

Backup mit SQL (Beispiel: MySQL)
In MySQL erfolgt die Datensicherung meist über das Tool mysqldump, welches eine komplette Datenbank in Form von SQL-Befehlen exportiert:

bash
Kopieren
Bearbeiten
mysqldump -u [benutzername] -p [datenbankname] > backup.sql
Dieser Befehl exportiert die gesamte Datenbank inklusive Tabellenstruktur und Inhalte in eine .sql-Datei. Diese kann später mit folgendem Befehl wiederhergestellt werden:

bash
Kopieren
Bearbeiten
mysql -u [benutzername] -p [datenbankname] < backup.sql

Backup-Arten
- Vollbackup: Die gesamte Datenbank wird gesichert.

- Teilbackup: Nur bestimmte Tabellen oder Inhalte werden gesichert.

- Automatisierte Backups können per Skript oder Zeitplan (z. B. über den Windows-Taskplaner oder cron unter Linux) regelmäßig durchgeführt werden.

Best Practices
- Backups regelmäßig testen (Wiederherstellung prüfen!)

- Backups versionieren und mit Zeitstempel speichern

- Mindestens ein Backup an einem externen Ort aufbewahren (Cloud, externer Server)

- Automatisierungen nutzen, um manuelle Fehler zu vermeiden
