# FastAPI: High Performance, Easy to Learn, Fast to Code, Ready for Production

**FastAPI** is a modern, fast (high-performance), web framework for building APIs with Python 3.8+ based on standard Python type hints.

---

## What is FastAPI?

FastAPI is designed to make building APIs incredibly fast and robust. It bridges the gap between high performance (on par with NodeJS and Go, thanks to Starlette and Pydantic) and rapid developer productivity.

### Key Features
- **Fast:** Very high performance, on par with **NodeJS** and **Go**.
- **Fast to Code:** Increase the speed to develop features by roughly 200% to 300%.
- **Fewer Bugs:** Reduce about 40% of human (developer) induced errors.
- **Intuitive:** Great editor support. Completion everywhere. Less time debugging.
- **Easy:** Designed to be easy to use and learn. Less time reading docs.
- **Short:** Minimize code duplication. Each parameter declaration has multiple uses. Fewer bugs.
- **Robust:** Get production-ready code. With automatic interactive documentation.
- **Standards-based:** Based on (and fully compatible with) the open standards for APIs: **OpenAPI** (previously known as Swagger) and **JSON Schema**.

---

## Visualizing FastAPI Architecture

Below is a conceptual overview of how FastAPI leverages standard Python type hints to automatically generate data validation and interactive documentation.

![FastAPI Architecture Flow](https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=800&q=80)

---

## How It Can Be Used

FastAPI is versatile and can be used across various domains in software architecture:

1. **RESTful APIs:** Build robust endpoints supporting GET, POST, PUT, DELETE operations.
2. **Microservices:** Create lightweight, fast services that communicate efficiently in a distributed system.
3. **Data Science & Machine Learning:** Serve ML models rapidly by wrapping heavy libraries (like PyTorch, TensorFlow, or Scikit-Learn) inside async API endpoints.
4. **Real-time Applications:** Leverage WebSockets for real-time chat, notifications, or live data feeds.

### Interactive Documentation Preview

One of FastAPI's standout features is its built-in interactive Swagger UI generated automatically from your code.

![Interactive Swagger UI Example](https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=800&q=80)

---

## Quickstart Example

Here is a simple example of how easy it is to create a FastAPI application:

```python
from fastapi import FastAPI

app = FastAPI()


@app.get("/")
def read_root():
  return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: str | None = None):
  return {"item_id": item_id, "q": q}
```

### Running the Application

Run your app using Uvicorn:

```bash
uvicorn main:app --reload
```

Once running, navigate to `http://127.0.0.1:8000/docs` to explore your automatically generated interactive API documentation!


# Portfolio Example

See below to interact with the About section data for this portfolio.