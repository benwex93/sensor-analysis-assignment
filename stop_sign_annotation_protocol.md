Nexar Home Assignment Assignment: Define a Labeling Protocol for Stop Sign Behavior 

Labeling Instructions:

For each stop sign in the video:

Approximate timestamp when stop sign first visible: ______
    • Did vehicle slow? (Yes/No)
        ◦ If yes: was another vehicle already stopped? (Yes/No)
        ◦ If yes: Approximate number of “inch up” stops: ______
        ◦ Approximate timestamp when vehicle finally decelerated for stop-sign: ______
        ◦ Complete stop? (Yes/No)
    • Approximate timestamp when stop sign out of sight: ______
    • Driver’s action after stop: (Left / Right / Straight)
    • Other drivers stopped at intersection (can select multiple): (Opposite / Left / Right)
Collisions / Near-Collisions
    • Event type: (Collision / Near-collision)
    • Timestamp of event: ______
    • Driver involved? (Yes/No)
    • If yes, driver: 
        ◦ Turned (Left / Right / Straight)
        ◦ Collision location on driver’s vehicle: (Left / Right / Front / Back)
    • One other driver involved? (Yes/No)
    • If yes, other driver: 
        ◦ Approached from (Left / Right / Opposite)
        ◦ Turned (Left / Right / Straight)
        ◦ Collision location on other driver’s vehicle: (Left / Right / Front / Back)
    • Driver not involved and secondary driver involved? (Yes/No)
    • If yes, secondary driver: 
        ◦ Approached from (Left / Right / Opposite)
        ◦ Turned (Left / Right / Straight)
        ◦ Collision location on secondary vehicle: (Left / Right / Front / Back)

Explanation:
The goal is to extract as much information as many features as possible since the final task is not clearly defined. Then, downstream, data scientists can choose which features will serve as labels and which features can be dropped. To achieve this, our instructions attempt to abstract out as much information as possible without getting too bogged down with the details. 
The annotator is requested to approximate timestamps to the best of his ability without worrying too much about exactness. We try to list the checklist in a logical and convenient manner for the annotator.
Criterion is given as objective as possible and are easy to recognize. There is nothing subjective like “was driver driving reckless?” or “who was at fault?”. These are interesting questions but are a more suitable task for unsupervised learning.

Assumptions:
    • Only available information is the video itself. 
    • That is possible to recognize a near-collision. If we don’t try then we lose valuable training signal
    • Important to distinguish between decelerating for stop signs (normal driving) and decelerating for crash
    • That approximate timestamps are sufficient
    • Collision location can be localized to one of 4 sides
    • No more than 2 cars per collision
    
Trade-offs:
We ignore timestamps for “inching up” i.e. every single starting and stopping moment as you approach the stop-sign behind another car since it is very complex and burdensome for annotator