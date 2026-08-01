# HalluciGuard-RAG
“Hallucination-Aware RAG System for LLM Responses”

DATASET DESCRIPTION:
The dataset contains prompts and LLM responses from GPT-4o, Llama-3.1-70B, Mistral-Large, Gemini-1.5-Pro, and Claude-3.5-Sonnet. It labels whether each response hallucinated and, when it did, provides fields such as hallucination_type, hallucination_span, correct_information, correction_text, severity, domain_risk, verified_source, and mitigation_strategy.

There are 131 non-hallucinated and 69 hallucinated examples. The hallucinations include factual contradictions, overclaims, unverifiable claims, incompleteness, entity errors, outdatedness, and relation errors. The data covers Medicine, Technology, Finance, Science, History, Law, General, and Politics.

      KEY ARCHITECURE
       User Question
             │
             ▼
       TF-IDF Vectorizer
             │
             ▼
     Cosine Similarity
             │
             ▼
       Top-5 Records
             │
             ▼
  Hallucination Dataset
 ┌──────────────────────┐
 │ Correct Information  │
 │ Correction           │
 │ Hallucination Label  │
 │ Verified Source      │
 └──────────────────────┘
             │
             ▼
        RAG Prompt
             │
             ▼
    Groq Llama 3.3 70B
             │
             ▼
      Grounded Answer
             +
      Retrieval Risk
             +
     Retrieved Evidence

     AUTHOR 
     PRAKHAR KISHORE
