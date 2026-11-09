# Reflection Questions — Suggested Brief Answers

1. **What is the prediction target, and why is the original quality column excluded from the input features?**  
   The target is a binary category: `quality >= 6` is GOOD QUALITY and `quality < 6` is NEEDS IMPROVEMENT. The original quality score is excluded because it is used to create the target; including it as an input would leak the answer to the model and produce misleading evaluation results.

2. **What does recall for the GOOD QUALITY class tell you? What could low recall mean for the business?**  
   Recall for GOOD QUALITY is the proportion of truly good-quality test samples that the model correctly identifies as good. Low recall means some good samples are incorrectly flagged as needing improvement, which could lead to unnecessary additional review or missed opportunities to recognize acceptable batches.

3. **Why might a model trained on this red-wine dataset perform differently on another producer's wine samples?**  
   Producers may use different grapes, processes, equipment, regions, and measurement conditions. These differences can change the relationship between the measured attributes and the quality category, so the training data may not represent the new samples.

4. **Why should the prediction be treated as a preliminary screening result rather than a final quality decision?**  
   The model is trained on a limited historical dataset and can make incorrect predictions. Final decisions should use appropriate laboratory testing, sensory evaluation, food-safety procedures, and professional quality-control judgment.

5. **What additional data or testing would help improve the reliability of the system?**  
   More representative samples from different producers, regions, vintages, and production conditions would help. The model should also be tested on independent new batches, monitored for changing data patterns, and evaluated using precision, recall, F1-score, and a confusion matrix—not accuracy alone.
