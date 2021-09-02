# F11Robo_CG
対向二輪ロボットのシュミレーションを動作させるROSアプリケーション用リポジトリ
(CGの課題用)
# キーボード操作
以下のコマンドを実行するとキーボードからロボットを操作できる。
```bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/F11Robo/diff_drive_controller/cmd_vel
```
# Gazebo
```bash
roslaunch F11Robo_CG gazebo.launch
```
# mapping
以下のコマンドを入力して実行する
```bash
roslaunch F11Robo_CG gmapping_gazebo.launch
```
## マップ保存
```bash
rosrun map_server map_saver -f ファイル名
```
Ex. ファイル名がmapのとき
```bash
rosrun map_server map_saver -f  map
```
# navigation
以下のコマンドを入力して起動する
gazeboで動かす場合
```bash
roslaunch F11Robo_CG navigation_gazebo.launch
```
# Path Planning & Path Following
自作のナビゲーションノードで
Path PlanningのアルゴリズムにはA*、Path FollowingのアルゴリズムにはPurePursuitを使用した
```bash
roslaunch F11Robo_CG navi.launch
```
# Goal generator
navigationを起動後以下のコマンドを実行する
```bash
rosrun F11Robo_CG goal_generator
```