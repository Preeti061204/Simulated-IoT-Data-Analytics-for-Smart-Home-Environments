The synthetic datasets provided simulate hourly energy consumption across various rooms of a smart home environment, including the kitchen, living room, two bathrooms and two bedrooms. Each room’s dataset captures not only the power usage of individual appliances (measured in watts or kilowatt-hours), but also includes contextual parameters such as indoor and outdoor temperature, humidity, appliance activity, and occupancy status.

#### ✅ **Room-wise Dataset Highlights**

* **Kitchen:**

  * Tracks usage of microwave, fridge, gas/induction stove, exhaust fan, etc.
  * Includes indoor temperature, humidity, absolute humidity, and appliance usage indicators.
  * Contains outdoor weather conditions for contextual analysis.

* **Living Room:**

  * Monitors power usage of smart TV, fan, heater, lights, and other ports.
  * Captures motion detection, sound detection, lighting levels, and air quality (indoor & outdoor).
  * Includes occupancy levels and airflow index for comfort analysis.

* **Bathrooms 1 & 2:**

  * Records geyser, lights, exhaust fan, washing machine, and other small appliance usage.
  * Includes temperature, humidity, absolute humidity, and occupancy status.
  * Bathroom 1 includes additional correlation with Bathroom 2’s conditions.

* **Bedrooms 1 & 2:**

  * Tracks power consumption of fans, tube lights, TV, heater, and small lights.
  * Contains temperature, humidity, absolute humidity, and occupancy indicators.
  * Monitors device usage like ports and categorizes energy by weekday for temporal patterns.



#### 🔄 **Combined Energy Dataset**

* Aggregates total energy consumption (in kWh) across:

  * Living Room, Bathroom 1, Bathroom 2, Bedroom 1, Bedroom 2, and Kitchen.
* Provides a unified timestamped view of total household energy usage.
* Supports:

  * Comparative analysis of room-wise vs. total energy.
  * Identification of peak consumption periods.
  * Development of time-series forecasting or energy optimization models.
