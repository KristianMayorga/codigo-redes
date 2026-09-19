# Codigo Redes — Validador de URLs

Aplicación de escritorio en **Python** (interfaz con **Tkinter**) que analiza una URL y estima si es potencialmente maliciosa.

## Cómo funciona

La función `validar_url` revisa, entre otras cosas:

- Que el esquema sea `https`
- Que el host no contenga `@`
- El código de respuesta HTTP y el `Content-Type`
- Señales sospechosas en el HTML de la respuesta (`location.href`, formularios)

Si alguna señal falla, la URL se marca como maliciosa en una ventana emergente de Tkinter.

## Dependencias

Gestionadas con **Poetry** (`pyproject.toml` / `poetry.lock`):

- `requests`

## Cómo ejecutarlo

```bash
poetry install
poetry run python main.py
```
