**RAG implementation on a story**

So first, I saved the story in a txt file and used TextLoader to make it a Document data type. Then I used RecursiveCharacterTextSplitter to divide the document into various number of chunks, so that its easier for searching.

I then embedded the chunks using an open source model "sentence-transformers" and stored in a vector db called chromadb.

I connected the Gemini LLM and created a prompt and gave it context about the story related to the question. For example if the question is how old is the character named Elias, the context retrieved will be related to the question. This is done by using embeddings and cosine-similarity.

The LLM then appropriately answers the question.
