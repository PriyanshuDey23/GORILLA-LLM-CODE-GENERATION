# GORILLA LLM APP 🦍‍👤

## Overview
The **GORILLA LLM App** is a Streamlit-based application that interfaces with the GORILLA server to generate and execute Python code based on user-provided prompts. This app uses OpenAI's API structure to communicate with the GORILLA model and enables code execution directly within the app interface.

---

## Features
- **Prompt-based Code Generation**: Users can input a custom prompt to query the GORILLA server and receive a generated Python code snippet.
- **Model Selection**: Choose between different model options (‘gorilla-7b-hf-v1’ or ‘gorilla-mpt-7b-hf-v0’).
- **Generated Code Execution**: Automatically executes the generated code and displays the output or errors.
- **Interactive UI**: A user-friendly interface built with Streamlit, featuring real-time responses and code previews.

---

## How It Works
1. **Input Prompt**: Users enter a custom text prompt.
2. **Model Query**: The app queries the GORILLA server using the selected model.
3. **Code Extraction**: The generated response is parsed to extract the Python code.
4. **Code Execution**: The extracted code is saved to a file and executed, with the results displayed on the app.

---

## Requirements
### Software and Libraries
- **Python 3.8+**
- **Streamlit**
- **OpenAI Python Client**

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd gorilla-llm-app
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

### File Structure
- `app.py`: Main application script.
- `requirements.txt`: List of dependencies.

---

## Usage
1. **Launch the App**:
   Run the app in your browser by executing the `streamlit run app.py` command.

2. **Enter Prompt**:
   - Input a text prompt into the text area.
   - Select a model option.

3. **Generate and Execute Code**:
   - Click **Gorilla Magic** to generate the Python code.
   - View the extracted and executed code output in real-time.

4. **View Results**:
   - Check the execution output or error messages directly within the app.

---

## Key Functions
### `get_gorilla_response(prompt, model)`
- Queries the GORILLA server with the given prompt and model.
- Returns the generated response.

### `extract_code_from_output(output)`
- Parses the GORILLA server’s output to extract Python code from the response.

### `run_generated_code(file_path)`
- Executes the extracted code using a Python subprocess and displays the output/errors in the app.

---

## Configuration
### OpenAI API Setup
- The OpenAI API key is not used in this application but remains a placeholder (`"EMPTY"`).
- The base URL for the GORILLA server is hardcoded as:
  ```python
  openai.api_base = "http://zanino.millennium.berkeley.edu:8000/v1"
  ```

### Page Layout
The Streamlit page layout is configured as wide for an enhanced user experience:
```python
st.set_page_config(layout="wide")
```

---

## Limitations
- **API Key**: The OpenAI API key is set to "EMPTY" and not functional for querying OpenAI endpoints.
- **Error Handling**: Limited error-handling mechanisms are implemented for server communication and code execution.

---

## Future Improvements
- Enhance error handling and debugging features.
- Add support for additional model options and configurations.
- Implement secure handling of API keys and environment variables.
- Improve UI for displaying multiline code snippets.

---

## License
This project is released under the MIT License.

---

