Search’s relevance settings can help you deliver the most relevant content to your users by letting you tailor how search queries match your results.

## Relevance score and tuning

When you search, the system will calculate how well a document matches your query and give that document a relevance score (called a **document score**). This is used to deliver the most relevant results first. Relevance tuning is about tweaking this score calculation so that the results are ordered the way you want.

Silverstripe Search offers the following ways to tune your relevancy scoring:

- Configuring [Search weighting](./weights) lets you emphasise certain fields
- Adding [Search Boosts](./boosts) can promote results that match certain criteria
- Changing the [Precision](./precision) setting will globally affect how searches match queries
- Adding [Synonyms](./synonyms) can change how individual terms are matched
- Using [Curations](./curations) you can promote or hide individual results for specific queries