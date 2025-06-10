I just broke Claude Code
engineers I think I just broke Claude
Code the best agent coding tool in the
game check this out and you tell me the
amount of value you can create in a
single prompt is incredible the amount
of value you can create in two prompts
is insanely mindblowing and not well
understood let me show you exactly what
I mean here I'm running a clawed code
infinite agentic loop now what does that
mean and what does that look like inside
of this five directory codebase I'm
generating infinite self-contained UIs
that self-improve on each set how is
this possible if I open up go into
commands you can see I have this
infinite.md prompt that's fueling this
claw code agent that's fired off five
sub agents you can see them all working
here live right now this one just wrote
1,000 lines we have another thousand
lines here one tool use three one two
and you can see here this is wave two
with five agents in parallel and more
are getting queued up right now you can
see it just finished wave two how can
just two prompts make Cloud Code run
forever you can see wave 3 is getting
set up right now iterations 16 through
20 if we scroll down here you can see a
new set of iterations loaded up check
out this task list right this is going
to just keep running back to the
question how is this possible this is
Infinite Agentic Loop
enabled by an infinite agentic
loop this powerful pattern is fueled by
just two prompts it's fueled by the
infinite prompt that we're going to get
into in just a second and of course your
spec your plan your PRD so if we open
this up a little bit you can see here I
have just three specs where we're
inventing some new UIs i have three
versions of them let's go ahead and kick
off another infinite agentic loop like
this and while it's dedicating work to
multiple sub agents for us we can talk
about how you can use this to generate a
virtually unlimited set of solutions for
a specific problem i'll create a new
terminal instance let's fire up cloud
code here and let's update the model i
want to fire this off on Opus very
clearly state-of-the-art model and then
we'll use the infinite custom slash
command here i'll type slashinfinite and
you can see here we have the infinite
agentic loop command i'll hit tab here
and now we need to pass in a few
variables into this so the first
parameter is the plan we want to fire
off i'm going to go ahead copy this get
the path to this paste it in here you
can see we're still running in the
background right agent 16 through 20
still running here it takes a new
directory so you can see our first agent
is operating in the source directory
let's set this directory to
source_infinite and then lastly it takes
Fire off a new wave of agents
a count or the information dense keyword
infinite we're going to of course pass
in infinite so we're going to kick this
off and now we're going to have two
agents running in parallel and so we can
see here our second infinite agentic
loop is starting to fire off here so if
I close this and open up the second
directory you can see that got created
here in our plan you can see cloud code
writing up this plan for infinite
generation we need to dive into the
prompt this is the most important thing
it's the pattern here that's so valuable
let's go ahead and dive in here and
understand how this infinite agentic
loop works with our two prompt system
and then let's talk about how this
breaks down if you've been using
longunning cloud code jobs you already
know exactly how this breaks there's a
natural limit here that we're starting
to bump into over and over and over and
it completely breaks this infinite
agentic loop workflow let's start with
the infinite prompt so we have our
initial command and then we have a
really important part of this the
variables with cloud code custom/comands
you can pass in arguments like this and
they'll be placed in position our first
argument gets replaced with spec and
then we get infinite source and then we
get infinite so this gets replaced and
then we can use these variables
throughout this prompt and the cloud 4
series is smart enough to know that it
should replace the variables we placed
in here with the actual variables passed
in right so you can see the spec file
throughout this prompt and you can see
the output directory as well then we
have count which is going to be one to n
or of course infinite you can see here
in this first step of the infinite
agentic loop prompt we're reading the
spec file this is a really interesting
pattern we're treating prompts right our
specs as first class citizens that can
be passed in to other prompts okay this
is a really powerful technique there's a
lot of value here that's untapped we
explored this a little bit in our
parallel agent decoding with git work
trees video we put out a couple weeks
ago what we're doing here is a little
different because we're running
infinitely and we're generating a single
file although to be completely clear you
know we could rewrite this prompt to
generate any set of files so we have
argument parsing our agent is going to
first read the spec file to understand
what's going on then it's going to
understand where it's going to output
all these files then it's going to fire
off parallel agents in groups of five
this is going to speed up the output of
our agent our first round files have
already been created for that infinite
loop and then this is really important
we're actually specifying what each sub
aent receives okay okay so it's getting
the spec it's getting the directory it's
getting its iteration number right you
can see they all have their own
iteration number and it's getting their
uniqueness directive right we want these
all to be unique we want each example to
grow on each other this is really cool
so here we're actually passing in a
prompt for our sub aents so that's
what's getting written out here right
this is a concise prompt for the sub
aent and then we have you know phase
five we're just kind of continuing down
the line infinite cycle and then I have
this line in here i'm not 100% sure if
this works i don't know if Claude can
see the end of its context window but it
seems to work okay evaluate context
capacity remaining if sufficient
continue with next wave if approaching
limits complete and finalize right so
this is where this pattern completely
breaks clog code you can't keep running
this it's going to hit the context
window of course we don't actually have
infinite context windows this will
generate you know some 20 30 files or
sets um depending on your setup all
right all right so then we're going to
just continue along the lines here there
are some details at the bottom here not
all this matters as you can see here I
am writing these prompts now with agents
we're entering this interesting zone
where you want to be writing prompts
that write the prompts for you you can
see here you know both of our lists here
are continuing to expand we now have 10
hybrid UIs inside of Source Infinite
let's go ahead and actually look at what
the heck is getting generated here right
you know just to briefly describe the
prompt that we're passing in right so we
have our spec file that we're passing in
to our infinite agentic loop prompt
we're saying invent new UI v3 and what
we're doing here is we're creating
uniquely themed UI components that
combines multiple existing UIs into one
elegant solution okay and that's that's
basically it that's a key idea of what
we're doing here and I'm using UI as a
example just like with our parallel
agent decoding video with git work trees
ui is just the simplest way to show off
a powerful pattern like this you know
we're specifying that naming scheme here
with the iteration and then we have a
kind of rough HTML structure that's all
Reviewing the Claude 4 Opus UIs
self-contained into a single file so
let's go and open this up let's see what
this looks like right so if we open up a
terminal here and we get the path to one
of these files we can say uh Chrome and
then open up one of these files check
this out neural implant
registry um very interesting this is a
classified database access terminal very
clearly it's just a table right so this
is kind of interesting it's got a really
cool unique theme to it let's see what
we can do here so we can search nice
echo cerebra max okay great so we can
search across columns we can sort that
looks great status filters active risk
level here i'm constantly impressed with
the caliber of code that the Cloud 4
series is producing now it's just kind
of mind-blowing that not only was it
able to launch off this it did five
versions at the same time right you and
I we really have access to premium
compute that we can now scale up
infinitely uh with this pattern right
very cool UI let's go on to another
example right adaptive flow UI liquid
metal so obviously some UI issues here
but this is just a simple UI it looks
like nothing special oh interesting that
just adapted very interesting i did not
expect that so it's actually creating
additional UI here based on what we type
in oh I like this kind of error state
look at this it's errored right here
right this is not a true email address
and we do get email autocomplete here
very cool and you can see we also have a
progress bar here at the bottom in
particular I like this like active state
let's go ahead and look at another UI
that was generated for us again this is
all happening in parallel in the
background you know this compute is
solving this problem for us at scale
creating many many versions right what
do we have some 20 um yeah 50 versions
now with two parallel infinite agenda
coding agents this is crazy right this
it's really cool very powerful obviously
the real trick with this pattern is
going to be to pointing it at a problem
where you need multiple potential
solutions okay this is the real trick
with this pattern you know everything we
do on the channel you need to take it
and you need to point it at a problem
there's a ton of value here that you can
get out of this interesting interesting
twoprompt infinite agentic loop pattern
right we're starting to compose prompts
we already know that great planning is
great prompting and you know maybe
that's a important thing to really
highlight here right we're generating
all these cool UIs um you know we can
continue to just look at look look at
this so interesting right we can look at
UI after
UI right after UI and look at this one
so interesting right look at all these
just interesting creative UIs there's
you know a lot of likely garbage here
but there's a lot of value here as well
right we're literally inventing new UIs
as we go along and new UI patterns right
we can just keep going check this one
out how cool is this okay so you know
this is the power of an infinite agentic
10:26
loop multiple solutions it's just going
10:28
to keep going keep firing we're using a
10:31
ton and ton and ton of compute here
10:34
right you can see we're launching
10:35
another wave of agents inside of this
10:38
agent right one tool call 30k 30k 30k 2
10:42
minutes each these are shorter jobs i've
10:45
run jobs that are 30 minutes plus and
10:48
you can fire them all off in a subtask
10:50
it's so incredible what we can do with
10:51
cloud code and with the right pattern
10:54
right the right prompting patterns that
10:56
lets us scale compute okay so really
10:58
interesting stuff there what's important
11:00
what's the signal here right couple
11:02
things to call out um you can pass
11:05
prompts into prompts you can specify
11:08
variables at the top of your files
11:11
you're likely going to want multiple
11:12
variables that control what happens and
11:15
what gets done okay we have this
11:18
infinite information dense keyword this
11:21
triggers our agenda coding tool to run
11:23
infinitely of course you need to phrase
11:25
things you need to be more specific with
11:27
how that works you can start with this
Great Planning is Great Prompting
11:30
prompt and modify it build it make it
11:32
your own couple more key ideas this is a
11:34
classic one right um we have been using
11:37
plans for over a year now on the channel
11:40
and every principal AI coding member you
11:43
know that great planning is great
11:44
prompting i sound like a broken record
11:47
bringing this up for you know over half
11:49
a year now but there's a reason for it
11:51
okay we know that tools will change we
11:53
know that models will improve you can't
11:54
fixate on these things right cloud code
11:57
is the very clear winner right now but
12:00
it won't always be that way okay and
12:02
we're going to get another model all
12:03
that stuff changes what doesn't change
12:05
is the principles of AI coding many of
12:07
you know this is why I built principled
12:09
AI coding sorry for existing members and
12:12
for engineers that have already taken
12:13
this but the repetition is probably
12:15
important anyway it's so so important to
12:17
realize that you want foundational
12:19
skills that don't change with the next
12:22
model with the next tool the plan right
12:25
great planning is great prompting this
12:27
is principle four or five this is so
12:29
relevant it's increasingly important
12:32
okay why is that it's because we can now
12:34
scale or compute further right but how
12:36
we do that is always about communicating
12:40
to our agents okay cloud code is the
12:42
best top agent right now for engineering
12:45
why is that it's because it operates in
12:47
the highest leverage environment for
12:49
engineers the terminal anything you can
12:52
do claw code can do and you know part of
12:55
me wants to say better you know we'll
12:57
debate that more in the channel as time
12:59
goes on it's definitely getting there uh
13:00
but you can see we're generating yet
13:02
another batch of agents here okay we
13:04
have this ocean file explorer very
13:06
interesting but anyways refocusing here
13:08
right the spec is super important
13:10
because this details what we want done
13:12
inside of this infinite agentic loop
13:15
right so we have this really cool
13:16
pattern where we're treating our prompts
13:19
like you can treat functions in certain
13:21
languages right you can you can pass the
13:23
function into a function that's what
13:25
we're doing here right the same idea
13:27
transferred to this domain of agentic
13:30
coding and really prompt engineering
13:31
we're taking a prompt passing it in to a
13:34
prompt you know the magic is obviously
13:36
in the pattern of this infinite agentic
13:38
loop but it's really in what you ask
13:41
your spec to do right it's what you ask
13:43
your agent to do there's a ton and ton
13:46
of value in this pattern i hope you can
13:48
see how powerful this is when do you
13:51
want to use something like this look at
13:53
all these UIs we have generating right
13:54
we have two two uh agents going back to
13:57
back
13:58
here very very cool so what when do you
14:01
want to use something like this you want
14:02
to use a pattern like this it's very
14:04
similar again to our parallel agent
14:07
coding with git work trees there we
14:09
cloned our entire codebase into the work
14:11
tree directory so that multiple agents
14:13
can work on their own directories again
14:15
link for that video is going to be in
14:16
the description i highly recommend you
14:17
check that out but what we're doing here
14:19
is so fascinating it's so powerful we're
14:21
scaling our compute we're solving a
14:23
specific problem with many variations of
14:26
how it can be solved so when do you want
14:28
to use the infinite agentic loop you
14:30
want to use it when there are multiple
14:32
potential solutions that you want to
14:34
explore you want to use it when you're
14:35
working on a hard problem that you don't
14:37
know the answer to and you think that
14:39
having many versions will help you get
When to use the Infinite Agentic Loop
14:41
closer and so this is all stuff you
14:43
would encode in your lower level prompt
14:45
that the infinite agentic loop prompt
14:47
will execute on right and you want to
14:49
use this when this is a really really
14:51
big idea uh this is like a lead
14:54
researchers are doing this when you want
14:55
to set up a self-improving agentic
14:58
workflow that is trying to achieve some
15:02
verifiable outcome that increases over
15:05
time okay we've all heard about
15:07
reinforcement learning you can take that
15:09
idea of reinforcement learning you can
15:10
take that idea of self-verifiable
15:12
domains and you can embed it in an
15:14
infinite agentic loop prompt like this
15:17
uh this is a really really big idea more
15:19
on this on the channel in the future we
15:21
don't have enough time to cover that
15:23
here right now but that's just really
15:24
important to call out those are kind of
15:26
the three big use cases for this that I
15:28
can find right away i'm sure if you dig
15:30
into this if you start using this you'll
15:32
find uh more you know use cases for this
15:34
right so pretty incredible stuff right
15:36
we have two agents running in cloud code
15:38
you can see I am hitting the limit i'm
15:40
breaking cloud code right now okay we're
15:42
running just straight out of Opus
15:44
credits i am running in the cloud code
15:46
max pro subscription wherever the top
15:48
tier is i'm going to go ahead i'm going
15:49
to stop these agents i I need a few more
15:51
credits for today to um do some other
15:54
engineering work i'm going to stop these
15:55
here you can see we're literally
15:57
infinitely generating tons and tons of
16:01
solutions to this problem right that's
16:03
the trick here right that's the real
16:05
value prop of the infinite agentic loop
16:07
you want multiple versions multiple
16:09
potential futures of an answer to a
16:11
problem that you have okay ui is
16:13
obviously just the simplest one that's
16:14
why I've showed it here a couple times
16:15
on the channel um you know we can just
16:17
keep looking through these different
16:19
user interfaces with different ideas and
16:21
themes blended together check this one
16:23
out very smooth very cool um and this is
16:26
all happening you know in the background
16:28
with compute we're scaling up doing this
16:30
again we're scaling up our compute even
16:33
further beyond that's what we do on the
16:35
channel every single Monday check out
16:37
Principal AI coding as many of you know
16:38
I am actively working on the second
16:41
phase course this is the foundation i
16:44
highly recommend you check this out what
16:45
comes next after AI coding is of course
16:48
agentic coding i'll have more details on
16:51
the next generation course as we move
16:53
closer to the release date looking at a
16:55
Q3 launch so stay tuned for that you
16:57
know this is a really powerful technique
16:58
try this don't ignore this please uh for
17:01
your own good um you know it's
17:02
completely free a lot of the stuff I'm
17:04
doing here obviously is all free for you
17:06
guys link in the description to this
17:07
codebase i'll save some of these
17:09
generations so you can kind of really
17:11
see and understand how this works but
17:13
it's really about the infinite prompt
17:15
take all this stuff make it your own
17:17
improve on it solve your problem better
17:19
than ever with compute big theme on the
17:21
channel to scale your impact you scale
17:23
your compute okay tune in make sure you
17:26
subscribe like all that good stuff
17:28
compute equals success scale your
17:30
compute you win you know where to find
17:32
me every single Monday stay focused and
17:35
keep building


CLion Is Now Free for Non-Commercial Use
Sponsored
jetbrains.com
Download


All

From IndyDevDan

Computer programming

Related

Watched


Customer Surveys
Sophisticated online survey platform with omnichannel distribution & analytics.
Sponsored
Qualtrics XM

Download

28:07
Now playing
Mastering Claude Code in 30 minutes
Anthropic
176K views Streamed 2 weeks ago


46:51
Now playing
Claude Code just destroyed all coding apps… it’s insane
David Ondrej
42K views 1 day ago
New


27:37
Now playing
PANEL 3: Strategic AI and Cybersecurity // Budapest Energy and Security Talks 2025
Egyensúly Intézet \\ Equilibrium Institute
6 views 1 hour ago
New

Shorts

The ancient humans who wiped out 90% of Europeans – David Reich
10M views


Why they make us look at the farmhouse
2.7M views


How Theia, the Planet that Created the Moon, Could Also Be Hiding in Earth’s Core
834K views

This Is the Closest Black Hole to Earth, and You Can See It with a Simple Telescope
15M views

Big WAHOO and then off to Poppys snack chair 😂🥰 #prairiedog #animal #cute
32M views

The Most Polite Cat Ever 😹
10M views



23:55
Now playing
How I build Agentic MCP Servers for Claude Code (Prompts CHANGE Everything)
IndyDevDan
15K views 7 days ago


11:21
Now playing
Let's Talk THAT Apple AI Paper—Here's the Takeaway Everyone is Ignoring
AI News & Strategy Daily | Nate B Jones
20K views 23 hours ago
New


23:25
Now playing
Astonishing discovery by computer scientist: how to squeeze space into time
Chalk Talk
340K views 3 days ago
New


8:09
Now playing
Canada’s Massive Play | Italian Referendum Fails | Vietnam's System & Tariffs
Market Update
2.1K views 1 hour ago
New


9:19
Now playing
Claude Code - 47 PRO TIPS in 9 minutes
Greg + Code
49K views 2 weeks ago


15:14
Now playing
AI's Most Promising Alien Hunters
Bloomberg Originals
9.8K views 4 hours ago
New


11:09
Now playing
Why MCP really is a big deal | Model Context Protocol with Tim Berglund
Confluent Developer
175K views 2 weeks ago


29:21
Now playing
Voice to Claude Code: SPEAK to SHIP Agentic Coding AI Assistant
IndyDevDan
10K views 4 weeks ago


16:46
Now playing
My SIMPLE FRAMEWORK to PICK the BEST AI Coding Tools (Aider vs Claude Code)
IndyDevDan
10K views 1 month ago


8:17
Now playing
Claude Code Is The Best AI Coding Agent [Tutorial]
Ras Mic
16K views 3 days ago
New


24:56
Now playing
How Vibe Coding Goes PRO
Brian Casel
26K views 4 days ago
New


11:39
Now playing
Deep Dive on OpenAI Data Connectors
AI News & Strategy Daily | Nate B Jones
5.5K views 4 days ago
New


27:32
Now playing
The Collapse of AI Reasoning (by Apple)
Discover AI
21K views 3 days ago
New


10:10
Now playing
AgentZero: ALL-IN-ONE AI Multi Agent Can DO ANYTHING With MCP Support & Plugins! (Opensource)
WorldofAI
8K views 1 day ago
New


32:29
Now playing
Single File Agents. Python Scripts with Astral UV. AI Coding with Aider Architect
IndyDevDan
31K views 3 months ago


12:13
Now playing
The great friendship collapse: Inside The Anti-Social Century | Derek Thompson
Big Think
104K views 23 hours ago
New


9:36
Now playing
China’s 34% Plunge: The Collapse Accelerates | US-China Trade War | Huawei’s Issues
China Update
1.4K views 21 minutes ago
New


22:43
Now playing
Syphilis Is Changing Like We've Never Seen... In Seattle
Heme Review
480K views 3 weeks ago

Shorts

The ingenious structure helping fish swim upstream
9.5M views


Scientists Warn Against Creating "Mirror Life"
2.4M views


He's Living Every Cat's Dream 🤩
7M views

Tucker was fired 10 minutes before it was announced? Barely enough time to pack up Nazi memorabilia!
4.5M views

Betelgeuse Supernova Soon? New Update
951K views

TOP-SECRET UFO FOOTAGE RELEASED | The Proof Is Out There | #Shorts
3.9M views


The year of the AI Agent: Beyond Automation - Ulysses Maclaren - NDC Melbourne 2025
NDC Conferences
188 views 3 hours ago
New

Claude Code INSIDERS: Codex FIRST Look and 5 AI Coding INSIGHTS
IndyDevDan
19K views 3 weeks ago

The powerful witch with the ability to control everything, tasked with saving the world
Feel Free Recap
3.8K views 23 hours ago
New

Episode #3 - AI killed my coding brain… and my ability to write basic code
Run it Bare
718 views 9 days ago

Sarah Silverman's Brief But Spectacular take on saying goodbye
PBS NewsHour
40K views 13 hours ago
New

A 3-step AI coding workflow for solo founders | Ryan Carson (5x founder)
How I AI
77K views 2 weeks ago

LocalSite: NEW Deepseek Coder! FULLY FREE AI Coder is INSANE! (Opensource + Local)
WorldofAI
4.6K views 12 hours ago
New

Extracting Knowledge Graphs From Text With GPT4o
Thu Vu
71K views 13 days ago

How I reduced 90% errors for my Cursor (+ any other AI IDE)
AI Jason
236K views 2 months ago

UIGEN-T3 14B & 4B + Free MCPs + Unlimited FREE API + RooCode: This is THE BEST Local UI Coder Setup!
AICodeKing
1.8K views 3 hours ago
New

RAG is Exploding: 58 NEW RAG Methods in 48 hours
Discover AI
28K views 2 weeks ago

AI Coding is NOT ENOUGH: Claude Code's NEXT LEVEL Agentic Coding FEATURE
IndyDevDan
64K views 1 month ago

Have you heard these exciting AI news? - June 06, 2025 AI Updates Weekly
Lev Selector
1.8K views 3 days ago
New

Is RL + LLMs enough for AGI? – Sholto Douglas & Trenton Bricken
Dwarkesh Patel
133K views 2 weeks ago

Building AI Agents at the Edge with NVIDIA Llama Nemotron Nano 4B
NVIDIA Developer
1.6K views 16 hours ago
New

"I've changed my mind on AI coding" – Adam Wathan (creator of Tailwind)
Justin Jackson
26K views 3 days ago
New

A Quest for a Cure: AI Drug Design with Isomorphic Labs
Google DeepMind
110K views 4 days ago
New

Activate Claude 4 GOD Mode To Build Beautiful Apps (TRY THIS NOW)
Income stream surfers
3.5K views 16 hours ago
New

    
