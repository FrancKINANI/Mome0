# Mome Mobile Robot Simulation

Ce projet présente une simulation de robot mobile utilisant **ROS1 Noetic**, **Gazebo**, et **RViz** pour les tâches de **cartographie**, **localisation** et **navigation autonome**. La simulation se déroule sous **Linux Focal Fossa 20.04**, avec des nœuds écrits en **Python** et des fichiers de configuration en **xacro** et **XML**.

## Fonctionnalités

1. **Cartographie** : Création d'une carte de l'environnement en utilisant des capteurs intégrés.
2. **Localisation** : Utilisation d'un algorithme de localisation pour déterminer la position actuelle du robot.
3. **Navigation autonome** : Le robot se déplace de manière autonome à travers l'environnement cartographié.

## Prérequis

- **Ubuntu 20.04 (Focal Fossa)**
- **ROS1 Noetic**
- **Gazebo** : simulateur pour la modélisation de l'environnement.
- **RViz** : outil de visualisation pour la robotique sous ROS.
- **Python 3.8+**
- **xacro** pour les fichiers de description de robot.
  
### Installation

1. **Installer ROS1 Noetic** :
   - Suivez les instructions sur le [site officiel de ROS](http://wiki.ros.org/noetic/Installation/Ubuntu).

2. **Cloner le dépôt Git** :
   ```bash
   git clone https://github.com/FrancKINANI/Mome0.git
   cd mome
   ```

3. **Configurer les dépendances** :
   ```bash
   sudo apt install ros-noetic-gazebo-ros ros-noetic-navigation
   ```

4. **Compiler le package** :
   ```bash
   catkin_make
   source devel/setup.bash
   ```

### Simulation

1. **Lancer Gazebo** :
   ```bash
   roslaunch mome gazebo.launch
   ```

2. **Visualiser dans RViz** :
   ```bash
   roslaunch mome rviz.launch
   ```

3. **Démarrer la navigation autonome** :
   ```bash
   roslaunch mome navigation.launch
   ```

### Arborescence simple du projet

```bash
mome/
├── launch/
│   ├── gazebo.launch
│   ├── rviz.launch
│   └── navigation.launch
├── src/
│   ├── mapping.py
│   ├── localization.py
│   └── navigation.py
├── urdf/
│   └── mome_robot.xacro
├── config/
│   ├── costmap_params.yaml
│   ├── local_planner.yaml
│   └── global_planner.yaml
└── README.md
```

Contributeurs

- Franck HTW
- Professeur ABANAY
