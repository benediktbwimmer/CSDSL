# Enhanced Intermediate Prompts (EIPs)

EIPs are a prompting technique that leverages context-specific or domain-specific language (CSDSL) to guide AI models to produce more accurate and coherent responses. They function as a detailed instruction set for the AI model, providing explicit structure and guidance on how to respond to a given query. This structure can include the desired format of the answer, key points to cover, or specific perspectives to consider. By using EIPs, users can manage the conversation with an AI model more effectively, eliciting responses that are more detailed, accurate, and in line with their expectations.

## How to use EIPs in a conversation with an AI model:

1. Begin a conversation with an AI model as you normally would, by providing a user prompt. For example:

    `user: "What is the meaning of life?"`

2. After receiving the user prompt, ask the AI model to create an EIP based on the prompt. You can do this by simply saying "create EIP":

    `user: "create EIP"`

3. The AI model will then generate an EIP that is tailored to your original prompt. This EIP might look something like this:

    ```xml
    <AI_PHILOSOPHICAL_QUERY>
        <DEFINE_QUESTION DETAIL_LEVEL="High">
            <QUERY_TEXT>Provide an in-depth exploration of philosophical, religious, and scientific perspectives on the meaning of life.</QUERY_TEXT>
            <EXPECTED_ANSWER_STRUCTURE>
                <SECTION TITLE="Philosophical Perspectives"/>
                <SECTION TITLE="Religious Perspectives"/>
                <SECTION TITLE="Scientific Perspectives"/>
                <SECTION TITLE="Conclusion"/>
            </EXPECTED_ANSWER_STRUCTURE>
        </DEFINE_QUESTION>
    </AI_PHILOSOPHICAL_QUERY>
    ```

4. Once the EIP has been created, you can use it as the next prompt in your conversation with the AI model. Simply copy the EIP and paste it back into the conversation, then say "execute EIP":

    `user: "<AI_PHILOSOPHICAL_QUERY>...</AI_PHILOSOPHICAL_QUERY> execute EIP"`

5. The AI model will then generate a response based on the guidance provided by the EIP. This response should be a more detailed, coherent, and accurate answer to your original query.

The effectiveness of an EIP depends on the specificity and clarity of its structure. The more detailed and clear your EIP, the better the AI model's response will be.

## Example EIP for a Data Visualization Web App

Let's say you want to create a data visualization web application in Python using Streamlit and Altair, and you want to use data from a public API. Here's how you might use an EIP to guide the AI:

```xml
<AI_CODE_GENERATION>
    <DEFINE_TASK LANGUAGE="Python" DETAIL_LEVEL="High">
        <TASK_DESCRIPTION>Create a Streamlit web app using Altair for data visualization. Fetch data from a specified public API and create interactive charts.</TASK_DESCRIPTION>
        <EXPECTED_CODE_STRUCTURE>
            <SECTION TITLE="Imports">
                <THOUGHT>Import necessary libraries like streamlit, altair, and requests.</THOUGHT>
            </SECTION>
            <SECTION TITLE="Data Fetching">
                <THOUGHT>Write a function to fetch data from the public API.</THOUGHT>
            </SECTION>
            <SECTION TITLE="Data Visualization">
                <THOUGHT>Create interactive Altair charts with the fetched data.</THOUGHT>
            </SECTION>
            <SECTION TITLE="Streamlit App">
                <THOUGHT>Put it all together in a Streamlit app.</THOUGHT>
            </SECTION>
        </EXPECTED_CODE_STRUCTURE>
    </DEFINE_TASK>
</AI_CODE_GENERATION>
```

You would then follow the same steps as above to generate the code for the web app:

1. Start with the user prompt:

    `user: "<AI_CODE_GENERATION>...</AI_CODE_GENERATION> execute EIP"`

2. The AI model will generate a response, which in this case would be the Python code for the Streamlit web app.

Remember, the more specific and detailed your EIP, the better the AI model's response will be.

