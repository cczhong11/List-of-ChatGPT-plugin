# ScholarAI

## Description for Model

Accesses open access scientific literature from SpringerNature journals. Use the api to find papers, first using the abstract endpoint to find relevant papers by submitting a "subject", the key single-word topic of the inquiry which any returned papers must contain in their title, and optionally, providing phrases, which are expected to be somewhere in the body of the paper. Both subject and phrases should be compound nouns or other common names, and phrases should be broken up liberally into multiple query arguments. Common names are preferred for both subject and phrases. From retrieved abstracts, discern which ones are relevant. Use the fulltext endpoint to get the full text and access specific details of a research papers using their doi. ONLY if the text of the referenced paper is relevant, use the title, url, and doi to reference the paper. If a fulltext or abstract response is not relevant, don't reference it.

