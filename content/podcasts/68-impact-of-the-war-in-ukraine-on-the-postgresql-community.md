---
title: "Impact of the War in Ukraine on the PostgreSQL Community – HOSS Talks FOSS 68 With Bruce Momjian"
description: "Catching up with Bruce on all things Open Source and PostgreSQL"
short_text: "Bruce and the Hoss catch up on all things Open Source and PostgreSQL.  They talk about the impact of the war in Ukraine on the PostgreSQL community & the rise of protest ware in open source.  Matt and Bruce also jump into the impact of end user/developers feelings towards databases in general on the future of PostgreSQL development.  Some developers care about databases but don’t have time, but there are others who don’t care. How do we involve both of these groups and inspire them?  Will derivative projects based on PostgreSQL help or hinder this effort?  Tune in and hear our thoughts."
date: "2022-05-24"
podbean_link: "https://percona.podbean.com/e/impact-of-the-war-in-ukraine-on-the-postgresql-community-%e2%80%93-hoss-talks-foss-68-with-bruce-momjian/"
youtube_id: "apssdN9eH50"
speakers:
  - matt_yonkovit
  - bruce_momjian
---

## Transcript
**Matt Yonkovit:**  
Hey everybody, welcome to another HOSS Talks FOSS. I'm the HOSS Matt Yonkovit, Head of Open Source Strategy here at Percona. And I am joined once again by Bruce Momjian, from EnterprisedB. Bruce has been on this podcast before, and we had been ships passing in the night last week at the Postgres conference. we saw each other but didn't get to catch up. So we figured why not exactly on a call like this and chat and catch up on what's going on? And so it's always exciting. we've got other conferences, and we're starting to be in person again, I don't know about you, but I'm glad to actually talk to people in person. Right

**Bruce Momjian:**  
Yeah, there was a lot of energy in San Jose, because everyone was together and a lot of stuff you couldn't talk about online, it was just too hard to really get the emotion across. It's much easier in a group. Yeah. Together in person. 

**Matt Yonkovit:**  
Yeah. And there were so many people to talk to. Right. So you got to talk to me a little bit about everything. Very true. Yeah. So, Bruce, I figured maybe we would just catch up on a few topics, and see what's trending. See, what you're seeing in the industry you are is plugged in, as plugged in can be in terms of the Postgres community and so I'm curious, what sort of trends things are you starting to see evolve? is you looking towards the next year? you've been talking with folks, you've been following the mailing lists? Are you seeing a couple of patterns or something that we should be aware of in the community?

**Bruce Momjian:**  
Well, probably the big issue this week. And last week, actually, was how to deal with the Russia issue. So I spent a lot of time on that. Because obviously, as a person in leadership, it kind of becomes my responsibility to keep an eye on what we talked about earlier about risks to the community, right? What does that look like? And it kind of spans quite a wide spectrum, for example. If we have committers, in these countries, what if they can't communicate with us securely? What if they don't feel they can actually tell us if something's wrong? Right, yeah. And so we kind of did that due diligence to find out who has commit keys and which countries? And there are all these people feeling like they can communicate with us? Because if they can't communicate with us, then effectively something bad could happen to them something bad? Could have been other keys? And we would not be aware of that, right. The second issue, that's kind of hot, same, same topic, is how to deal with people who want to disengage with Russia and Belarus. So we had somebody this week who did not want their blog entry syndicated to those countries. And how do we handle that? Is it do we require all the so we have, we have a planet Postgres, which syndicates all the blogs together, and they publicly posted that, although my blog summary will appear in Planet Postgres, anyone in Russia and Belarus, who clicks on that one, the link to see the full blog will actually not see it? And how does that it's certainly the right of that person to do whatever they want? They've, they're creating the blog content, but to the extent that they that we're syndicating that, is that acceptable? What does it do to the user experience do if everyone was to do this? What if Russians were to post a blog that was only visible to people in Russia? Would we accept that right, like, you see how it can kind of spiral out of control?

**Matt Yonkovit:**  
I know this is a topic that is a hot topic. In fact, Amanda Brock from the open UK is going to be talking at our conference, specifically about some of these topics, from an overall open source community perspective, which should be interesting. It's a slippery slope, but it's not the first time we've had a bit of controversy around this. If you remember, GitHub, blocked some countries when they had embargoes against them, right. So if you were in certain countries, you couldn't get to your GitHub project. And that was a big hubbub a couple of years ago. Because it was like, oh, wait a minute, what happened with this, Postgres being in a bit of a different space, but it does follow that same kind of geopolitical pressure if you will, because countries come and go on these different embargoes, so you have not only governmental regulations on what's allowed But then you have moral and ethical questions that come up. And it's a very difficult topic because you do see some open source projects start to develop morality clauses and focus on do we need more ethics like compliance things, but that's a dangerous slope as well. Yeah. if you think about it from a licensing perspective, you can use this software, unless your name is Bruce. How do you enforce it? How do you ensure that that happens? So it does become a little dangerous. As you might have seen, there were several articles over the last month or so, since the war in Ukraine started, where some people actually put poison pills in their open-source.

**Bruce Momjian:**  
Yeah, yeah, that was really, that was really serious. And obviously, it affects the reputation of that project. And also some way spills out to open source in general.

**Matt Yonkovit:**  
It does. It precedes doubt, in a company.

**Bruce Momjian:**  
Yeah. And this is not I did write a blog entry on the website called the abuse of open source with a question mark, because this is not a completely new thing. When you think of you go back to Alfred Nobel and the dynamite and him creating a Nobel Prize to sort of offset the damage. Think of the Manhattan Project engineers trying to prevent the use, of the atomic bomb against Japan. But also, even more recently, there was some open source, concern about the use of open source by the US Immigration and Customs Enforcement ice and that was sort of they came in when they really didn't, didn't really stick very much. But yeah, it's sort of like how you put the genie back in the bottle if it's knowledge. And software, in some sense, is knowledge, right? How do you? Can you restrict that knowledge? And if you do, what are the ramifications of that. And that's really where we've kind of come through. I mean, obviously, the open-source, legal, the term of what would be considered open source by the OSI does not have any discriminatory use to it. But then how do you deal with a blog entry that you're syndicating that has discriminatory use, so we're just kind of keeping an eye on it, it's not something we're ready to take an action on. Obviously, if it became widespread, and in fact, the blog entry explained in detail how other people could do the same thing if they want to show the Nginx examples of how to do it and do geolocation stuff. So the person in some ways is advocating that others follow this pattern. I haven't seen anybody follow it if it becomes followed, and it really hampers the usability of planet Postgres itself. That could be a concern to me, we have to add, because the bottom line and you wear this as well, is it open source? By definition, the OSI has no discriminatory, real use to it? So how does that OSI license for the software? Does that? How much does that spill into the infrastructure that we support and the planet Postgres infrastructure that we support? And how does that deal with content creators who may have discriminatory, right? So that's, that's, if you wonder, the hot topic for the past two weeks, that's it. He just, he just did it basically, two days ago, or a day and a half ago. So it is the hot thing I've been working with the Russians for since the invasion, making sure they're okay. Trying obviously, Postgres has relied a lot on Russian technology, Russian software, engineers, and all that not a lot of that non-relational stuff came from the Russians. So that I'm going to be speaking at Percona Live. So how do you honor and show appreciation for the work that's been done in the past? By a very, very dedicated Russian team, at the same time, not supporting an invasion? And how do you also help those who probably are as upset or more upset than we are? I put a personal blog out yesterday, basically, saying the title is the Russia I grew up in doesn't exist anymore. And this is a gentleman who left Russia for Georgia. And he basically said, he said, he said, I'm talking about the hope for this country to be happy and free, it's gone. It's not there anymore. And it probably will not happen now, in the next 20 or 30 years. And we're sitting there trying to understand what the new normal is, but the Russian who really understand the tragedy of this are also trying to figure out what the new normal is, in a way that impacts them even more than us. And the gentleman also talked about how tragic it is in Ukraine, and certainly more tragic in that it is for the Russians. But it's trying to sort of explaining that, that what that looks like going forward for Russia is really very unclear and very dark.

**Matt Yonkovit:**  
Yeah, no, and I mean a from a Ukrainian perspective, we all have colleagues lots of Percona employees are from the Ukraine and Russia. Our founders are, one Ukrainian and one Russian. Yeah. And I think that from an overall perspective, no one that I have talked to that I have connections within the community space thinks that anything that's going on is right, or just morally justified, it is a horrible situation. And it's amazing, the dedication of those folks in Ukraine and not only do they love their country, but a lot of them are still working, and it's an under the stress, and it's you have a lot of admiration for people who are willing to stand up for what they think is right. Yeah, yeah. Now, without minimizing that very difficult situation. And that is a tragic area. Let's, let's shift over a little bit to some of the more technical topics, some Postgres side of things. And I had given a talk last week, and it was interesting. My talk was on how developers are going to impact the future of Postgres and the development cycles. And I wanted your take on this because this is a trend that I am seeing more and more. I'm gonna say something that many people disagree with me, but I have a reason. So it might have to explain. Developers, a lot of developers and users don't like databases, right. They don't think databases are cool. they'd rather spend their time doing other things. Oftentimes, they think they're too complex. And the need for people to move fast. And not have to think are increasing. and that's not necessarily I am not, I don't condemn that, but I am seeing more and more people looking at no code or low code solutions I mean, for years, we've had to deal with ORM s connecting to databases. Yeah, exactly. for years, we've had frameworks and things, but we're starting to see an escalation in terms of like the needs and the desires, and almost a de-evolution of the skill set that most database professionals have. And so that worries me a bit in terms of inflection points from an open-source database perspective, because it means less feedback. But it also means people doing things that the databases were never intended to do, which could result in new features, or it could result in entirely new projects, or crazy things that try and take what we've already done and evolve it into something completely different. And I don't know if that's a trend you've been tracking or seen. But I'm curious about your take on that.

**Bruce Momjian:**  
It's funny, I thought it's something that I had never really thought of before because you were, you're talking about the right how, how is the new What's the new normal here? What's What are people kind of wanting from a database, right? And I kind of go back to my time as a developer back in the 90s, when we used to write applications. And a lot of times, I'm afraid that developers approach the data store of their application, as though they're the only person running it. So they're basically in their head. As they're thinking of their application. They're thinking, Okay, I got a flat-file here. And only when I'm reading my application, I'm like, Okay, I read a record, I put a record back, I read a record, I'll do the standard ORM kind of approach. But they're not. They don't really want to embrace the fact that 1000s of people potentially are doing it to the same Datastore at the same time, that there may be billions of records in there that are getting analyzed that are getting joined that are getting processed in other ways, and they're frustrated, they're frustrated that why is it so complicated? Why can I just get my data? Gee, if, if this was a single-user application, I would need any of this. Right? And they may be right. They a lot of cases, you don't need a relational system, if you've got a small amount of data, and it's not there's a single user so and of course, SQL Lite is a fantastic solution for that, although that itself is SQL. So maybe that's negative, I don't know. But, it feels like there's so much focus on tool sets and toolchains. And the new development paradigm of the month, it seems that, that they just don't have time, they don't have focus, they're, they're very focused upward out in what the UI looks like, and sort of how that's going to go to display to people and what's the user experience going to be? And that's great, but they don't want to look at that bottom piece. I think one of the things that makes me unusual, I've always been a tinkerer, I always go downward. I'm always like, when I started with computers, I read CPU books to understand, how does the hardware work? How does the IO work? I remember looking at your arts and how ISA bus, right? And because of that, as an application developer, I started to look at how does the database doing what it's doing, right? Because I'm wanting to understand downward from understanding the hardware, how I need to understand how the data and I got involved with Postgres, because of that interest at the lower level, right. But the question is, how do you do that, for people who aren't inclined in that way? And that's tough. I mean, I think, I think a lot of this stuff a lot of the nonrelational stuff that Postgres has really is very fascinating. And it, it, I think one of the reasons it's resonated with so many developers, is because it gave them a reason to like relational systems, because all of a sudden, you could, it wasn't this very restrictive thing. And you could do these cool things, which would be really hard to do in your application. And I almost think as a relational database, we have to continually market that. And, I think the best way to explain for me is having to understand the server understanding how NBCC works, how locking works, and how aggregates work. And all of that query optimizer stuff works, right? How all of that kind of fits together to make the developer's experience super simple, right? Because that's the beauty for me of it. Because if you don't use a relational database, you've and you need something complicated, then you have to do in your application. So I'm always regularly telling people that the database is the thing that makes your application simple. And as soon as you leave the relational system, whether you're going for a NoSQL solution or something else, your application, as you're saying is going to be a lot harder. And you're going to do stuff that you really shouldn't be doing like a nested loop in your app, when you should be doing a hash join, or a merge joins, you may not even know what those things are. And you certainly don't want to be writing them. And you certainly don't want to be writing them in a way that you ought to detect what type of results set should use, and which type of join in your app.

**Matt Yonkovit:**  
Now, that reminded me of a story. So I was actually helping a company and the company doesn't exist anymore. Really bad model, their model was to create a social media, like an app or website for your music playlists. So it's a little unusual, but I remember going there. And these were really smart, MIT, Stanford folks. And they actually just selected all of the data out of Table A all the data out of Table B, and then they joined it in Java. And then they did their joins in Java. They filtered out the data that they wanted, and then they throw it back. And then they went and they got another set of data. And they did the same thing. And they couldn't understand why the performance was so atrociously bad and it's like, Why do you think you're smarter than the people who wrote the joins within the database? Why are you taking everything and redoing and reinventing the wheel? But they thought because they were super smart that they could outthink the database and do it in a better more efficient way. I mean, yeah, I mean, at least I have to give them some credit for actually like, thinking about how joins work. Because I think in a lot of cases, people don't even think that. But it is a strange thing because you're right, a lot of people they'll not understand the database, how it works. And that causes issues. And I think that there is a difference, though, between those who don't care and those who just don't have the time. Right. And so I think that's a nuance, but I think some people do care. And they kind of like, they'll just trust that the database handles it and just figure it out later. And those people, they can develop bad code, bad designs, they can cause all kinds of issues, but then there are the ones that just don't care. And I think those are a bit more dangerous. But I think that we're I, I'm a bit concerned. And this is, this is one of those interesting things, the rise of people taking parts of Postgres and building other databases, and trying to establish new kind of like norms. I wonder what your take is on that, and what let me give you an example. Right, you've got some folks who will take the Postgres client libraries cockroach up by other folks. I mean, great databases, and great technology have no problems with them as companies. But it's a trend to kind of replace the back-end Postgres. And then I've seen other ones that are taking, and sticking with the back into Postgres, and adding compatibility layers on top to change all of the client protocols to make it something that it is. So it's, it's weird, because it's Postgres, like, but it isn't, Postgres. Right? And so I'm like, Oh, does this, how does this fit into the new ecosystem? And is this one of those, you're gonna be talking about challenges and risks? Is this a risk? Where do you start to see a bit more of a fracture? Or is it something that we say, this is just yet another kind of distribution? I just had someone on a podcast who likened Postgres to Linux. Right. And so this is just another distribution of Linux. And so it's an interesting take. And it's a bit of a slippery slope. And it's something that I've seen more and more of. And so and I'm not saying any of these technologies are bad. I'm not saying they're doing anything wrong. I'm just curious where this takes the ecosystem in the next 20 years. Right.

**Bruce Momjian:**  
Yeah. I do have a slide actually, about that in, in the deck for competitive challenges. So the good news is, this is not completed this is not entirely new. I mean, we had I think, I mean, we've had, we've had sort of forks of Postgres way back to when I started. So I think the Tiza might have been the first one who basically tailored it, for FPGAs. So they had an FPGA storage kind of solution. The early 2000s, and late 90s, I think, are pretty far back. Then we had some ports that ported Postgres to windows before we had a port, one was out of Japan and moves out of Boston, then we start to get a lot of data warehouse forks. Certainly, Greenplum is the best one. And then, so and now we're getting more of the distributed forks. So I almost feel like whatever sort of Hot Topic, there is, some startup kind of comes along and says, Hey, let's do a fork of Postgres and do X, right. I've always we've always had as a community mixed feelings on these things. I've always been of the opinion that the forking has two possibilities. Right. The first possibility is that the new fork becomes so popular, that it basically eclipses the original project. Ah, now you might think that's kind of bizarre, but if you look at I believe it's was it EGCs, the GCC compiler, that effectively was a fork of GCC and it became so popular that the GCC people had to eventually take it and make it the new GCC? Okay. And the reason for that was because the GCC project had become so conservative in adding compiler optimizations that EGC came along and it gets stuff everyone wanted, and everyone was like, Well, this is what we want. But and if EGC isn't going to do it, we're gonna use that. So GCC had to move over and just say we have to be, that's what we're going to use from now on. And all the current code for GCC is now really EGC s in a way, right? The second possibility is that the project, the fork becomes this extra thing that sort of takes a workload that the original thing doesn't do. And tailors it for that, whether it's for Greenplum, it would be, it would be data warehouse for Yugabyte, it would be distributed. And it doesn't do what the original does as well, but it does a similar thing. And I, frankly, I'm fine with that, I really feel that effectively as that new workload becomes popular, either we bring some of that code or those ideas into Postgres, or that project continues to grow, but they also need the community to grow at the same time. And they basically help the fund and bring Postgres forward. So, if we look at Greenplum there's been certainly a lot of engineers will be implemented helped us. There's a there's, there's a Percona Postgres, right, I think there's, there's EDB Postgres, there's a free Jitsu Postgres, and, as far as I know, all of those projects are helping rds, certainly Postgres is, is bringing in a lot of engineering help. So I kind of see it as better, it's really a, it's really a question of whether you see the world as expansive or limited, right? If you think of the world as having limited resources, limited opportunities, and you have to basically close off the challenges to your, to your world, then you're gonna see these forks as negative, if you think of an expansive universe, where they're opening up the use case for Postgres, they're opening up the visibility of the project. And, and you have to have the confidence of the project is strong enough to remain viable and visible in that environment, then you're going to embrace that, even if for example, Greenplum for the first 10 years, or whatever, it really just forked Postgres and didn't really come back a lot. There wasn't a whole lot of feedback. And then a couple of years ago, they were like, oh we really need to get up in current Postgres. There's a huge lag. Now, we're missing a lot of features. Let's get some engineers involved. Let's bring the code up to current Postgres. I don't know where they are on that now. But the point is that that fork, and certainly the EDB fork, the company I work for, has helped fund the community. And if we prevented those, then we wouldn't have those resources.

**Matt Yonkovit:**  
Yeah. And I mean, I think it's the philosophy if you make the pie bigger, everyone is more successful, right? So we're contributions more people who are contributing to the ecosystem, more eyeballs, more usage is we don't need to fight over the same territory,

**Bruce Momjian:**  
But you have to be a healthy project, you have to be nimble, you have to be one that embraces new people coming in, it doesn't happen by accident. And if you're, if you're rigid, like the GCC was, then this is going to be a problem. You really have to be, you have to be pretty strong. And in fact, I have another slide talking about whether the cloud could Eclipse open-source, that's another similar concern where the cloud becomes a fork, the cloud deployments, the cloud database services become before could they become so big, that people don't even know the project exists? Right? Yeah. And what would that look like? So you're, it's a similar kind of case. That where you have this, this service that's out there, that's kind of using, fortunately, you're using your name, right. So you're, you're kind of okay, there. But could it have become so big that, that nobody even downloads your software anymore. Nobody knows who you are. People don't think there's a way of getting involved except through the cloud provider. Right?

**Matt Yonkovit:**  
Yeah, that's that is a risk. Right? Yeah, the risk. So, Bruce, I like to kind of I started this since our last podcast. I like to end with kind of a rapid-fire set of questions, just some random things. Sure. Just interested in your get people can get to know you a little bit and also give you the opportunity to share some insights. So what is your favorite upcoming feature in Postgres 15?

**Bruce Momjian:**  
Probably, if I take a guess right now, the movement of the stat This is really geeky, the movement of the stats collector to shared memory, was a big thing for us. So it's something it's been a long-term issue that I think it's gonna, it's gonna improve quite a bit.

**Matt Yonkovit:**  
What was your favorite release of Postgres? Like, do you have a favorite? Like this one was just like

**Bruce Momjian:**  
Probably the one that added the Windows port was the coolest. Yeah. Okay, it would be 8.4 Something like eight.

**Matt Yonkovit:**  
Okay, fair enough. Last book that you read

**Bruce Momjian:**  
This book, what I read was a book on Amish history. Oh, okay. Yeah, very interesting. I'm on my fourth Amish book. I'm looking over there at the bookcase. That's something I'm really interested in. Because of the pack pandemic, I'm home a lot more so. Alright, let's get to the books.

**Matt Yonkovit:**  
All right. All right. So that's an interesting one. And so also curious if we are to meet you at a conference and we're going to go to dinner. What's your favorite food?

**Bruce Momjian:**  
Well, I just came back from a conference. I had two and a half ribeyes in five days. So I guess it's rebar.

**Matt Yonkovit:**  
Oh, yeah. So steak eater there...

**Bruce Momjian:**  
It's not necessarily my favorite, but it's the one I don't get at home a lot. So I have a tendency to favor that, so I didn't say favorite stuff. I don't get it home like a jumble. I love steak. I love I love it. I pretty much love everything. So yeah,

**Matt Yonkovit:**  
Fair enough. Okay, and we're gonna end with this one. If you can get through to developers worldwide or technologists worldwide, with just one thing that you wish that they would do? What would that one thing be? Make it you think here? Yes, sweat? No right or wrong answer.

**Bruce Momjian:**  
It is tragic to find that there's an easy solution that is something that you spent a lot of time working on. And a lot of times that answer is in the database.

**Matt Yonkovit:**  
Hmm. Okay. Okay. Make use of the tools that are available to you understand the technology that you're using, and explore your databases more. Always, good advice. Bruce, thank you for hanging out with me today on the HOSS Talks. FOSS. I appreciate you stopping by we are going to look forward to catching up in person at Percona Live in a few weeks here. That should be exciting. And any final words for the audience here?

**Bruce Momjian:**  
No, I'm certainly looking forward to Percona Live. So I think this might be the first time I've done the US one. I've done the European ones quite

**Matt Yonkovit:**  
Oh, okay. So this is unusual because you're from the US.

**Bruce Momjian:**  
what happens is that the events are always on travel. I'm already out there. So it's like I'm already in Europe. So yeah, every time it's been in the US it's been a conflict, but it's always worked. It's so I'm so excited. I'm excited to go to Austin and be in person again together. Right? Yes. To hang out and have a good time. Yeah, it is really, it is really something I've missed.

**Matt Yonkovit:**  
Yeah. And for those who are watching, go ahead and like this video, and subscribe to it. Give us comments, give us questions, and tell us what audience or guests you would like to pursue in the future. If you'd like to hear from Bruce again. Do you want me to bring him on and grill him on some topic? Feel free to suggest that as well. I'm happy to do that. You know me, I like to talk to people. But, Bruce, hopefully, that's okay with you, Kim before I said go ahead and have me grill him. But until next time, we appreciate you hanging out with us. We'll see you later.

**Bruce Momjian:**  
Bye-bye. Great. 

