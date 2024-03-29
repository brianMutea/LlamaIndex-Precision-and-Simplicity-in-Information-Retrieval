# LlamaIndex Precision and Simplicity in Information Retrieval

[See Notebook](https://github.com/brianMutea/LlamaIndex-Precision-and-Simplicity-in-Information-Retrieval/blob/main/LlamaIndex_Introduction_Precision_and_Simplicity_in_Information_Retrieval.ipynb)

#### Create a Storage Context to upload the specified topics(data) from Wikipedia to DeepLake
```Python
from llama_index.storage.storage_context import StorageContext
from llama_index import VectorStoreIndex

storage_context = StorageContext.from_defaults(vector_store = vector_store)
index = VectorStoreIndex.from_documents(
    docs, storage_context = storage_context
)
```

![uploading data to deeplake](https://github.com/brianMutea/LlamaIndex-Precision-and-Simplicity-in-Information-Retrieval/blob/main/Screenshot%20from%202024-02-07%2010-47-52.png)

#### Query

```Python
query_engine = index.as_query_engine()
response = query_engine.query("What does NLP stand for?")
print(response.response)
```

Result

```Python
NLP stands for Natural Language Processing.
```

[See Notebook](https://github.com/brianMutea/LlamaIndex-Precision-and-Simplicity-in-Information-Retrieval/blob/main/LlamaIndex_Introduction_Precision_and_Simplicity_in_Information_Retrieval.ipynb)
