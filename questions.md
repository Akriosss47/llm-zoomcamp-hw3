Run both 1_chat_without_rag.yaml and 2_chat_with_rag.yaml in the Kestra UI. Read the execution logs for each.

The non-RAG response about Kestra 1.1 features is best described as:

Vague, generic, or fabricated — the model guesses from training data


Question 3: Token usage — short summary
Run 4_simple_agent.yaml with summary_length = short (leave the other inputs as defaults).

Open the execution logs and find the token usage logged by the log_token_usage task.

What is the approximate output token count for multilingual_agent?
Answer:63

Question 4: Token usage — long summary
Run 4_simple_agent.yaml again with summary_length = long.

Compare the multilingual_agent output token count to your result from Question 3. Roughly how many times more output tokens does the long summary use?
Answer:182

Question 5: Modifying a flow
Open 4_simple_agent.yaml in the Kestra flow editor. Find the english_brevity task and change its prompt from asking for exactly 1 sentence to asking for exactly 3 sentences.

Save the flow, then run it with summary_length = long.

Compare the english_brevity output token count to the original 1-sentence version (also with summary_length = long). How do they compare?
Multilingual Agent:
- Input tokens: 282
- Output tokens: 184
- Total tokens: 466
English Brevity Agent:
- Input tokens: 199
- Output tokens: 86
- Total tokens: 285
