# GDIM32 In Class Activities

## Week 1

### Activity 1

Use official document and blog write by others. It will be very useful.

### Activity 2

| Questions | Answers |
| ---- | ------------------------------------------------------- |
| Q1   | 10                                                      |
| Q2   | 2                                                       |
| Q3   | Show “hello world” every frame in the log.              |
| Q4   | MonoBehaviour                                           |
| Q5   | Show "x = 10" in log.                                   |
| Q6   | Argument. Pass the value to the method.                 |
| Q7   | code is Calling a static method.                        |
| Q8   | "tansform" should be "\_playerTransform"(or transform). |

### Activity 3

[W1 In Class Activities](https://docs.google.com/document/d/1y5LOXHts-EvqE00ku0UjBCC5AgohWl3lteMNVPOctuo/edit?usp=sharing)

## Week 2

### Activity 1

<img width="1755" height="1273" alt="W2" src="https://github.com/user-attachments/assets/8956da8b-b808-4895-8c5d-dec73091c0cf" />

### Activity 2

[Change in class](https://github.com/UCI-GDIM32-W25/uci-gdim32-mg2-MG2/commit/785f3dc3be5120c0e6749ffe4ec070a3a7003dfa)

I have completed the game.

## Week 3

### Activities 0-2

buddy's name: Pengcheng Qi

### Activity 3

<img width="1755" height="1273" alt="无标题" src="https://github.com/user-attachments/assets/0915341f-4f67-4fe6-aabd-79063ce1625b" />

## Week 4

### Activity 0

buddy's name: Pengcheng Qi

### Activity 1

The scripts destroy them self. The `Awake()` of the `Locator` checks if there are multiple instance of `Locator` and destroy them.

### Activity 2

<img width="1280" height="1707" alt="1" src="https://github.com/user-attachments/assets/213acce8-25b7-4b1b-b1e2-c7988d238eeb" />

#### How will the **model-view-controller pattern** be useful in this project?


You can use model for score, view for UI, and controller for player action.

#### How will the **events** be used?

A game over event will used to tell the UI and Sound system.

#### How will a **Singleton** be used?

Make sure there are only one `GameController`.

## Week 5

### Activity 1

These design is good for those projects that you will need to have same interact with different effects. For example if you need to make bullets shoot at a table and enemy. I will use interface.

### Activity 2

#### Model

EnemyStats

ItemW5Demo2

#### Controller

EnemyW5Demo2

layerW5Demo2

#### View

DialogueBubble

InventoryUI

### Activity 3

#### Scenario 1

Scriptableobject: Data for the beat 

Parent class: Beat

Child class: Different types of beat

Singleton: Gamecontroller contains score etc.

#### Scenario 2

Scriptableobject: animations and stats

Abstract parent class and multiple interfaces: Attack and movements.

#### Scenario 3

Abstract parent class and two child classes: plant and rock. 

Interfaces: which are destroyable and crops.

State machine: Different grow stage

### Activity 4

Haoyi Zhang, Pengcheng Qi, Allen Gu

[Final Project Proposal Template - Google Docs](https://docs.google.com/document/d/1x9D6Q_2PD2IP5_ACEah36JJO2HM0rF6mYcNEO8_yNTk/edit?tab=t.0)

## Week 6

###  Activity 1

#### Gizmo

This tool can draw things that can only seen by the developer. This tool can used to draw things like collider and velocity etc. This can help developers to quickly find some issue like wrong collider.

#### Profiler

This tool can helps developer to find why the game is lagging by show what happed in single frame. So developer can know where to optimize the game to get higher performance.

#### Breakpoint

This tool can pause the game exactly before a certain line of code. So developer can check the variable and logic of the code and find what goes wrong and fix it.

### Activity 2

Attendance: Allen Gu, Haoyi Zhang, Pengcheng Qi

[Draft Document](https://docs.google.com/document/d/1x9D6Q_2PD2IP5_ACEah36JJO2HM0rF6mYcNEO8_yNTk/edit?tab=t.0)

## Week 7

### Activity 1

1. State Machine

   Duck have 2 states

   ```c#
   private enum DuckState 
   {
       Wandering,
       Pursuing
   }
   ```

    UpdateState() → RunState() → Run[Wander/Pursue]State()

   ```c#
       private void UpdateState ()
       {
           if(HasLineOfSightToPlayer())
           {
               _state = DuckState.Pursuing;
           }
           else 
           {
               _state = DuckState.Wandering;
           }
       }
   ```

   ```c#
       private void RunState ()
       {
           switch(_state) 
           {
               case DuckState.Wandering: RunWanderState(); break;
               case DuckState.Pursuing: RunPursueState(); break;
               default: Debug.LogError("unhandled state " + _state); break;
           }
       }
   ```

2. Raycasting

   ```C#
   Physics.Raycast(_raycastStart, _raycastDir, out hitInfo, _lineOfSightMaxDistance, _lineOfSightLayers.value)
   ```

   ```c#
   _raycastStart = transform.TransformPoint(_raycastStartOffset);
   _raycastDir = (PlayerW72.Instance.PlayerCenter - _raycastStart).normalized;
   ```

   Use tag to verify this is player

   ```C#
           if(hitInfo.collider.gameObject.tag.Equals(_playerTag))
           {
               _hasLineOfSightToPlayer = true;
           }
   ```

3. Vector

   How to find direction from A to B

   ```c#
   Vector3 direction = (B - A).normalized;
   ```

### Activity 2

Attendance: Allen Gu, Haoyi Zhang, Pengcheng Qi

### Activity 3

<img width="822" height="717" alt="5f5f337556e90bfbdca6da1725232f75" src="https://github.com/user-attachments/assets/8fbab51e-2644-47fb-a1b1-8af152a10d3e" />

### Activity 4

[Link to the Trello Board](https://trello.com/b/TcDWOqGX)

### Activity 5
