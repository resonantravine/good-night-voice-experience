# Good Night Voice Agent

A time-based voice UX case for bedtime disengagement.

Good Night explores how AI voice can help users move out of interaction before sleep. Instead of designing another assistant that responds more, explains more, or keeps the user engaged, this project tests voice personas, timing, silence, and fading UI as materials for designed withdrawal.

The project shifted from asking what the AI should say to asking when the AI is no longer needed to speak.

## Project Snapshot

| Area | Detail |
| --- | --- |
| Role | Product concept, voice UX, sound interaction design |
| Medium | Voice UI, TTS, sound design, interaction timing |
| Tools | Doubao TTS 2.0, ElevenLabs, Reaper, Figma |
| Prototype | Figma prototype, voice persona demos, public test agent |
| Focus | Designed withdrawal, persona-based comfort, low-stimulation interaction |

## Demo

Voice persona demos:

| Persona | Waveform video | Duration | Design role |
| --- | --- | ---: | --- |
| Mark / Release | [mark-waveform.mp4](https://github.com/resonantravine/good-night-voice-experience/releases/download/good-night-demo-assets-2026-06-19/mark-waveform.mp4) | 4:26 | Helps release emotional residue with a warmer, gradually slowing presence. |
| Alice / Disengage | [alice-waveform.mp4](https://github.com/resonantravine/good-night-voice-experience/releases/download/good-night-demo-assets-2026-06-19/alice-waveform.mp4) | 2:22 | Reduces participation through minimal, grounded language. |
| Marian / Settle | [marian-waveform.mp4](https://github.com/resonantravine/good-night-voice-experience/releases/download/good-night-demo-assets-2026-06-19/marian-waveform.mp4) | 1:16 | Creates stillness with sparse language and a soft closing cue. |

Prototype links:

- Release assets: [Good Night Voice Agent Demo Assets](https://github.com/resonantravine/good-night-voice-experience/releases/tag/good-night-demo-assets-2026-06-19)
- Existing public case site: [good-night-voice-experience](https://resonantravine.github.io/good-night-voice-experience/#/good-night)
- Figma prototype: [aged-shy-78989692.figma.site](https://aged-shy-78989692.figma.site)
- Public ElevenLabs test agent: [Talk to Good Night](https://elevenlabs.io/app/talk-to?agent_id=agent_2501krfhz1k1fnbaygh21mamqec9&branch_id=agtbrch_4001krfhz2mgfcs8kxd50dzdds0z)
- A/B timing comparison: [audio samples](assets/audio/ab/)

## Design Question

How can a voice agent help someone leave an interaction, rather than keep them engaged?

Most conversational products optimize for more response, more content, and more retention. Good Night tests the opposite direction: a voice interaction that becomes simpler, quieter, and less demanding over time.

## Interaction Model

```text
Arrival -> Unloading -> Slowing -> Fading -> Exit
```

| Stage | Interaction goal | Voice behavior |
| --- | --- | --- |
| Arrival | Let the user begin without effort. | Brief greeting, low demand, permission to do less. |
| Unloading | Receive a small amount of residue from the day. | One simple question at most; no analysis. |
| Slowing | Reduce cognitive and conversational load. | Shorter responses, fewer prompts, slower pacing. |
| Fading | Make silence acceptable. | Less language, no new topics, no pressure to continue. |
| Exit | Help the user stop interacting. | Warm closure, no reopening question. |

## Voice Persona System

Good Night is not a therapist, coach, productivity assistant, or emotional companion. The voice should feel calm and present, but it should not create dependency or invite the user into a long reflective conversation.

The persona system explores three useful tensions:

- **Warmth vs. distance:** supportive enough to feel safe, restrained enough to let the user leave.
- **Softness vs. clarity:** quiet enough for bedtime, clear enough not to feel uncomfortable or uncanny.
- **Presence vs. withdrawal:** present at the start, gradually less active over time.

See [docs/voice-persona-system.md](docs/voice-persona-system.md).

## Sound And Timing Design

The core design material is not only wording. Timing, silence, response length, and audio fade are part of the interaction model.

Design rules:

- Ask fewer questions as the session continues.
- Respond with less content than the user gives.
- Treat silence as a valid state.
- Move toward closure when the user says they are tired, sleepy, done, or says good night.
- Avoid stacked instructions; offer one small action at a time.
- Separate timing control from TTS generation when breath, pause, and spacing need precision.

See [docs/sound-and-timing.md](docs/sound-and-timing.md).

## Prototype Learning

Early feedback showed that sleep support is not one need. Some users wanted low-stimulation audio that helps them disengage, while others wanted responsive emotional security before sleep. Across those differences, the strongest direction was the withdrawal phase: fading sound, dimming UI, and explicit exit cues helped users understand that they were allowed to stop.

The main open challenge is synthetic voice quality. Several listeners reacted not to the interaction model itself, but to the AI tone. This makes voice authenticity and timing control central to the next iteration.

See [docs/user-feedback.md](docs/user-feedback.md).

## Case Visuals

- [Spatial sound design](assets/images/spatial-sound-design.png)
- [UI screen A](assets/images/ui-screen-a.png), [UI screen B](assets/images/ui-screen-b.png), [UI screen C](assets/images/ui-screen-c.png)
- [2x2 feedback map](assets/images/feedback-map-2x2.png)

## What This Demonstrates

- **Voice UX strategy:** designing for disengagement instead of retention.
- **Conversation restraint:** knowing when not to ask another question.
- **Persona boundaries:** avoiding therapy, coaching, dependency, or over-intimacy.
- **Timing and silence:** treating pacing, breath, and fade as interaction design, not decoration.
- **Prototype evaluation:** comparing persona demos by comfort, clarity, pacing, and exit behavior.

## Key Design Decisions

- The success metric is not session length. A successful session is one where the user stops interacting.
- Memory and emotional content should be used carefully, if at all. The agent should avoid sounding like it knows too much.
- The voice should reduce itself over time: shorter language, fewer prompts, softer closure.
- Audio and silence are part of the product behavior, not post-production polish.
- The final stage is not a conclusion. It is a disappearance: voice, UI, and prompts gradually withdraw.

## Project Structure

```text
docs/
  case-study.md             # portfolio case narrative
  interaction-model.md      # Arrival -> Unloading -> Slowing -> Fading -> Exit
  voice-persona-system.md   # persona boundaries and demo comparison
  sound-and-timing.md       # pacing, fade, silence, and exit logic
  user-feedback.md          # feedback notes and future evaluation plan
assets/
  audio/ab/                 # A/B timing comparison audio
  images/                   # case diagrams, UI screenshots, and feedback map
prototype/
  links.md                  # public prototype, Notion source, and agent links
```

## Related Work

This project pairs well with [AI Radio Agent](https://github.com/resonantravine/ai-radio-agent). AI Radio Agent focuses on audio content generation; Good Night focuses on voice interaction restraint, timing, and disengagement.

## License

MIT
