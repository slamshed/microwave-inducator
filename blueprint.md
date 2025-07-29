# Microwave Indicator – Blueprint Inputs

This file describes the inputs required for the Microwave Indicator blueprint in Home Assistant.

## Inputs

### 1. Power Sensor (`power_sensor`)
**Type:** entity  
**Required:** Yes  
**Description:**  
The power sensor that measures the microwave’s power usage in watts.  
**Example:** `sensor.ikea_of_sweden_inspelning_smart_plug_power_4`

---

### 2. Red Indicator (`red_entity`)
**Type:** entity (switch or light)  
**Required:** Yes  
**Description:**  
This is the entity that turns **on** while the microwave is actively cooking.  
**Example:** `switch.shelly_plus_1_1_switch_0`

---

### 3. Green Indicator (`green_entity`)
**Type:** entity (switch or light)  
**Required:** Yes  
**Description:**  
This is the entity that turns **on** after the microwave finishes and stays on for the configured duration.  
**Example:** `switch.shelly_plus_1_4_switch_0`

---

### 4. On Threshold (`on_threshold`)
**Type:** number (float or integer)  
**Required:** Yes  
**Description:**  
The wattage level above which the microwave is considered “on.”  
**Example:** `10`

---

### 5. Off Threshold (`off_threshold`)
**Type:** number (float or integer)  
**Required:** Yes  
**Description:**  
The wattage level below which the microwave is considered “off.”  
**Example:** `10`

---

### 6. Green On Duration (`green_on_duration`)
**Type:** number (integer, seconds)  
**Required:** Yes  
**Description:**  
How long the green indicator should stay on after cooking ends.  
**Example:** `60`

---

### Notes

- On and off thresholds should be selected to suit your microwave's idle and active wattage. A good rule of thumb is:
  - `on_threshold` = 10 W (or slightly above idle)
  - `off_threshold` = same or slightly lower than `on_threshold`
- If your microwave drops to 0W between cooking stages, consider using a short delay before transitioning to green.

---
