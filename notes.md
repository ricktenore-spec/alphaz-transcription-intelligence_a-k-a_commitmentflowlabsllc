notes.md:
Notes
2025-05 — Initial Research
Exploring the intersection of transcription accuracy and psychological signal detection. Most transcription APIs handle the speech-to-text well, but the real value is in what happens after — detecting tone shifts, hesitation patterns, and verbal compliance without psychological commitment.
Key observations so far:
Deepgram handles real-time streaming well for call scenarios
OpenAI's structured output mode is useful for extracting specific behavioral signals
Embeddings could cluster similar conversation moments across multiple calls
The hard part is not transcription — it's interpretation
Architecture Thinking
Considering a pipeline approach:
Audio in → Deepgram transcription
Transcript → OpenAI structured analysis
Analysis → pattern detection (commitment, disengagement, trajectory)
Output → actionable coaching insights
Open Questions
What's the minimum transcript length needed for reliable signal detection?
How do we handle overlapping speech in two-party calls?
Can we detect disengagement from text alone, or do we need audio features (tone, pace)?
roadmap.md:
Roadmap
Phase 1 — Foundation (Current)
Set up Deepgram integration for audio transcription
Build basic OpenAI prompt for conversation analysis
Create simple Streamlit interface for reviewing results
Test with sample mortgage sales conversations
Phase 2 — Signal Detection
Implement commitment signal detection
Implement disengagement pattern detection (momentum decay, fake agreement, decision fatigue)
Build trajectory prediction ("what happens next")
Add intervention suggestions ("what changes the outcome")
Phase 3 — Pattern Library
Cluster similar conversation moments using embeddings
Build a library of common disengagement patterns
Create coaching templates mapped to detected patterns
Phase 4 — Integration
Explore real-time analysis during live calls
Consider webhook-based architecture for production use
Evaluate scaling approaches for multi-tenant usage
Timeline
No fixed timeline. This is experimental and iterative.
