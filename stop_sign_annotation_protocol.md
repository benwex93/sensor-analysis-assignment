# Nexar Home Assignment  
**Assignment:** Define a Labeling Protocol for Stop Sign Behavior  

---

## Labeling Instructions

### For each stop sign in the video:
- **Approximate timestamp when stop sign first visible:** ______  
- **Did vehicle slow?** (Yes/No)  
  - If **Yes**:  
    - Was another vehicle already stopped? (Yes/No)  
    - Approximate number of “inch up” stops: ______  
    - Approximate timestamp when vehicle finally decelerated for stop-sign: ______  
    - Complete stop? (Yes/No)  
- **Approximate timestamp when stop sign out of sight:** ______  
- **Driver’s action after stop:** (Left / Right / Straight)  
- **Other drivers stopped at intersection (multiple allowed):** (Opposite / Left / Right)  

---

### Collisions / Near-Collisions
- **Event type:** (Collision / Near-collision)  
- **Timestamp of event:** ______  
- **Driver involved?** (Yes/No)  
  - If **Yes, driver:**  
    - Turned: (Left / Right / Straight)  
    - Collision location on driver’s vehicle: (Left / Right / Front / Back)  
- **One other driver involved?** (Yes/No)  
  - If **Yes, other driver:**  
    - Approached from: (Left / Right / Opposite)  
    - Turned: (Left / Right / Straight)  
    - Collision location on other driver’s vehicle: (Left / Right / Front / Back)  
- **Driver not involved and secondary driver involved?** (Yes/No)  
  - If **Yes, secondary driver:**  
    - Approached from: (Left / Right / Opposite)  
    - Turned: (Left / Right / Straight)  
    - Collision location on secondary vehicle: (Left / Right / Front / Back)  

---

## Explanation
The goal is to extract as many features as possible since the final task is not clearly defined.  
Downstream, data scientists can decide which features serve as labels and which can be dropped.  

- Annotators should approximate timestamps without worrying about exactness.  
- Criteria are objective and easy to recognize (e.g., whether the vehicle stopped), avoiding subjective judgments like *“Was the driver reckless?”*.  
- Such subjective assessments may be useful for unsupervised learning but are not part of this task.  

---

## Assumptions
- Only available information is the video itself.  
- Near-collisions are recognizable and important to capture (to retain valuable training signal).  
- It is important to distinguish between **normal deceleration for a stop sign** and **deceleration due to a crash**.  
- Approximate timestamps are sufficient.  
- Collision locations can be localized to one of four sides.  
- No more than two cars are involved in a single collision.  

---

## Trade-offs
- We ignore detailed timestamps for every “inch up” event (small start/stop movements behind another car at a stop sign), since this is overly complex and burdensome for the annotator.  
