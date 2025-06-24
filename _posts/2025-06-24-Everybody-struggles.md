## Everybody Struggles
<img src = "/images/obstacle.jpg">
# The Imposter Creeps In
"Everybody Struggles" — the title of this blog post resonates deeply with my experience as an Outreachy intern working on the Servo project. A month into my internship, I’ve felt the highs of confidence and the lows of self-doubt. The imposter syndrome that creeps in during challenging moments is real, but so is the growth that comes from pushing through. This journey has been a mix of excitement, obstacles, and profound learning, as I navigate Rust, Servo’s devtool, and the open-source world.
Riding the Wave of Confidence
My first week at Servo was electric. I dove into my project—improving the network monitor to align with Firefox’s DevTools—with excessive enthusiasm. I was optimistic, maybe even a touch overconfident, thinking I could breeze through my tasks in a month and a half. Everything clicked: I researched about how browsers work, what a browser engine is and what an embeddable browser is. This got me started, and I submitted my first pull request [refactored handle_network_event fn to use BrowsingContexActor]( https://github.com/servo/servo/commit/e1ec650cfe4007d6af280f7800a976c62f0ad903). The code flowed, the builds passed, and I felt like I was in sync with the project. It was a honeymoon phase, and I was riding the wave.




# Reality Hits
Then came the second week, and reality began to unfold. The initial flow met a stronger current—tasks became more complex, and the codebase revealed its depth. I was working on aligning Servo’s network monitor logs with Firefox’s format [https://github.com/servo/servo/issues/37479](issue #37479), which required restructuring JSON serialization to use a flat resourceUpdates object instead of categorized updates. The decline in my confidence wasn’t immediate, but I started to feel the weight of Rust’s strict compiler and the intricacies of Servo’s DevTools protocol.
One major hurdle was resolving Git conflicts in my local repository. My PR got stalled due to upstream changes, and I struggled to understand how to rebase properly. Terms like nit, lint, and commit sign-offs—common in open-source workflows—were initially confusing. A nit (short for nitpick) refers to a minor suggestion in a code review, like fixing a typo or formatting. Lint refers to static code analysis tools (e.g., test-tidy in Servo) that catch style or potential errors. Commit sign-offs were new to me; they involve adding a Signed-off-by line to commits to confirm agreement with the project’s contribution terms. These terms felt like a foreign language at first.






# Obstacle is the Way
By the fourth week, I could fully relate to “Everybody Struggles.” The turning point came when I hit a wall. I needed to refactor NetworkEventActor to merge properties like waitingTime, and responseContent into a single JSON object, matching Firefox’s DevTools logs. Rust’s borrow checker threw errors that seemed cryptic, and my initial fear of debugging them made me doubt my abilities. I’d naively hoped my code would run flawlessly on the first try—not because I thought I was a genius, but because I dreaded the time it would take to decipher and fix errors.
A particularly tough moment was resolving Git rebase conflicts. My local branch diverged from the upstream repository, stalling my PR. I spent hours wrestling with commands like git rebase and git push --force, terrified of losing my work. But with my mentor’s patient guidance and some sheer determination, I pulled it off. Each resolved conflict and fixed error felt like a small victory, building my confidence in Git and Rust.
Looking back, these struggles have been profoundly transformative. As the Stoics say, “The obstacle is the way.” Each challenge pushed me to grow. I’m no longer intimidated by Rust’s error logs, I learned to scope borrows correctly to satisfy the borrow checker when restructuring NetworkEventActor to use Option-wrapped structs like ResponseContentMsg.
My Git and GitHub skills have also leveled up. I now understand how to rebase branches, resolve conflicts, and use test-tidy to catch linting issues before submitting PRs. The process of signing off commits (git commit -s) has become second nature, ensuring my contributions comply with Servo’s guidelines. The open-source community’s feedback, like addressing nits in code reviews, taught me to value constructive criticism.





# Looking Forward
I’m eager to see where this journey takes me. The struggles have tested my limits in a profoundly needed way, and each small victory has built my confidence. I’m excited to tackle remaining tasks.
Everybody struggles, but those struggles are the building blocks for growth. I’m grateful for my mentor’s guidance, the Servo community’s support, and the Outreachy program for giving me this opportunity to learn, fail, and grow. Here’s to more challenges and the skills they’ll unlock!
