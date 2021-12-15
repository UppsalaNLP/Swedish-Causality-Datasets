# Ranking Dataset

This set contains pairs of sentences annotated on a 6 point scale by how well the match the causality expressed in an exemplary prompt containing a causal connective and at least a cause or an effect.
Examples of such prompts are:

- _"Radon orsakar cancer"_ 'Radon causes cancer'
- _"Radon orsakar [MASK]"_ 'Radon causes [MASK]'
- _"[MASK] orsakar cancer"_ '[MASK] causes cancer'

We use the [MASK] token here, because the sentences were embedded using a Swedish BERT model for sentence similarity.


The data is formatted in JSON. For each sample, the data includes 

- the input used to generate the  __prompt__ that is supposed to be matched (instead of a full statement, these take the form "_Orsak: “radon”, Verkan: “cancer”_", "Cause: “radon”, Effect: “cancer”", "_Orsak: “radon”_", etc.)
- for both sentences:

	* up to two sentences of context to the left
	* the __target sentence__ that was matched
	* up to two sentences of context to the right


- the ranking __annotation__ for causality 


The annotation scheme is as follows:

| Label | Meaning                                                     |
|:-----:|-------------------------------------------------------------|
| 0     | both sentences are irrelevant to the prompt                 |
| 1     | first sentence relevant, second sentence irrelevant         |
| 2     | second sentence relevant, first sentence irrelevant         |
| 3     | both sentences equally relevant                             |
| 4     | first sentence most relevant, second sentence also relevant |
| 5     | second sentence most relevant, first sentence also relevant |
