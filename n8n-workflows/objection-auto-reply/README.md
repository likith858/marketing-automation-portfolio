# Objection Auto-Reply

**What it does:** a short form asks what's stopping the student from joining. A Switch node routes each answer (fees too high, no time, not sure it works, will join later) to its own personalised reply.

**Flow:** Form Trigger > Switch (4 rules) > Price / Time / Trust / Delay Reply > Merge

**Lesson learned:** each Switch output must go to its own action; joining them before the reply sends every reply to everyone.

**Business value:** every hesitant lead gets an answer to their exact objection within seconds.
