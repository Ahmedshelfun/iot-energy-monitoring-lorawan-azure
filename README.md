# IoT Energy Monitoring with LoRaWAN and Microsoft Azure

**Team internship project (2023) | Savonia University of Applied Sciences / Kuopion Energia collaboration**

An IoT energy-monitoring learning project involving **Carlo Gavazzi EM24** energy measurements, **LoRaWAN / ThingPark** connectivity, and **Microsoft Azure IoT Central** visualization. The original internship report documents the architecture, equipment, Azure Functions exploration and screenshots of the monitoring interfaces.

> **Project status:** Educational prototype / internship work. The report documents hardware readings and dashboard screenshots, but does not independently verify an end-to-end production deployment. An early VEGA-SH integration option encountered compatibility challenges.

## Architecture (project goal)

```text
Carlo Gavazzi EM24 energy meter
        |
  Meter data / Modbus interface
        |
 LoRaWAN integration and gateway
        |
 ThingPark network platform
        |
 Azure cloud integration
        |
 Azure IoT Central dashboard
```

The report describes this intended data path. Some integration steps were exploratory; screenshots alone should not be taken as proof of continuous live telemetry through every stage.

## Technologies

- Carlo Gavazzi EM24 / EM24 AV5 energy meter
- Energy readings: voltage, current, power and accumulated energy (kWh)
- LoRaWAN and ThingPark
- Microsoft Azure IoT Central dashboards
- Azure Functions (C# HTTP-trigger prototype)
- IoT device integration and troubleshooting

## Project contributions

**Ahmed Shelfun — Lead practical implementation**

I carried out the practical technical work on the energy monitoring setup. I had already taken a course using the same equipment, which helped me work with the hardware. I created the Azure application and built the dashboard for visualizing the energy data. I also worked on the system integration and troubleshooting.

**Philip Konadu Agyemang — Technical coordination and communication**

Philip supported the project by communicating with ThingPark specialists about the LoRaWAN data transmission and helping coordinate technical discussions.

This division of work is based on the team members' account. The project demonstrates collaboration between hands-on implementation and communication with specialists.

## Evidence from the internship report

The 2023 report includes screenshots of:
- Azure IoT Central energy monitoring dashboards
- Carlo Gavazzi EM24 readings for current, voltage, power and energy
- ThingPark device and connectivity monitoring

The original report also includes example Azure Function code. It is a generic HTTP-trigger demonstration rather than a complete energy-payload processing implementation; it has therefore **not** been presented here as a working production integration.

## Reproducing or extending the project

1. Configure an appropriate EM24 meter and compatible interface, following the equipment manuals and electrical safety requirements.
2. Verify the LoRaWAN gateway, supported integration hardware and ThingPark configuration.
3. Configure Azure connectivity and a telemetry schema.
4. Create an Azure IoT Central application and dashboard for validated measurements.
5. Test the full data path and record sample payloads and results.

These are reproduction guidelines, **not** a claim that all steps have been re-tested from this repository.

## Security and documentation

The original internship report contains a cloud storage credential in a configuration example. **It is intentionally excluded from this public repository.** Any still-active credential must be rotated/revoked. Do not commit `local.settings.json`, connection strings, API keys or device secrets.

A sanitized project summary is provided in this repository instead of the original PDF. The report is jointly authored and is not published here without reviewing all collaborators' and organizations' sharing permissions.

## Future improvements

- Add approved, redacted screenshots and hardware photos
- Publish reproducible, secret-free configuration examples
- Implement and test an energy telemetry ingestion function
- Validate measurements against meter readings
- Document troubleshooting and results

**Project team:** Ahmed Shelfun and Philip Konadu Agyem
