## RAG Assignment Part a
In this assignment, I implemented a RAG pipeline using Langchain and Pinecone.

## RAG Assignment Part b
In this assignment, I implemented a complete Retrieval-Augmented Generation (RAG) pipeline using LangChain and Milvus for semantic search, and OpenAI’s LLM for question answering. The process begins by loading a PDF file using PyPDFLoader, and then splitting it into manageable text chunks using the RecursiveCharacterTextSplitter. This allows the model to handle large documents efficiently by breaking them into overlapping sections of fixed size, ensuring context is preserved across chunks.

Next, I created a vector store using the Milvus vector database. For this, I used OpenAIEmbeddings to convert the text chunks into high-dimensional embedding vectors. The vector store is initialized with different index types (FLAT, IVF_FLAT, and HNSW) to compare performance across search algorithms. I added the embedded documents into Milvus and performed a similarity search to retrieve the top k most relevant chunks for a user query. The retrieval process also outputs the retrieval time and average similarity score as performance metrics.

To enhance the quality of the retrieved documents, I applied Maximum Marginal Relevance (MMR) reranking, which balances relevance and diversity using a parameter lambda_mult. This is done by converting the Milvus store into a retriever using MMR search, fetching a larger number of documents (fetch_k) and selecting the most diverse yet relevant subset (k).

Using the reranked documents, I then passed the query to a RetrievalQA chain with an OpenAI LLM (temperature set to 0 for deterministic responses). The model generated a natural language answer based on the retrieved context. Finally, the generated answer was saved in a .docx file using the python-docx library, with separate output files for each index type to support comparison.

Overall, this assignment helped me understand and implement each stage of a RAG system: document preprocessing, vectorization, semantic search, reranking, LLM answering, and result saving—demonstrating an end-to-end approach to building intelligent question-answering systems from unstructured documents.
