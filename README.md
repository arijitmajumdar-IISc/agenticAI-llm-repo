LLM output is plain text by default. Output parsers turn the plain text into structured format, so the downstream code can rely on the types instead of taking the hedache of fragile text parsing. Output parsers also have capability to format instructions so our model knows exactly what to do.

In this repo, I plugged and played with important output parsers available in langchain document. Codes are quite simple (no complex theory here, it is for my own learning and creating the base), but it has a holistic view of "how to use". Along with that, I have tried to provide a basic idea on how to use templates for string/normal prompt, chat and message. 

Following parsers are used here:

**String**:  Output parser that parses the LLM result into string format.

**JSON**: Output parser that parses the LLM result into JSON format.

**XML**: Output parser that parses the LLM result into XML format.

**CSV**: Output parser that parses the LLM result into CSV format.

**Output Fixing parser**: Wraps another output parser. If the output has some parsing error, it passes the error and the bad output to LLM and tell it to fix it.

**RetryWithError**: Along with Output fixing parser, it will also send the original instructions.

**Pydantic**: Takes a user defined Pydantic model and returns data in that format.

**YAML**: Takes user defined Pydantic model and returns data in that format. Uses YAML to encode it.

**PandasDataframe**: Useful for doing operations with Pandas dataframe.

**Datetime**: Parses response into a datetime string.

**Structured**: Returns structured information.

**All parsers will be attempted mostly with simple prompt template and Chat prompt template.**
