# GORILLA LLM Code Generation 🦍‍🕵️

This project provides a Streamlit-based interface for interacting with the GORILLA LLM (Large Language Model). Users can input a prompt, select a model, and generate Python code based on the prompt. The generated code can then be executed directly within the application.

---

## Features

- **Interactive Prompt Input**: Users can provide text prompts to query the GORILLA LLM server.
- **Model Selection**: Supports multiple model options, such as `gorilla-7b-hf-v1` and `gorilla-mpt-7b-hf-v0`.
- **Code Extraction**: Extracts Python code snippets from the model's response.
- **Code Execution**: Automatically runs the generated Python code and displays its output or errors.
- **Streamlit Interface**: A user-friendly web interface with features like text areas, dropdowns, and result displays.

---

## Requirements

### Python Libraries
- `openai==0.28`
- `streamlit`
- `transformers`
- `torch`
- `pandas`
- `numpy`

Install these dependencies using:
```bash
pip install openai==0.28 streamlit transformers torch pandas numpy
```

### Additional Tools
- A Python interpreter must be installed on your system to execute generated code.

---

## Configuration

### GORILLA Server Configuration
The code interacts with a GORILLA server. Ensure that:
- The GORILLA server is running and accessible.
- Update the `openai.api_base` variable with the correct server address.

---

## How to Run

1. **Start the Streamlit Application**:
   Run the following command in your terminal:
   ```bash
   streamlit run app.py
   ```

2. **Provide Input in the Interface**:
   - Enter your prompt in the text area.
   - Select the desired model from the dropdown.
   - Click the "Gorilla Magic" button to generate code.

3. **View and Execute Code**:
   - The application displays the generated Python code.
   - The code is saved to a file and executed automatically.
   - View the output or any errors in the Streamlit interface.

---

## Code Structure

### Main Functions

1. **`get_gorilla_response(prompt, model)`**:
   - Sends the prompt to the selected GORILLA model and retrieves the response.

2. **`extract_code_from_output(output)`**:
   - Extracts the Python code from the GORILLA model's response.

3. **`run_generated_code(file_path)`**:
   - Executes the generated Python code and displays the output or errors in the Streamlit app.

4. **Streamlit Interface**:
   - Handles user inputs, calls backend functions, and displays results.

---


---

## Notes

- Ensure the GORILLA server is running and accessible for successful code generation.
- The `openai.api_key` variable is ignored in this implementation.
- The generated code is saved to files (`generated_code_gorilla_7b_hf_v1.py` or `generated_code_gorilla_mpt_7b_hf_v0.py`) in the current working directory.

---

## Troubleshooting

- **Connection Issues**:
  Ensure the `openai.api_base` URL is correct and the server is running.

- **Code Execution Errors**:
  Review the error message displayed in the Streamlit app. Fix the generated code if necessary.

---

## Future Enhancements

- Add support for more models and dynamic configuration.
- Improve error handling and user feedback.
- Save and manage multiple generated code files.

---

## License

This project is open-source and available for modification and redistribution under the MIT License.

