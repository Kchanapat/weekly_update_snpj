# UPDATE WEEK 3
**Work Done**
- Benchmark reference
  - **Benchmarking Retrieval-Augmented Generation for Medicine** : งานนี้สร้าง benchmark สำหรับ RAG ทางการแพทย์ (≈ 7,600 คำถาม) ใช้ evaluation แบบ domain-specific โดยเปรียบเทียบว่า retriever ดึงข้อมูลจากได้แม่นยำแค่ไหน ประเมินเฉพาะ accuracy ระดับ retrieval (ไม่ลึกถึง category-level แต่เน้น domain accuracy)
    - https://arxiv.org/abs/2402.13178?utm_source=chatgpt.com
  - **BigEarthNet-MM: A Large Scale Multi-Modal Multi-Label Benchmark Archive for Remote Sensing Image Classification and Retrieval** : ใช้การ retrieval เพื่อดึงภาพที่มี labels เหมือนกับภาพ query (multi-label retrieval) , วัด performance ด้วย metrics เช่น precision, recall, F1‑measure และ Hamming loss สำหรับแต่ละ label/class
    - https://arxiv.org/pdf/2105.07921
  - **Retrieval Augmented Generation Evaluation in the Era of Large Language Models: A Comprehensive Survey** : evaluation framework แบบ unified สำหรับระบบ RAG = ประเมินทั้ง retrieval(วัดคสม.ดึงเอกสารที่เกี่ยวข้องกับคำถาม ใช้ recall, Precision, nDCG) และ generation (วัดคุณภาพของข้อความที่ LLM สร้างจากบริบทที่ retrieve มา เช่น Faithfulness,Completeness, Fluency)
    - https://arxiv.org/html/2504.14891v1#S4
-  Report Chapter 3 : qdrant vector store
   - Qdrant is a high-performance vector database designed specifically for efficient similarity and semantic search on large-scale, high-dimensional vector data. Its core search algorithm is based on Hierarchical Navigable Small World graphs (HNSW), which enable fast approximate nearest neighbor search with both high accuracy and low latency. This design makes Qdrant suitable for AI and machine learning applications that require rapid, precise retrieval in vector spaces.
   - the foundational HNSW algorithm implemented in Qdrant is well-established in the literature for enabling efficient nearest neighbor search in high-dimensional spaces (Malkov & Yashunin, 2018). Furthermore, Qdrant’s enhancements for payload filtering and scalable vector storage have been documented in their technical blog posts and white papers, which explain the practical application of these techniques in production systems.
   - References: https://arxiv.org/pdf/1603.09320
    
**Future work**
- report
  - multiagent
  - langgraph
  - question categorization
  - llm for classify question
  - llm for clarify question
  - llm for check out of domain question
  - Hybrid search
  - metadata filtering https://medium.com/@piash.tanjin/optimizing-rag-systems-query-classification-with-metadata-vector-search-2540401b9601
  - qdrant vector store
  - together ai api
  - llm for annotate chunk category
