# spacy-rust
Rust bindings for the spaCy Python NLP library.
## Motivation
I created this library because, at the time of development, there was no comprehensive Natural Language Processing (NLP) library available for Rust. My project heavily relied on spaCy's capabilities, and I wanted to maintain some level of integration with it while working in Rust. This led me to take a detour from my main project to develop these bindings, making it easier to leverage spaCy's powerful NLP features in Rust-based applications.
## Status
This project is currently a work in progress. Contributions and feedback are welcome!
## Example
The following example demonstrates how to perform sentence similarity using these bindings:
rustCopylet spacy = spacy::Module::init();
spacy.load("en_core_web_lg");
let pangram1 = spacy::nlp("With tenure, Suzie'd have all the more leisure for yachting, but her publications are no good.");
let pangram2 = spacy::nlp("Amazingly few discotheques provide jukeboxes.");
pangram1
  .call("similarity")
  .args(pangram2)
  .kwargs("")
  .invoke();
## Future Plans
As this project evolves, I aim to expand the bindings to cover more of spaCy's functionality, making it easier for Rust developers to incorporate advanced NLP capabilities into their projects without having to switch between languages or rely on external Python processes.
## Contributing
Contributions to improve and expand these bindings are greatly appreciated. Feel free to submit issues, feature requests, or pull requests to help make this library more robust and useful for the
