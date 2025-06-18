# Auftrag 3.1: Grundlagen Container-Technologie

## Antworten auf die Fragen:

1. **Was ist Container-Technologie oder Container-Virtualisierung?**  
   Container-Technologie ist eine Methode, um Anwendungen und ihre Abhängigkeiten in isolierten Umgebungen zu betreiben. Diese Umgebungen teilen sich den Kernel des Betriebssystems, sind aber voneinander getrennt. Container sind leichtgewichtig und starten schneller als virtuelle Maschinen (VMs).

2. **Was sind die Vor- und Nachteile der Container-Technologie zu virtuellen Servern (VM)?**  
   **Vorteile:**  
   - Container sind schneller und benötigen weniger Speicherplatz.  
   - Sie sind einfacher zu verschieben (portabel).  
   - Effizienter, da sie den Kernel des Host-Betriebssystems nutzen.  

   **Nachteile:**  
   - Container sind weniger isoliert als VMs, was Sicherheitsrisiken erhöhen kann.  
   - Sie sind stark vom Host-Betriebssystem abhängig.

3. **Welche Produkte kennen Sie im Zusammenhang mit virtuellen Servern und Container?**  
   - Virtuelle Server: VMware, Hyper-V, VirtualBox.  
   - Container: Docker, Kubernetes, Podman.

4. **Wie unterscheiden sich die Technologien VM und Container in Bezug auf Bereitstellung, Speicherplatz, Portabilität, Effizienz und Betriebssystem (Kernel)?**  
   - **Bereitstellung:** Container starten schneller, VMs brauchen mehr Zeit.  
   - **Speicherplatz:** Container sind kleiner, VMs benötigen mehr Speicherplatz.  
   - **Portabilität:** Container sind einfacher zu verschieben.  
   - **Effizienz:** Container teilen sich Ressourcen besser, VMs sind schwerfälliger.  
   - **Betriebssystem:** Container nutzen den Kernel des Hosts, VMs haben ihr eigenes Betriebssystem.

5. **Können virtuelle Server immer durch Container ersetzt werden?**  
   Nein, Container sind nicht für alle Szenarien geeignet. Wenn eine vollständige Isolation oder ein anderes Betriebssystem benötigt wird, sind VMs besser.

6. **Was ist der Unterschied zwischen Self-Managed und Fully Managed?**  
   - **Self-Managed:** Du bist selbst für die Verwaltung und Wartung der Infrastruktur verantwortlich.  
   - **Fully Managed:** Der Anbieter übernimmt die Verwaltung, und du kannst dich auf die Nutzung konzentrieren.