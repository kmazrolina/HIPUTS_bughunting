# MISS2024_Project_Glowczyk_Zrobek
# Summary of the HiPUTs Multilane Feature in Web Visualization Project 🚗🌐

## Project Overview
The goal of the project was to enhance the web visualization capabilities of the HiPUTs simulation by integrating and debugging the multilane feature, making the visualization more useful for debugging purposes and improving the realism of the simulation.

## Key Accomplishments 🏆

### 1. Problem Domain Definition 📝
- **Issues Identified:**
    - Vehicles moving on pedestrian/bicycle paths.
    - Lack of multiple lanes.
- **Proposed Solutions:**
    - Integrate multilane support into web visualization.
    - Create minimal test scenarios for better analysis.

### 2. Integration of Multilane in Web Visualization 🔧
- Added support for multilane features in the web visualization.
- Included RoadID and LaneID in car info pop-up windows.
- Implemented car position shifts for better visualization.
- Identified issues with cars driving against traffic and limited OSM lane visualization.

### 3. Tool Selection and Further Analysis 🛠️
- Explored tools such as JOSM, GPX, and React components for improved visualization.
- Proposed modifications for enhanced zooming, lane visualization, and individual car tracking.

### 4. Lane Visualization Implementation 🖼️
- Visualized lanes using React Leaflet `<Polyline/>`.
- Fixed bugs related to cars driving against traffic and incorrect lane placements.
- Investigated incorrect road mappings and potential data corruption in OSM.

### 5. Prototype Development 💡
- Developed prototypes with features like map toggling, lane search, road segment highlighting, and dynamic information display.
- Analyzed road directionality and identified issues with lane duplication.

### 6. Bug Fixes and Strategy Implementation 🐛
- Fixed bugs by modifying code and adding edge existence checks.
- Implemented strategies to correct graph connectivity and eliminate fake road connections.

### 7. Configuration and Running the Application ⚙️
- Configured the server to support web visualization.
- Updated instructions for running the application, including enabling web visualization settings and modifying `model_settings.json`.

### 8. Recent Updates 🆕
- Changed `crossroadMinDistance` from 10 to 0 to eliminate incorrect intersections.
- Added car length to the web visualization.
- Updated code to fix failing tests and improve visualization accuracy.
- Enhanced README with instructions for running the web visualization and customizing car display options.

## Detailed Changes and Additions 🛠️

### Code Adjustments
- Corrected dead ends and map connectivity issues by updating the `DeadEndsCorrector.java`, `MapConnectivityCorrector.java`, `WrongConnectionsCorrector.java`, and `AddReversesOnDeadEndsFixer.java` files.
- Added conditions to check for null fixers before transforming graphs.
- Included edge existence checks to avoid adding duplicate edges.

### Configuration Updates
- Introduced new boolean variables in `Configuration.java` for displaying car length and customizing car icon styles.
- Updated the `application.yml` file to include options for drawing lanes and car length in web visualization.

### Visualization Enhancements
- Added new classes and methods in `CarMessage.java`, `CarOptionsMessage.java`, and `CarOptionsMsgProducer.java` for managing car display options.
- Modified `VisualizationService.java` to initialize and send car display options to the web visualization.
- Updated React components (`App.tsx`, `Car.tsx`, `MapContainer.tsx`, `Visualization.tsx`) to handle new car options and display settings.

## Future Directions 🔮

### Further Bug Fixes
- Continue monitoring and fixing any emerging issues related to road mappings and car behaviors.

### Tool Integration
- Explore the possibility of integrating JOSM with React for better map editing and visualization.

### Feature Enhancements
- Improve zooming capabilities and lane visualization further.
- Add more sophisticated debugging tools for better analysis of car behaviors in the simulation.

### Testing and Validation
- Conduct extensive testing with larger maps and more complex scenarios to ensure robustness and reliability.

The project successfully improved the web visualization capabilities, fixed critical bugs, and laid a strong foundation for future enhancements and tool integrations. 🏁

Code avaliable at [HiPUTS Gitlab](https://gitlab.ii.agh.edu.pl/g/ncn-scat/HiPUTS)

Branches:
- [freature/multi-lane-visualization](https://gitlab.ii.agh.edu.pl/g/ncn-scat/HiPUTS/-/commits/freature/multi-lane-visualization)
- [pre-merged-develop](https://gitlab.ii.agh.edu.pl/g/ncn-scat/HiPUTS/-/commits/pre-merged-develop)
- [web_visualization_rebase](https://gitlab.ii.agh.edu.pl/g/ncn-scat/HiPUTS/-/commits/web_visualization_rebase)

Project documentation avaliable in [wiki :book:](https://github.com/kmazrolina/MISS2024_Project_Glowczyk_Zrobek/wiki).
