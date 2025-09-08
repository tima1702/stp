# Получение API ключей

Если у вас по каким-то причинам не работает или плохо работает Ollama можете использовать бесплатные API ключи сервиса [OpenRouter](https://openrouter.ai)

## Последовательность действий

1. Зарегистрироваться на сайте https://openrouter.ai/
2. Создать [API Ключ](https://openrouter.ai/settings/keys)
3. Выбрать LLM с [бесплатным использованием](https://openrouter.ai/models?max_price=0) 

## Пример запроса к [qwen/qwen3-coder:free](https://openrouter.ai/qwen/qwen3-coder:free)

```bash
curl https://openrouter.ai/api/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $OPENROUTER_API_KEY" \
  -d '{
    "model": "qwen/qwen3-coder:free",
    "messages": [
      {
        "role": "user",
        "content": "What is the meaning of life?"
      }
    ]
  }'
```
