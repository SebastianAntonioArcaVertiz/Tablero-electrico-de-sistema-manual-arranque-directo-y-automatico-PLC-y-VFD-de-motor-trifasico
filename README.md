

Este repositorio contiene la documentación técnica, los esquemas eléctricos y el código fuente para el diseño e implementación de un tablero de accionamiento para un motor asíncrono trifásico (0.5 HP). El sistema está diseñado para entornos exigentes, alojado en un gabinete con grado de protección IP67 e IK10, y cuenta con dos regímenes de operación protegidos por un enclavamiento estricto:



**\***   **Modo Manual:** Arranque directo a la red mediante control electromecánico (contactor AC-3 y relé térmico Clase 10).

**\***   **Modo Automático:** Control de transición de tres velocidades fijas, gobernado por un Controlador Lógico Programable (PLC) interactuando con un Variador de Frecuencia (VDF).



**Este proyecto fue desarrollado como parte del proyecto final del curso de ELECTRICIDAD INDUSTRIAL, de la escuela de Ingeniería Electrónica y Telecomunicaciones de la Universidad Nacional de Piura (UNP).**



**\***   **Controlador (PLC):** Schneider Zelio programado en lenguaje Ladder.

**\***   **Accionamiento (VDF):** SUSWE de 0.75 kW (1 HP), configurado para rampas suaves de 5 segundos.

**\***   **Normativa Eléctrica:** Dimensionamiento de conductores (14 AWG y 16 AWG) y protecciones selectivas con disyuntores de Curva C según el Código Nacional de Electricidad (CNE-Utilización) y la NTP 370.301 / IEC 60364-5-523.

**\***   **Normativa de seguridad:** Se cumple con los entándares de la ley 29783 y la gestion de seguridad y salud en el trabajo, se adjunta los documentos IPERC y ATS de prueba que se utilizaron y se entregaron en el proyecto.

**\***   **Simbología:** Estándar IEC 60617.



El repositorio consta de videos de demostración de cómo funciona el sistema, planos en AutoCAD y pdf, un informe que detalla la elección de componentes, normas utilizadas y evidencias de fabricación, y la documentación de seguridad que se siguió para el desarrollo del proyecto.



El algoritmo del PLC fue diseñado mediante el uso de marcas de memoria para permitir la transición directa entre velocidades sin necesidad de accionar un paro intermedio. La gestión binaria de salidas hacia el variador se estructura de la siguiente manera:



**\***   **Velocidad 1 (10 Hz):** Activa `Q1` energizando el borne `X0` (Señal maestra de giro).

**\***   **Velocidad 2 (20 Hz)**: Activa `Q1` y `Q2` energizando los bornes `X0` y `X2`.

**\***   **Velocidad 3 (30 Hz):** Activa `Q1`, `Q2` y `Q3` energizando los bornes `X0`, `X2` y `X3`.





