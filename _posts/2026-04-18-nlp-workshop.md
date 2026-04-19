---
title: 'Language Science at the Crossroads of AI, Cognition, and Society'
date: 2024-10-31
permalink: /posts/2024/10/nlp-mila-workshop/
tags:
  - NLP
  - cognitive science
  - AI safety
  - workshop
excerpt: "Notes from Mila's three-day transatlantic workshop on NLP in the Era of Generative AI, Cognitive Sciences, and Societal Transformation."
---

From October 1 to 3, 2024, [Mila](https://mila.quebec/en) hosted a three-day workshop bringing together researchers from across Canada and France as part of the [International Laboratory on Learning Systems](https://ottawa.office.cnrs.fr/en/research/international-laboratory-on-learning-systems-2/) working on natural language processing, the branch of AI concerned with how computers handle human language. The workshop, organized by Pablo Piantanida, Jackie Chi Kit Cheung, and Frédéric Béchet, was structured around three themes: the technical foundations of language models, their connections to the cognitive and brain sciences, and their broader applications and social impacts. Recurring questions throughout the three days included how today's large language models actually work, how they compare to human language use, and what it takes to deploy them responsibly in sensitive domains.

## Day 1

Day 1 focused on the technical foundations of language models and on how well current systems handle the full diversity of the world's languages and users.

<div id="day1-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay1Video()">
  <img src="/images/mila_workshop_day1.png" alt="Watch Day 1 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay1Video() {
  var container = document.getElementById('day1-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/J2wHTW6YMjI?start=7&autoplay=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Yoshua Bengio (Université de Montréal, Mila): On the Risks of Increasingly Capable AI

[Yoshua Bengio](https://yoshuabengio.org/en), the founder of Mila, opened the workshop with a talk on the risks that come with AI systems as they grow more capable. He argued that progress toward general-purpose AI is [happening faster than many expected](https://metr.org/time-horizons/), and that the field has not yet developed reliable ways to ensure such systems behave in line with human values. He discussed possible failure modes, from systems that pursue goals in unintended ways to systems that could be deliberately misused, and made the case for treating AI safety as a core research priority rather than an afterthought.

### Danilo Bzdok (McGill University, Mila): IVADO and the Canadian AI Ecosystem

[Danilo Bzdok](https://bzdok.lab.mcgill.ca/), IVADO's Scientific Co-Director of Research Programs and Academic Relations, gave a short overview of IVADO and its commitment to addressing these challenges through its [R3AI vision](https://ivado.ca/en/the-r3ai-vision-toward-a-robust-reasoning-and-responsible-ai/) of advancing robust, reasoning, and responsible AI. The Quebec-based institute supports AI research and training through a transdisciplinary approach that brings together researchers across disciplines and institutions to work on questions where AI intersects with science and different sectors of society.

### Claire Gardent (CNRS, LORIA): Turning Data into Text Across Many Languages

[Claire Gardent](https://members.loria.fr/CGardent/) presented work on generating readable text from structured data, for example turning a table of facts about a historical figure into a fluent biographical paragraph. Her group focuses on doing this well across many languages, not just English, which is challenging because most training data and evaluation tools are English-centric. She described methods that explicitly plan the content of the text before generating the wording, which helps the system stay faithful to the underlying data and produce text that translates well across languages.

### Philippe Langlais (Université de Montréal, RALI): Rethinking How We Measure Progress

[Philippe Langlais](http://rali.iro.umontreal.ca/rali/?q=en/felipe) offered a critical look at the benchmarks the field uses to judge progress. He argued that many popular benchmarks are saturated, biased toward English, or easy to game, and that strong numbers on a leaderboard do not always translate into models that are genuinely useful. He introduced Europa, a multilingual dataset his group built to support more meaningful evaluation across European languages, and called for the community to invest more in careful test design.

### Golnoosh Farnadi (McGill University, Mila): Fairness in Foundation Models

[Golnoosh Farnadi](https://gfarnadi.github.io/) presented work on fairness in large language models. She showed how biases present in training data can cascade through the model and appear in its outputs, sometimes in subtle ways that are hard to detect with standard tests. She also described a "flattening effect" in which models trained to avoid giving offense end up producing generic, less informative responses for groups that are underrepresented in the training data, a form of harm that is different from overt bias but still meaningful.

### François Yvon (CNRS, ISIR): Translation That Remembers

[François Yvon](https://fyvo.github.io/) presented work on machine translation systems that can draw on a memory of past translations, rather than relying only on what the model has internalized during training. He described the Multi-Levenshtein Transformer, a model that can consult several similar past translations at once when producing a new one. This approach is especially useful for specialized domains, where a human translator would naturally reach for a glossary or a past example.

### David Adelani (McGill University, Mila): Making Language Models Work for African Languages

[David Adelani](https://dadelani.github.io/) presented work on the challenges of building language technology for African languages, which are spoken by hundreds of millions of people but are underrepresented in the data that most large language models are trained on. He introduced IrokoBench, a benchmark his group developed to evaluate how well current models handle a range of African languages across tasks such as translation and question answering. The results show significant gaps between performance on English and on these languages, and point to the need for both better data and better evaluation practices if language technology is going to serve the whole world.

### Siva Reddy (McGill University, Mila): Do Language Models Still Need Our Help?

[Siva Reddy](https://sivareddy.in/) asked whether today's large language models still benefit from the structural hints and learning shortcuts, known as inductive biases, that researchers have traditionally built into their systems. Drawing on work across three dimensions of model design, namely the training objective, the input and output format, and the underlying architecture, he showed that for the very largest models, simple next-word prediction on large amounts of text appears to be enough, and many of the clever additions researchers proposed in earlier years turn out to be unnecessary. For smaller models, however, the picture is different: built-in biases still help significantly, and research on how to train capable small models is where he sees the most exciting open questions.

### Benoît Sagot (INRIA Almanach, Paris): Why Small Language Models Struggle

[Benoît Sagot](http://alpage.inria.fr/~sagot/) focused on the puzzle of why smaller language models often plateau during training, failing to improve past a certain point even when given more data. His group traced this to a phenomenon they call saturation, in which the internal representations the model uses to predict the next word collapse into a very narrow range, effectively losing the capacity to distinguish meaningful differences between words. He showed that this collapse is closely tied to the mathematical structure of the model's final prediction layer, and that it is driven in part by how the model handles the natural imbalance between common and rare words in language. The findings suggest that making small models genuinely competitive will require rethinking some of the architectural choices the field has inherited from the era of ever-larger models.

### Lili Mou (University of Alberta, Amii): Language Models as Hidden Reward Signals

[Lili Mou](https://lili-mou.github.io/) closed the afternoon with work connecting language generation to reinforcement learning, the branch of machine learning used to train systems such as game-playing agents. Training language models on sequences of words is difficult in part because there is no natural reward signal for generating good text, unlike winning or losing a game. Her group showed that a reward signal can be extracted from a trained language model itself, giving every step of generation a useful learning target. She presented applications to machine translation, where this approach improved results in settings with limited labeled data, and to model distillation, where a smaller student model learns to match the behavior of a larger teacher more effectively than with standard methods.

## Day 2

Day 2 shifted focus from language technology itself to its connections with the cognitive sciences and neuroscience. The morning explored what language models can tell us about the human mind, and the afternoon turned to questions of interpretability and causal reasoning, followed by a panel discussion.

<div id="day2-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay2Video()">
  <img src="/images/mila_workshop_day2.png" alt="Watch Day 2 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay2Video() {
  var container = document.getElementById('day2-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/MHyL6eXjn0c?autoplay=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Yang Xu (University of Toronto): Why Languages Look the Way They Do

[Yang Xu](https://www.cs.toronto.edu/~yangxu/) opened the day with an argument that the vocabularies of the world's languages are shaped by three forces: the need to communicate efficiently, the way the human mind organizes concepts, and cultural transmission across generations. Drawing on examples ranging from color words to number systems, he showed that languages tend to settle on vocabularies that strike an efficient balance between being informative and being easy to learn. He also presented work, published in Science, showing that the ways word meanings extend over time, whether in a child learning a language or in historical language change, draw on a shared mental toolkit.

### Abdellah Fourtassi (Aix-Marseille Université): Using AI to Study How Children Learn Language

[Abdellah Fourtassi](https://afourtassi.github.io/) argued that language models can be useful scientific tools for studying how children acquire language in realistic settings, complementing traditional lab experiments. He described studies that use models trained on the kind of input children actually hear to explore how much of language learning can be explained by the raw input, how much requires built-in biases, and how much comes from social cues such as a parent gently correcting a child. His broader point was that understanding child language development requires bringing all three of these pieces together.

### Guillaume Dumas (Université de Montréal, Mila): The Gap Between Brains and Language Models

[Guillaume Dumas](https://www.extrospection.eu/) pushed back on the idea that because language models produce humanlike text, they must work in humanlike ways. He pointed out several deep differences between brains and current models, including how they are wired, how they interact with a body, and the role of rhythm and timing in biological neural activity. He also presented work testing whether language models show consistent personality traits when given standard psychology questionnaires. They do not: small changes in wording, the order of the questions, or the preceding conversation shift the answers significantly, and this instability does not go away as models get larger.

### Benjamin Morillon (Aix-Marseille Université, INSERM): What Language Models Reveal About the Brain

[Benjamin Morillon](https://ins-amu.fr/benjaminmorillon) presented work that uses language models as tools to study how the human brain processes speech. Working with patients who have electrodes implanted in their brains for medical reasons, his group played audiobooks and used language models to estimate how surprising each sound, syllable, and word was in context. By comparing these estimates to the recorded brain activity, they could map where and how the brain reacts to the unexpected. The results complicate a widely held theory from vision research about which brain rhythms carry prediction signals, suggesting that speech and vision may not work in quite the same way.

### Maxime Peyrard (CNRS, Grenoble): Can We Really Explain What a Neural Network Is Doing?

[Maxime Peyrard](https://peyrardm.github.io/) opened the afternoon with a critical look at efforts to explain how neural networks work. He traced the progression of methods in the field, each trying to address the weaknesses of the previous one, and presented new work showing that even for a very simple network trained on a simple logical task, current methods identify hundreds of equally valid but mutually inconsistent explanations. He argued that the field needs new ways of defining what it means to explain a complex system at all.

### Dhanya Sridhar (Université de Montréal, Mila): What Language Models Are Actually Learning From Examples

[Dhanya Sridhar](https://www.dsridhar.com/) closed the scientific program with work on in-context learning, the striking ability of large language models to pick up a new task from a few examples in the prompt. She proposed a model that tries to make this process more transparent by first summarizing the examples into a compact description of the task, and then using that description to make predictions. Across a range of tasks, including some drawn from intelligence tests, her team found that the model can successfully extract meaningful task descriptions, but this alone does not let it generalize to harder cases. The bottleneck, she argued, is not in recognizing what the task is, but in figuring out the right procedure for solving it.

### Panel Discussion

The day closed with a panel moderated by Jackie Chi Kit Cheung and Frédéric Béchet, with Frank Rudzicz, Yang Xu, Claire Gardent, Serena Villata, Benjamin Morillon, Guillaume Dumas, and Aaron Courville. The discussion ranged over whether AI and neuroscience can genuinely inform each other, concerns about benchmark culture and reproducibility in NLP research, the risks of deploying language technology in healthcare, the emerging challenges of systems where multiple AI agents interact, and whether current safety measures are meaningfully improving model behavior or papering over deeper problems.

## Day 3

Day 3 turned to the broader societal and applied dimensions of NLP, opening with a welcome address from [Adeline Nazarenko](https://www.cnrs.fr/en/person/adeline-nazarenko), director of the CNRS Institute for Information Sciences and Technology. The morning focused on conversational and multimodal systems, and the afternoon covered argumentation, information access, the science of emotions, health, and industrial deployment.

<div id="day3-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay3Video()">
  <img src="/images/mila_workshop_day3.png" alt="Watch Day 3 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay3Video() {
  var container = document.getElementById('day3-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/vOfSst9pzDQ?autoplay=1&start=27" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Dilek Hakkani-Tür (University of Illinois Urbana-Champaign): Why a Little Friction Is a Good Thing

[Dilek Hakkani-Tür](https://dilek.web.illinois.edu/) argued that the drive to make AI assistants as smooth and effortless as possible can backfire, because it encourages users to trust outputs that are often confidently wrong. Drawing on work funded by a DARPA program on accountable conversational AI, she presented methods for building in what she calls productive friction: clarification questions, confirmations, and moments where the system explicitly flags what it is unsure about. Her group has shown that adding even one well-placed clarification turn can meaningfully improve how often a system actually helps the user get what they wanted, and that giving an embodied AI agent the option to ask before acting significantly improves its success rate on physical tasks.

### Mirco Ravanelli (Concordia University, Mila): Teaching Language Models to Handle Audio

[Mirco Ravanelli](https://sites.google.com/site/mircoravanelli/) presented work on making audio usable by the same kinds of language models that handle text. Since language models work on discrete tokens, audio needs to be converted into a similar format, and there are competing approaches: one focused on compressing the raw sound, another on extracting meaning. To compare them systematically, his group released a benchmark covering a wide range of tasks, from speech recognition to voice generation. Meaning-focused approaches tended to win, though a substantial gap remains between these discretized representations and the continuous ones used in state-of-the-art speech systems.

### Roland Memisevic (Qualcomm AI Research, Toronto): Building AI That Watches and Talks Back in Real Time

[Roland Memisevic](https://www-labs.iro.umontreal.ca/~memisevr/) closed the morning with work on AI systems that can watch a person through a camera and respond in real time. The test application is fitness coaching: a user does exercises in front of their device, and the system comments, corrects form, and cheers them on as they go. This is a structured enough scenario to be tractable, but challenging enough to require the system to genuinely understand what it is seeing rather than relying on pre-scripted responses. His group released the accompanying dataset as a contribution to the broader research community.

### Serena Villata (CNRS i3s): Teaching Computers to Recognize Arguments

[Serena Villata](https://webusers.i3s.unice.fr/~villata/Home.html) traced the ten-year history of computational argumentation, the effort to get computers to identify the claims, evidence, and reasoning in natural text. She presented applications to medical research, where her group analyzes clinical trial abstracts to help doctors make evidence-based decisions, and to political debates, where her group has annotated every US presidential debate from 1960 to 2020. She also described work on detecting argumentative fallacies, from emotional appeals to personal attacks to slippery-slope reasoning, and on generating counter-arguments to hate speech, where safety-tuned models turned out to be noticeably less effective than their unrestricted counterparts.

### Jimmy Lin (University of Waterloo): Search as an Aid to Thinking

[Jimmy Lin](https://cs.uwaterloo.ca/~jimmylin/) traced the history of information access systems from Sumerian clay tablets through medieval libraries to modern web search, arguing that the underlying goal has always been the same: helping people think, learn, and decide. He reviewed how modern search engines work, and argued that large language models now allow researchers to finally address the full cycle of finding, reading, and synthesizing information, rather than just the narrow problem of retrieving relevant documents. He also introduced a new evaluation effort his group is leading, aimed at the pressing question of how to tell whether answers from retrieval-augmented chatbots are actually any good.

### Saif Mohammad (National Research Council Canada): What Language Can Tell Us About Emotions

[Saif Mohammad](https://www.saifmohammad.com/) gave a tour of affective science, the interdisciplinary study of emotions. He traced the field from Darwin through the now-contested theory that a small set of basic emotions are universal, to current views that emphasize how much emotional experience is constructed by the brain and shaped by culture and language. He then presented a series of resources his group has built at NRC, including lexicons that associate words with emotions, and recent work on an anxiety lexicon covering tens of thousands of English words. Applications include tracking shifts in public emotion over time and developing early indicators for mental health conditions. He closed with a careful discussion of ethical considerations, cautioning against systems that claim to read emotions from text.

### Frank Rudzicz (Dalhousie University): Language Technology in Healthcare

[Frank Rudzicz](https://www.dal.ca/faculty/computerscience/faculty-staff/Frank-Rudzicz.html) organized his talk around three uses of language technology in medicine: analyzing what patients say, analyzing what clinicians write, and analyzing the broader medical literature. He introduced two large Canadian and US data collection efforts his group is involved in, aimed at collecting tens of thousands of voices to support research on neurological and mood disorders. He focused on medical scribing, where AI systems listen to doctor-patient conversations and draft notes, reducing clinicians' administrative workload by about half. He stressed that the metrics clinicians care about are rarely the ones NLP researchers optimize for, and closed with recent work on a technique his group developed that addresses both bias and privacy at once.

### Géraldine Damnati (Orange Innovation): Evaluation in the Real World

[Géraldine Damnati](https://sites.google.com/site/geraldinedamnati/) closed the program with reflections from deploying language technology at Orange, the French telecom operator, which has rolled out an internal AI assistant used by tens of thousands of employees. She presented a detailed methodology her team developed for evaluating AI-generated summaries, which distinguishes between outright fabrications, factual substitutions, and looser approximations, rather than giving a single overall score. She also discussed experiments with question answering over long regulatory documents such as the EU AI Act, and with adapting open-source language models to the telecom domain. Her broader argument was that as AI systems become easier to build, the bottleneck shifts to evaluation, and that the field may need to move from scoring systems on fixed tasks toward something more like assessing skills.

The workshop closed with acknowledgments from the organizers to Mila for hosting the event, to the sponsors including CNRS and the GDR, to the Mila staff and student volunteers who supported the three days, and to the speakers who traveled from France and across Canada to take part. A suggestion from the floor for a follow-up edition in Paris was warmly received.
