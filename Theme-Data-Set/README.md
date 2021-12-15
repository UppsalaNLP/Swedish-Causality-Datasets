# Main Binary Dataset

This set contains individual sentences annotated for the presence of causal relations.

While the sentences were sampled by matching cause-effect pairs such as _radon_ and _cancer_, the annotation is strictly about whether there are any kind of causal relations in a given sentence and agnostic of the initial cause-effect pair.
The data is formatted in JSON. For each sample, the data includes 

- the __theme__ that was matched
- up to two sentences of context to the left
- the __target sentence__ that was matched
- up to two sentences of context to the right
- the binary __annotation__ for causality
