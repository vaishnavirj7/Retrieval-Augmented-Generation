# Retrieval-Augmented-Generation

`Multilingual RAG` - Example of RAG (Retrieval Augmented Generation) by combining a `VectorDB (Weaviate)` for information retrieval with a generative AI model for text generation.
 - Queries are performed on a vectorized collection of `Wikipedia` articles.
 - The `.with_near_text()` method retrieves relevant documents based on semantic similarity to a query (e.g., "Vacation spots in California").
 - The retrieved data is passed to a generative AI model (`OpenAI`) to create new content.
 - The `.with_generate()` method is used to generate text based on the retrieved documents:
    - `Single Prompt Generation`: A Facebook ad is generated using the retrieved article's title and text.
    RAG combines retrieval (from a knowledge base) with generation (using a language model). This approach enhances the generative model's output by grounding it in factual, retrieved data, making it more accurate and contextually relevant. In this code:

      - `Weaviate` handles the retrieval.
      - `OpenAI`'s generative model handles the generation.
      - The `.with_generate()` method bridges the two, making this a `RAG` implementation.
