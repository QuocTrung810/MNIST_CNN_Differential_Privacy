# Conclusion

1. Accuracy:

    - FNN without DP: 96.31%
    - FNN with DP: 89.84%

    The FNN model without Differential Privacy (DP) has about 7% higher accuracy than the model using DP. This is expected and shows the trade-off between accuracy and privacy.

2. Privacy:

    - FNN without DP: No special privacy protection measures.

    - FNN with DP: ε (epsilon) = 1.00

    Epsilon is a measure of privacy in Differential Privacy. The lower the epsilon value, the higher the privacy level. Epsilon = 1.00 is considered a fairly good privacy level in many practical applications.

3. Implications of the results:

    a) Trade-off between performance and privacy:
    The results clearly show the trade-off between model accuracy and privacy protection. The DP model ensures better privacy, but at the cost of reduced accuracy.

    b) Privacy protection:
    With ε = 1.00, the DP-SGD model provides a strong guarantee that the participation or non-participation of an individual in the training dataset will not significantly affect the model's results. This protects the personal information of people in the dataset.

    c) Practical applications:
    Despite the reduced accuracy, 91.05% is still a good result for many applications, especially those requiring high privacy such as in the medical or financial fields.

4. Security:

    - Add noise: DP-SGD adds noise to the gradients during training, making it harder to infer individual data from the model.

    - Limit sensitivity: By limiting the norm of the gradients, DP-SGD ensures that no single data point can influence the model unduly.

    - Protect against reverse inference attacks: Reduces the attacker's ability to determine whether a particular data point was used to train the model.
