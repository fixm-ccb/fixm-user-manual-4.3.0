# FIXM Encoding Guidance - `fx:Flight`

This section describes general encoding guidance for FIXM Core's `fx:Flight` package that is always applicable, whatever the implementation context. 
Click on the packages, classes, or properties below to open the corresponding encoding guidance. 
Alternatively, you can use the Search box in the side bar to find relevant user manual entries.

*Note: links are provided below only when encoding guidance is available. The FIXM User Manual is being gradually enriched to provide guidance for all FIXM Core content.*

---
Package [`fx:Aircraft`]
- **Aircraft:** [aircraftAddress], [aircraftApproachCategory], [aircraftType], [capabilities], [coloursAndMarkings], [registration], [wakeTurbulence]
- **AircraftType:** [aircraftCount], [icaoAircraftTypeDesignator], [otherAircraftType]
---
Package [`fx:Arrival`]
- **Arrival:** [actualTimeOfArrival], [airportSlotIdentification], [arrivalAerodrome], [destinationAerodrome], [destinationAerodromeAlternate], [destinationAerodromePrevious], reclearanceInFlight, runwayDirection
---
Package [`fx:Capability`]
- **Capability:** [communication], [navigation], [standardCapabilities], [surveillance], [survival]
- **CommunicationCapabilities:** [communicationCapabilityCode], [datalinkCommunicationCapabilityCode], [otherCommunicationCapabilities], [otherDatalinkCapabilities], [selectiveCallingCode]
- **NavigationCapabilities:** [navigationCapabilityCode], [otherNavigationCapabilities], [performanceBasedCode], [requiredRunwayVisualRange]
- **SurveillanceCapabilities:** [otherSurveillanceCapabilities], [surveillanceCapabilityCode]
- **SurvivalCapabilities:** [carriedEltHexIdentifier], [dinghyInformation], [emergencyRadioCapabilityType], [lifeJacketType], [survivalEquipmentRemarks], [survivalEquipmentType]
---
Package [`fx:Cargo`]
- **DangerousGoods:** aircraftLimitation, airWaybillNumber, onboardLocation, packageGroup, shippingInformation
<!-- - **fx:DangerousGoodsPackageGroup:** dangerousGoodsPackage, shipmentDimensions -->
<!-- - **fx:DangerousGoodsPackage:** allPackedInOne, compatibilityGroup, dangerousGoodsLimitation, dangerousGoodsQuantity, hazardClass, packingGroup, properShippingName, radioactiveMaterials, shipmentDimensions, subsidiaryHazardClass, unNumber -->
---
Package [`fx:Departure`]
- **Departure:** [actualTimeOfDeparture], [airfileIndicator], [airportSlotIdentification], [departureAerodrome], [departureAerodromePrevious], [departurePoint], [departurePointPrevious], [estimatedOffBlockTime], [estimatedOffBlockTimePrevious], [estimatedRouteStartTime], [estimatedRouteStartTimePrevious], runwayDirection, [takeoffAlternateAerodrome]
---
Package [`fx:Emergency`]
- **FlightEmergency:** actionTaken, emergencyDescription, lastContact, originator, otherInformation, phase
<!-- - **fx:LastContactType:** lastContactFrequency, lastContactTime, lastContactUnit, position -->
- **RadioCommunicationFailure:** contact, radioFailureRemarks, remainingComCapability
---
Package [`fx:EnRoute`]
- **EnRoute:** [alternateAerodrome], boundaryCrossingCoordination, [currentModeACode]
- **BoundaryCrossing:** altitudeInTransition, clearedLevel, crossingPoint, crossingTime
---
Package [`fx:FlightData`]
- **Flight:** [aircraft], [arrival], [dangerousGoods], [departure], [emergency], [enRoute], flightConstraint, [flightIdentification], flightPlanOriginator, flightPlanSubmitter, [flightRulesCategory], [flightType], operator, radioCommunicationFailure, [remarks], routeTrajectoryGroup, [specialHandling], [supplementaryInformation]
- **FlightIdentification:** [aircraftIdentification], [aircraftIdentificationPrevious], [gufi], [gufiLegacy], [iataFlightDesignator]
- **RouteTrajectoryGroupContainer:** agreed, current, desired, negotiating
---
Package [`fx:RouteChanges`]
- **RouteChange:** cruiseClimbStart, level, speed 
---
Package [`fx:RouteTrajectory`]
- **RouteTrajectoryGroup:** [climbProfile], climbSchedule, [descentProfile], descentSchedule, element, [routeInformation], takeoffMass
- **FlightRouteInformation:** [airacReference], cruisingLevel, cruisingSpeed, estimatedElapsedTime, routeText, totalEstimatedElapsedTime
- **PerformanceProfile:** [profilePoint]
- **RouteTrajectoryElement:** alongRouteDistance, [constraint], elementStartPoint, flightRulesChange, modified, modifiedRouteItemReference, plannedDelay, [point4D], [routeChange], routeDesignatorToNextElement, routeTruncationIndicator, [seqNum]
- **TrajectoryPoint4D:** altimeterSetting, level, metData, [pointProperty], position, predictedAirspeed, predictedGroundspeed, time, verticalRange
- **TrajectoryPointProperty:** description, [propertyType], reference
---
Package [`fx:Constraints`]
- **RouteTrajectoryConstraint:** departureOrArrivalIndicator, description, [level], restrictionReference, [speed], [time]
---

<!----------------------------------------------------->
<!-- Links for fx:Aircraft -->
[`fx:Aircraft`]: general-guidance/fx_Aircraft
[aircraftAddress]: general-guidance/fx_Aircraft?id=aircraftaddress
[aircraftType]: general-guidance/fx_Aircraft?id=aircrafttype
[registration]: general-guidance/fx_Aircraft?id=registration
[capabilities]: general-guidance/fx_Capability
[aircraftCount]: general-guidance/fx_Aircraft?id=aircraftcount
[aircraftApproachCategory]: general-guidance/fx_Aircraft?id=aircraftApproachCategory
[coloursAndMarkings]: general-guidance/fx_Aircraft?id=coloursAndMarkings
[wakeTurbulence]: general-guidance/fx_Aircraft?id=wakeTurbulence
[icaoAircraftTypeDesignator]: general-guidance/fx_Aircraft?id=icaoAircraftTypeDesignator
[otherAircraftType]: general-guidance/fx_Aircraft?id=otherAircraftType

<!-- Links for fx:Arrival -->
[`fx:Arrival`]: general-guidance/fx_Arrival
[destinationAerodromePrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[actualTimeOfArrival]: general-guidance/fx_Arrival?id=actualTimeOfArrival
[arrivalAerodrome]: general-guidance/fx_Arrival?id=destinationaerodrome-arrivalaerodrome
[destinationAerodrome]: general-guidance/fx_Arrival?id=destinationaerodrome-arrivalaerodrome
[destinationAerodromeAlternate]: general-guidance/fx_Arrival?id=destinationAerodromeAlternate

<!-- Links for fx:Capability -->
[`fx:Capability`]: general-guidance/fx_Capability
[communication]: general-guidance/fx_Capability?id=communication
[selectiveCallingCode]: general-guidance/fx_Capability?id=selectivecallingcode
[navigation]: general-guidance/fx_Capability?id=navigation
[standardCapabilities]: general-guidance/fx_Capability?id=standardCapabilities
[surveillance]: general-guidance/fx_Capability?id=surveillance
[survival]: general-guidance/fx_Capability?id=survival
[communicationCapabilityCode]: general-guidance/fx_Capability?id=communicationCapabilityCode
[datalinkCommunicationCapabilityCode]: general-guidance/fx_Capability?id=datalinkCommunicationCapabilityCode
[otherCommunicationCapabilities]: general-guidance/fx_Capability?id=othercommunicationcapabilities-otherdatalinkcapabilities
[otherDatalinkCapabilities]: general-guidance/fx_Capability?id=othercommunicationcapabilities-otherdatalinkcapabilities
[navigationCapabilityCode]: general-guidance/fx_Capability?id=navigationCapabilityCode
[otherNavigationCapabilities]: general-guidance/fx_Capability?id=otherNavigationCapabilities
[performanceBasedCode]: general-guidance/fx_Capability?id=performanceBasedCode
[requiredRunwayVisualRange]: general-guidance/fx_Capability?id=requiredRunwayVisualRange
[otherSurveillanceCapabilities]: general-guidance/fx_Capability?id=otherSurveillanceCapabilities
[surveillanceCapabilityCode]: general-guidance/fx_Capability?id=surveillanceCapabilityCode
[carriedEltHexIdentifier]: general-guidance/fx_Capability?id=carriedEltHexIdentifier
[dinghyInformation]: general-guidance/fx_Capability?id=dinghyInformation
[emergencyRadioCapabilityType]: general-guidance/fx_Capability?id=emergencyRadioCapabilityType
[lifeJacketType]: general-guidance/fx_Capability?id=lifeJacketType
[survivalEquipmentRemarks]: general-guidance/fx_Capability?id=survivalequipmenttype-survivalequipmentremarks
[survivalEquipmentType]: general-guidance/fx_Capability?id=survivalequipmenttype-survivalequipmentremarks


<!-- Links for fx:Cargo -->
[`fx:Cargo`]: general-guidance/fx_Cargo

<!-- Links for fx:Departure -->
[`fx:Departure`]: general-guidance/fx_Departure
[airfileIndicator]: general-guidance/fx_Departure?id=airfileindicator
[airportslotidentification]: general-guidance/fx_Departure?id=airportslotidentification
[departureAerodrome]: general-guidance/fx_Departure?id=departureaerodrome-departurepoint
[departureAerodromePrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[departurePoint]: general-guidance/fx_Departure?id=departureaerodrome-departurepoint
[departurePointPrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[estimatedOffBlockTime]: general-guidance/fx_Departure?id=estimatedoffblocktime-estimatedroutestarttime
[estimatedOffBlockTimePrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[estimatedRouteStartTime]: general-guidance/fx_Departure?id=estimatedoffblocktime-estimatedroutestarttime
[estimatedRouteStartTimePrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[actualTimeOfDeparture]: general-guidance/fx_Departure?id=actualTimeOfDeparture
[takeoffAlternateAerodrome]: general-guidance/fx_Departure?id=takeoffAlternateAerodrome

<!-- Links for fx:Emergency -->
[`fx:Emergency`]: general-guidance/fx_Emergency

<!-- Links for fx:EnRoute -->
[`fx:EnRoute`]: general-guidance/fx_EnRoute
[alternateAerodrome]: general-guidance/fx_EnRoute?id=alternateAerodrome
[currentModeACode]: general-guidance/fx_EnRoute?id=currentModeACode

<!-- Links for fx:FlightData -->
[`fx:FlightData`]: general-guidance/fx_FlightData
[aircraft]: general-guidance/fx_Aircraft?id=encoding-guidance-for-fxaircraft
[arrival]: general-guidance/fx_Arrival?id=encoding-guidance-for-fxarrival
[dangerousGoods]: general-guidance/fx_Cargo?id=encoding-guidance-for-fxcargo
[departure]: general-guidance/fx_Departure?id=encoding-guidance-for-fxdeparture
[emergency]: general-guidance/fx_Emergency?id=encoding-guidance-for-fxemergency
[enRoute]: general-guidance/fx_EnRoute?id=encoding-guidance-for-fxenroute
[flightIdentification]: general-guidance/fx_FlightData?id=flightidentification
[aircraftIdentification]: general-guidance/fx_FlightData?id=aircraftidentification
[aircraftIdentificationPrevious]: general-guidance/fx_FlightData?id=aircraftidentificationprevious
[gufi]: general-guidance/fx_FlightData?id=gufi
[gufiLegacy]: general-guidance/fx_FlightData?id=compatibility-with-fixm-core-420
[flightRulesCategory]: general-guidance/fx_FlightData?id=flightRulesCategory
[flightType]: general-guidance/fx_FlightData?id=flightType
[remarks]: general-guidance/fx_FlightData?id=remarks
[specialHandling]: general-guidance/fx_FlightData?id=specialHandling
[supplementaryInformation]: general-guidance/fx_FlightData?id=supplementaryInformation
[iataFlightDesignator]: general-guidance/fx_FlightData?id=iataFlightDesignator


<!-- Links for fx:RouteChanges -->
[`fx:RouteChanges`]: general-guidance/fx_RouteChanges

<!-- Links for fx:RouteTrajectory -->
[`fx:RouteTrajectory`]: general-guidance/fx_RouteTrajectory
[climbProfile]: general-guidance/fx_RouteTrajectory?id=climbprofile-descentprofile
[descentProfile]: general-guidance/fx_RouteTrajectory?id=climbprofile-descentprofile
[profilePoint]: general-guidance/fx_RouteTrajectory?id=climbprofile-descentprofile
[routeInformation]: general-guidance/fx_RouteTrajectory?id=routeinformation
[point4D]: general-guidance/fx_RouteTrajectory?id=point4d
[pointProperty]: general-guidance/fx_RouteTrajectory?id=pointproperty
[propertyType]: general-guidance/fx_RouteTrajectory?id=pointproperty
[element]: general-guidance/fx_RouteTrajectory?id=element
[airacReference]: general-guidance/fx_RouteTrajectory?id=airacreference
[constraint]: general-guidance/fx_Constraints?id=encoding-guidance-for-fxconstraints
[routeChange]: general-guidance/fx_RouteChanges?id=encoding-guidance-for-fxroutechanges
[seqNum]: general-guidance/fb_Types?id=count-sequence-numbers

<!-- Links for fx:Constraints -->
[`fx:Constraints`]: general-guidance/fx_Constraints
[level]: general-guidance/fx_Constraints?id=level
[speed]: general-guidance/fx_Constraints?id=speed
[time]: general-guidance/fx_Constraints?id=time

<!----------------------------------------------------->
<!-----------------------------------------------------> 
