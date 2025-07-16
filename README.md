# Team Code_AI_3.0

**AI-Enhanced Text Adventure Game – Usage Guide**

## 🧙 Overview

A dynamic, AI-powered text-based RPG that showcases:

* **Step 5:** Scale-agnostic deployment (CLI → API)
* **Step 6:** Intelligent story generation, NPC dialogue, adaptive quests, and more

---

## 🛠 Step 5: Scale-Agnostic Approach

### 🔄 Local Mode

```bash
jac run adventure.jac
```

### 📘 Sample Output

```
🌟 Initializing AI-Enhanced Text Adventure World...

✅ World created with 5 connected realms
🏰 Rooms: Mystical Grove, Crystal Caverns, Sky Citadel, Abyssal Depths, Celestial Temple

🎮 Creating test player...
Player created: player_created

👤 Player Status:
Name: Hero, Health: 100, XP: 0, Level: 0
Inventory: enchanted dagger, healing potion

🏞️ Dynamic Room Description:
Room: mystical_grove
Base: An ancient grove where magic flows through every leaf and branch
Dynamic: The enchanted breeze whispers forgotten tales of travelers who once walked here.
Story Event: A glowing wisp circles around you, hinting at an undiscovered portal...

⚔️ Available Items: silver coin, mysterious map, healing herb
👹 Monsters: Shadow Wolf
👥 NPCs: Sage Eldara, Forest Spirit
🚪 Exits: crystal_caverns, sky_citadel

🎯 Quest Suggestion:
Level 0 Quest: Seek the whispering wisp and uncover the portal rune...

🗺️ World Map:
  mystical_grove: 2 exits, Items: True, Monsters: True, NPCs: True
  crystal_caverns: 2 exits, Items: True, Monsters: True, NPCs: True
  sky_citadel: 2 exits, Items: True, Monsters: True, NPCs: True
  abyssal_depths: 2 exits, Items: True, Monsters: True, NPCs: True
  celestial_temple: 0 exits, Items: True, Monsters: True, NPCs: True

🚀 Game ready! Deploy with: jac serve adventure.jac
📡 API endpoints will be available for multiplayer adventure!
```

---

### ☁️ Cloud Deployment

```bash
jac serve adventure.jac
```

#### 🧩 Auto-Generated API Endpoints

```
POST /AdventureAPI/create_player
POST /AdventureAPI/get_player_status
POST /AdventureAPI/get_dynamic_room
POST /AdventureAPI/move_player
POST /AdventureAPI/fight_monster
POST /AdventureAPI/take_item
POST /AdventureAPI/use_item
POST /AdventureAPI/talk_to_npc
POST /AdventureAPI/get_quest_suggestion
POST /AdventureAPI/complete_quest
POST /AdventureAPI/get_world_map
```

---

## 🤖 Step 6: AI-Enhanced Gameplay Features

### 1. 🏞️ **Dynamic Room Descriptions**

```python
jac def generate_room_description(room_name: str, player_history: list[str], current_items: list[str]) -> str by llm();
```

* Immersive scene descriptions influenced by player decisions

### 2. 📖 **Story Events Generator**

```python
jac def generate_story_event(player_name: str, current_room: str, inventory: list[str], last_actions: list[str]) -> str by llm();
```

* Contextual event narration based on real-time player state

### 3. 🧙 **NPC Dialogue Engine**

```python
jac def generate_npc_dialogue(npc_name: str, player_name: str, conversation_history: list[str], current_situation: str) -> str by llm();
```

* Interactive, evolving conversations with AI NPCs

### 4. 🎯 **Adaptive Quest Suggestions**

```python
jac def suggest_quest(player_level: int, inventory: list[str], completed_quests: list[str]) -> str by llm();
```

* AI-generated tasks tailored to player level and progress

### 5. ⚔️ **Combat Narration**

```python
jac def generate_combat_story(player_name: str, monster_name: str, player_inventory: list[str], outcome: str) -> str by llm();
```

* Dynamic combat storytelling with loot and experience rewards

---

## 🌐 API Usage Examples

### Create a Player

```bash
curl -X POST "http://localhost:8000/AdventureAPI/create_player" \
-H "Content-Type: application/json" \
-d '{"player_id": "player1", "target": "Arin"}'
```

### Get Player Status

```bash
curl -X POST "http://localhost:8000/AdventureAPI/get_player_status" \
-H "Content-Type: application/json" \
-d '{"player_id": "player1"}'
```

### Explore a Room

```bash
curl -X POST "http://localhost:8000/AdventureAPI/get_dynamic_room" \
-H "Content-Type: application/json" \
-d '{"player_id": "player1", "target": "mystical_grove"}'
```

### Fight a Monster

```bash
curl -X POST "http://localhost:8000/AdventureAPI/fight_monster" \
-H "Content-Type: application/json" \
-d '{"player_id": "player1", "target": "Shadow Wolf"}'
```

---

## 🧩 Key Demonstrations

### Step 5 – Deployment Benefits

* ✅ **No code changes** between local and API modes
* ✅ **REST API auto-generated** from walker abilities
* ✅ **Flexible** – CLI or Web API
* ✅ **Consistent gameplay logic**

### Step 6 – AI-Powered Enhancements

* 🧠 **Context-aware storytelling**
* 🗣️ **Natural NPC conversations**
* 🎮 **Smart quest and event generation**
* 🛡️ **Dynamic combat with narration**
* 📊 **Scalable multi-user support**

---

## 🌍 Real-World Applications

This pattern is useful for:

* Text-based adventure platforms
* Interactive learning simulations
* Game design prototypes with AI storytelling
* Role-playing companion bots

---

## 🧑‍💻 Team Members

* S.Jathees
* S.Sharukshan
* J.Derick


