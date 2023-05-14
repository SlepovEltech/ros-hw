# ROS homework (ИРПОДМР)
## Task
Необходимо реализовать класс, представляющий собой ROS-ноду. Логика поведения ноды следующая:
   * предполагается, что нода будет использоваться в совокупности с нодами turtlesim_node и turtle_teleop_key из пакета turtlesim
   * разрабатываемая нода должна создавать второй движущийся объект в окне turtlesim_node. При этом стартовая черепашка будет управляться с клавиатуры, а вторая - нет
   * необходимо реализовать возможность движения второй черепашки за первой. Для этого необходимо считывать координаты обеих черепашек через топики /<имя черепашки>/Pose, вычислять трансформацию между позициями и посылать команды в топик /<имя черепашки2>/cmd_vel
   * необходимо обернуть разрабатываемую ноду в один класс, чтобы избежать глобальных переменных
   * необходимо разработать launchfile, запускающий все требуемые ноды, а также установить в нём в качестве входного параметра скорость черепашки-преследователя.

## HowTo
git clone into <your worspace/src>
```
cd <your worspace>
catkin_make
source devel/setup.bash
roslaunch slepov_node slepov.launch
```
Или для кастомной настройки скорости:
```
roslaunch slepov_node slepov.launch speed:=2
```
