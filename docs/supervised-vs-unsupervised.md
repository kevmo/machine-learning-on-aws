Supervised and unsupervised learning are two of the primary categories of machine learning techniques, and they're based on how we use data to train models.

**Supervised Learning**:
- **Definition**: In supervised learning, we have an input variable \( X \) and an output variable \( Y \), and we use an algorithm to learn the mapping function from the input to the output. The goal is to approximate the mapping function so well that when we have new input data (\( X \)), we can predict the output variables (\( Y \)) for that data.
- **Label Requirement**: It requires labeled data, meaning each example in the dataset is paired with the correct output.
- **Use Cases**: 
    - **Regression**: Predicting a continuous value. For instance, predicting the price of a house based on features like the number of bedrooms, square footage, etc.
    - **Classification**: Categorizing data into predefined classes or labels. For example, determining if an email is spam or not spam.
- **Example**: If you had a basket of fruits and labels for each fruit, supervised learning could be used to teach a machine the type of fruit based on features like color, size, and shape. Once the machine is trained, you could show it a new fruit (without a label), and it would predict the type of fruit.

**Unsupervised Learning**:
- **Definition**: Unlike supervised learning, in unsupervised learning, we only have input data \( X \) and no corresponding output variables. The goal for unsupervised learning is to model the underlying structure or distribution in the data to learn more about the data.
- **Label Requirement**: It doesn't require labeled data.
- **Use Cases**:
    - **Clustering**: Finding natural groupings in data. For instance, segmenting customers based on purchasing behavior.
    - **Association**: Discovering rules that describe large portions of the data. For example, people that buy X also tend to buy Y.
- **Example**: Back to the basket of fruits – with unsupervised learning, the machine would group the fruits based on similarities: all apples together, all bananas together, etc., but it wouldn’t know that one group is called "apples" and another is called "bananas."

In essence, supervised learning is about learning a function that maps input to output based on example input-output pairs, while unsupervised learning is more about finding hidden patterns or intrinsic structures in input data.