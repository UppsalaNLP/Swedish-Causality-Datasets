# Binary Trial Data Set

This set contains sentences annotated for the presence of causal relations. It was extracted by matching a set of keywords expressing causality between events, objects or agents. More information on this will be available in the release article on these data sets. The set was annotated by three experts and the annotations were not consolidated, so each matched sentence comes with three labels assigned to it.

The data is formatted in JSON. For each sample, the data includes 

- the __keyword__ that was matched
- the ID of the __document__ it was taken from
- the title of the __section__ it occured in
- up to two sentences of context to the left
- the __target sentence__ that was matched
- up to two sentences of context to the right
- the binary __annotation__ for causality (containing one label for each of the annotators)
- the annotation for __context__ (again one label per annotator or null if the sentence is not annotated as causal)

Each target sentence comes with the two preceding and the two following sentences as context and is annotated for causality and scope of the causality. The scope here refers to whether or not the causality is contained within the target sentence (_t_) or whether the context is needed to understand it as causal (_c_).
