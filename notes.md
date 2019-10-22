Zabbix unter windows verzögert starten
36,     Hostname: Case sensitive
        Visible Name: Obvious
        Groups: Min 1 Gruppe wegen permissions
        Agent Interface: Schnittstelle von Zabbix, es gehen multiple (z.b. ipmi & linux)
        SNMP: Multiple allowed, Bulk request könnte problematisch werden wegen doofen standards
        JMX: Javakrams, tomcat und co.
        IPMI: Usernames, readonly important!

        MACROS: G_ -> Global
                T_ -> Template (D'uh)

    Tipp für Hosts: Linux hat keinen DNS Cache! DNS am Arsch -> Monitoring am Arsch.
                    Lokaler DNS kann helfen.

41,     ZBX: NUR Passive agent
        SNMP: NUR Pull
        JMX: Wenn avail
        IPMI: Wenn login erfolgreich

Custom Intervals bei werten, die korrelieren müssen!

Storage Perdiods in Marcos!
History -> Roh
Trends: Graphen und so
Valuemap
50, Quotes bei Items Keys


__Prüfungsrelevant:__
14, linke und mittlere spalte
24, PHP Time Zone muss gesetzt werden
27, JSON
33, definitionen
34, trigger -> event -> action

Agent: 10050 (TCP)
Server/Proxy: 10051 (TCP)
-> IANA Ports Offiziell
Zabbix Java Gateway: 10052
-> NICHT Offziell

42, Grau wenn disabled, etc
50, grundsyntaxaufbau: `key[parameter1, parameter2, <parameter3>]`
<> = Optional
55, not supported as agent active check
56, not supported as agent active check
60, item preproccessing types:
    Right/Left trim
    Regular expression (PCRE) XML and JSON Path
    Calculated as value * multiplier Use 0.125 to divide by 8
    Delta (simple change): (value-prevvalue)
    Delta (speed per second): (value-prevvalue)/(time-prevtime) Decimal, octal, hex, boolean
62, tabelle
67, verstehen (D'uh); Proxy ist 10051.
68
74, severities wissen können
    1 Not classified
    2 Information
    3 Warning
    4 Average 
    5 High
    6 Disaster
76, syntax von triggern
    Syntax: {host:key.function(param)}=0
            {zabbix:system.cpu.load.min(5m)}>10
            punkt vor strich, klammern zu erst, von innen nach außen
88, Items immer not supported, Triggers immer not known! NICHT umgekehrt!
90, Marcos. (A-Z, 0-9, _ , . )
    Systemmacros - kein Prefix
    Usermacros - $
    Lowlevel Discovery Macros - #

    Globale Ebene
    <Userebene
    <Templateebene
    <Theoretisch auch Host, ist aber doof


**Day 2:**

6, Templates are assigned to hosts directly (__not__ to a host group), Multiple templates can be linked to single host
9, Clone/Full Clone
21, Functions: grpavg, grpmax, grpmin, grpsum




