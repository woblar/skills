---
name: illustrate-a-topic
description: Research a topic and explain it in a hand-drawn pastel illustration. Use for the Illustrate a Topic workflow or when asked to illustrate a concept, mechanism, or comparison using one or more of its ten numbered layouts.
license: "MIT for instructions and configuration (see NOTICE.md)"
---

# Illustrate a Topic

Accept a topic or question and an optional layout theme number or name. Ask for the topic if it is missing. If the theme is omitted, choose one that serves the explanation and name it. A subject motif can guide the visuals while the theme governs the composition. Honour the requested order for a subset and use canonical order for all ten. Default to a curious nontechnical adult, plain English, and the pastel whiteboard style. Adapt the audience, depth, language, aspect ratio, and references to the request.

1. **Research the explanation.** Identify the main learning question and any necessary product, model, or version. Browse authoritative sources for new topics or use authoritative sources supplied by the user if browsing is unavailable. Verify the terminology, mechanism, and relevant limitations or safety details. Use the facts to write a brief with the core answer, 3–6 supporting facts, a concrete example, any important caveat, and source links. Reuse the brief across a batch and verify any claims a layout introduces. Treat example images as visual references only.
2. **Choose a composition.** Read [the ten layouts](references/themes.md) and [style and quality](references/style-and-quality.md). Inspect a relevant bundled example for the selected layout if the image and inspection tool are available. Use the written guidance when examples are unavailable. For a batch, sample one or two layouts and use the written rules for the rest. Preserve the requested composition. Each image in a batch should explain the topic on its own.
3. **Storyboard.** Use the [prompt template](references/prompt-template.md) to specify the visual relationships, exact title, short labels, and takeaway. Keep the storyboard and prompt as the deliverable when the user asks for planning only.
4. **Generate.** Use the host’s image-generation tool when available. Use an external generator or a CLI only when explicitly requested or confirmed. Follow the tool’s conventions for references and output. Attach inspected style or composition references when supported. Otherwise describe their relevant characteristics in the prompt. Generate one image per requested layout. If image generation is unavailable, explain that and deliver the researched storyboard and prompt.
5. **Inspect and deliver.** Check the composition, text, arrows, causal relationships, and object consistency. Revise material defects and inspect the revision. Keep engineering and safety-sensitive illustrations conceptual. Use verified deterministic tools for exact charts or schematics. Return the image with the layout name, a brief takeaway, and source links outside the artwork by default. For a long batch, report progress and identify any layouts you could not finish.

> Explain how a heat pump works using theme 4 for a nontechnical homeowner.

> Explain photosynthesis with the four-frame comic and bold takeaway poster for a 12-year-old.
