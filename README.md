# mobile-ui-design-generator
## 1. Overview
This project aims to develop a mobile UI generator using Stable Diffusion and GPT-2 within a Google Colab environment. The application takes a user's text query as input and generates a corresponding UI design image.

## 2. Model Training
### 2.1 GPT-2 for Prompt Generation
Pre-trained Model: We utilize a pre-trained GPT-2 model from Hugging Face Transformers (gpt2). No specific training was performed for this project; the model is used as-is for generating prompts based on user input.
Usage: GPT-2 takes a user's query as input and generates a more detailed prompt that can be used as input for Stable Diffusion.
### 2.2 Stable Diffusion for Image Generation
Pre-trained Model: We employ a pre-trained Stable Diffusion model from Hugging Face Diffusers (CompVis/stable-diffusion-v1-4). No further training is conducted within this project.
Usage: Stable Diffusion receives the prompt generated by GPT-2 (or directly from the user) and generates the UI design image based on it.
## 3. Application Development
### 3.1 Core Functionality
Prompt Generation: The application uses the pre-trained GPT-2 model to generate a detailed prompt from the user's input.
Image Generation: The generated prompt is then fed into the pre-trained Stable Diffusion model to create a UI design image.
Output: The generated image is displayed to the user and saved as a PNG file.
### 3.2 Gradio Interface
Interactive UI: A Gradio interface is integrated into the application to provide an interactive way for users to input their queries and view the generated UI designs.
## 4. Performance Evaluation
### 4.1 Prompt Accuracy
ROUGE Score: The ROUGE (Recall-Oriented Understudy for Gisting Evaluation) score is used to evaluate the accuracy of the prompts generated by GPT-2. It compares the generated prompt to a reference prompt.
Implementation: The rouge-score library is used to calculate the ROUGE score.
### 4.2 Image Similarity
Structural Similarity Index (SSIM): SSIM is used to measure the structural similarity between the generated UI design and a reference UI image.
Mean Squared Error (MSE): MSE is calculated to quantify the difference in pixel values between the generated and reference images.
Implementation: The scikit-image library is used to compute SSIM and the formula for MSE is directly implemented.
## 5. Running the Application
### 5.1 Dependencies
Ensure you have Python 3.7 or higher installed.
Install the required libraries:
 
pip install -r requirements.txt
Use code with caution
### 5.2 Instructions
Clone the repository: git clone https://github.com/your-username/mobile-ui-generator.git
Open the notebook: Open the mobile-ui-generator.ipynb notebook in Google Colab.
Run the cells: Execute all the cells in the notebook to initialize the models and set up the application.
Provide input: Enter your mobile UI design request in the input field or through the Gradio interface.
View output: The generated UI design will be displayed and saved as ui_design.png.
Important Notes

The project relies on pre-trained models, so no separate training process is included.
Performance evaluations are provided with metrics, but dataset specifics are not detailed as they are not core to the current application.
This documentation is for inclusion in your GitHub repository. Please adapt it to fit your specific file structure.
