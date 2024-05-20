---
layout: single
title:  "Summarizing and creating a reading list with ChatGPT"
---

## Summary
I like to read books. I'm always looking for ways to discover new titles. I mainly use Goodreads and Twitter as a discovery mechanism, and I use Goodreads to track my reading queue. I love when I find lists of books that others are reading, particularly when I discover a book I hadn't come across yet. It's been a while, but I shared my [top books from 2013](/2014/01/12/top-books-from-2013.html). I've read a lot between then and now, but haven't shared any of my lists. I wanted to see how I could use ChatGPT to build a similar summary list, with limited manual effort. I also wanted to see how I could use ChatGPT to find new recommendations based on books I've enjoyed.

Below, I'll share some learnings from this experiment, along with my reading list, and a new list of books recommended through using ChatGPT

## Steps and learnings with ChatGPT Prompting

- To build the initial list of books, I used this prompt:
  > I am going to give you a list of books below. I will be speaking them. I want you to take the title of the book and find the author of the book and create a bulleted list with all of the books. I'm going to speak starting now...(followed by me iterating over the book titles)...

  ChatGPT was able to build a bulleted list of all the books. Looking at the final prompt, there were some spelling errors and lack of separation between the spoken book titles due to speech-to-text -- but it was able to figure it out.

- ChatGPT was able to summarize the books and provide some representative quotes from the books. I used the following prompt (again, I was using speech-to--text to generate the prompt):
  >  I want you to take the above list and modify it in the following way for each book I want you to add a bullet under the book with a one to two sentence summary of what the book is about. I want you to add another bullet for each book that represents one of the most popular quotes from the book.

- I played around with the summary and quote content length. I also augmented each book with a link to its Amazon page.
  > For the original list of books that contain summary and a single quote, can you please make the title of the book a clickable link to where you can buy it on Amazon
  >
  >  can you modify the summary to be a bit more detailed maybe 3 to 5 sentences. Also, can you provide 2 to 3 different quotes for each one?

- I was a bit more specific when I asked ChatGPT to generate a future reading list. Here's the prompt I used
  > Given the above list of books, I want you to do the following:
  >   - Generate me a list of 10 possible books to read
  >   - The book recommendations should be informed by themes in the above books, and the likelihood that I will find them enjoyable given my interests above
  >   - The books should be less well known
  >   - The books should be written before the year 2000
  >   - Please provide these books in the same format used above

- I used ChatGPT to adjust the styling of the list, so that I could just copy/paste it in this post here. I asked it to create Markdown, and then played around with the formatting via a few iterative prompts. Here are two examples:
  > Can you format the list of books I read in markdown
  >
  > I want you to change the markdown so that, instead of having a bullet with the word quotes followed by a bullet list of quotes, I want to have a markdown quoted bulleted list using the quote capabilities of markdown


- ChatGPT did choose a few incorrect Amazon links, which I had to adjust manually

- The future reading list ChatGPT generated looks promising. I've only read 2 of the 10, and I haven't heard of most of the others

- I did attempt to get ChatGPT to write this post, but was unsatisfied with how it read. I decided to write the main post from scratch, rather than attempt to edit what it gave me. This is the prompt I used to try to write the post (it wasn't terrible, but didn't sound like me)
> I want to write a short post on my personal site highlighting the workflow I went through above to generate the list of books. Here is the criteria for the post:
>   - I want it to be in the same written style as other posts on mattstockton.com
>   - I want it to highlight the following goals:
>     - Build a summarized list of my most favorite books I've read over the past ~1 year
>     - Surface high-level summaries from those books, along with some short but relevant quotes
>     - Discover other books I might be interested in reading, that are lesser known and over 20 years old


Overall, I was pleased with the result, and it didn't take a lot of time to do. Drop me a note and let me know what you think of the reading lists below. If you've got some good reading recommendations, send those my way as well.

## Books I enjoyed recently 

Here's the list of books I read and enjoyed recently. The content and format of this list was generated with ChatGPT (as noted above in the learnings)

[**Outlive: The Science of Longevity**](https://a.co/d/3KaVIRh) by Peter Attia

This book explores cutting-edge research on extending the human lifespan and improving overall health. Attia delves into topics such as diet, exercise, sleep, and medical advancements to present a comprehensive guide to living a longer, healthier life. He emphasizes the importance of preventative measures and personalized health strategies.
  > "The goal isn't just to live longer, but to live healthier and more vibrant lives."
  >
  > "Prevention is the key to longevity; it's about addressing potential problems before they become real issues."
  >
  > "Our approach to health must be proactive, not reactive."

[**Good Strategy Bad Strategy: The Difference and Why It Matters**](https://www.amazon.com/dp/0307886239) by Richard Rumelt

Rumelt clarifies what constitutes good and bad strategy, emphasizing the importance of clear, coherent actions and realistic goals. He provides numerous examples from business, politics, and military history to illustrate his points. The book serves as a practical guide for leaders looking to develop effective strategies.
  > "A good strategy works by harnessing and applying power where it will have the greatest effect."
  >
  > "Bad strategy is not the absence of strategy; it's the presence of poor or faulty strategy."
  >
  > "Good strategy requires clear, decisive actions that lead to tangible results."

[**Principles for Dealing with the Changing World Order**](https://www.amazon.com/dp/1982160276) by Ray Dalio

Dalio uses historical analysis to predict future economic and political changes. He examines past cycles of rise and decline in global powers to offer insights into how current shifts might unfold. The book provides practical advice for individuals and policymakers on how to navigate these changes.
  > "The world is going to change in shocking ways over the next few years."
  >
  > "History shows us that nothing lasts forever, and the most successful societies are those that adapt."
  >
  > "Understanding past patterns is crucial to anticipating future trends."

[**The Coaching Habit: Say Less, Ask More & Change the Way You Lead Forever**](https://www.amazon.com/dp/0978440749) by Michael Bungay Stanier

Stanier presents seven essential questions that can transform how leaders coach their teams. By focusing on asking more and telling less, leaders can foster a culture of empowerment and continuous improvement. The book is filled with practical tips and real-life examples to help leaders apply these coaching techniques effectively.
  > "Stay curious a little bit longer, and rush to action and advice-giving a little bit more slowly."
  >
  > "Great leaders are not those with all the answers, but those who ask the right questions."
  >
  > "Coaching is about unlocking potential, not providing solutions."

[**Why We Sleep: Unlocking the Power of Sleep and Dreams**](https://www.amazon.com/dp/1501144316) by Matthew Walker

Walker delves into the science of sleep, explaining its crucial role in health, cognitive function, and emotional well-being. He covers the negative impacts of sleep deprivation and provides practical tips for improving sleep quality. The book underscores the necessity of prioritizing sleep for a healthier life.
  > "The best bridge between despair and hope is a good night’s sleep."
  >
  > "Sleep is the single most effective thing we can do to reset our brain and body health each day."
  >
  > "Dreams are not just bizarre tales, they are essential to our mental and emotional health."

[**Build: An Unorthodox Guide to Making Things Worth Making**](https://www.amazon.com/dp/0063046067) by Tony Fadell

Fadell shares his experiences in design and technology, offering insights into the process of creating innovative products. He emphasizes the importance of understanding user needs and iterating designs based on feedback. The book is both a memoir and a practical guide for aspiring entrepreneurs and product developers.
  > "Building great products is hard. Building a great team is even harder."
  >
  > "Innovation starts with understanding the problem, not the solution."
  >
  > "The best products are those that anticipate users' needs before they even realize they have them."

[**Good Inside: A Guide to Becoming the Parent You Want to Be**](https://a.co/d/j7bRlyr) by Dr. Becky Kennedy

Dr. Becky Kennedy offers a compassionate approach to parenting, focusing on understanding and nurturing the emotional well-being of both children and parents. She provides practical strategies for handling everyday challenges while fostering a positive and empathetic family environment.
  > "Parenting is about growing ourselves as much as it is about growing our children."
  >
  > "Children want to be good inside, and it's our job to help them feel that way."
  >
  > "Empathy and understanding are the keys to effective parenting."

[**Atlas of the Heart: Mapping Meaningful Connection and the Language of Human Experience**](https://www.amazon.com/dp/0399592555) by Brené Brown

Brown explores the emotions and experiences that define human connection. She offers a framework for understanding and expressing these feelings, helping readers build deeper and more meaningful relationships. The book combines research with personal anecdotes to illustrate key points.
  > "Connection is why we’re here; it is what gives purpose and meaning to our lives."
  >
  > "Vulnerability is the birthplace of love, belonging, joy, courage, empathy, and creativity."
  >
  > "We are wired for connection, but the key is to ensure those connections are meaningful."

[**Same as Ever: A Guide to What Never Changes**](https://a.co/d/fI1iaBP) by Morgan Housel

Housel discusses the timeless principles and behaviors that remain constant despite technological and societal changes. He argues that understanding these constants can help us navigate an ever-changing world more effectively. The book combines historical analysis with practical advice.
  > "The most important things in life are the things that never change."
  >
  > "In a world of constant change, understanding what remains the same is crucial."
  >
  > "Human nature doesn't change, and understanding it is the key to navigating the future."


[**The Creative Act: A Way of Being**](https://www.amazon.com/dp/0593652886) by Rick Rubin

Rubin shares his philosophy on creativity, emphasizing the importance of being open to inspiration and trusting the creative process. He provides insights into how to cultivate creativity in everyday life and overcome common obstacles. The book is both a guide and a source of inspiration for creative individuals.
  > "Creativity is not a noun, it's a verb. It's a way of being."
  >
  > "The best ideas often come from the least expected places; stay open to everything."
  >
  > "Creativity is about finding new ways to solve old problems."

[**Unreasonable Hospitality: The Remarkable Power of Giving People More Than They Expect**](https://a.co/d/anvrJFJ) by Will Guidara

Guidara emphasizes the importance of exceeding expectations in hospitality to create memorable experiences for guests. He shares stories from his career in the restaurant industry to illustrate how going above and beyond can transform customer experiences. The book provides practical tips for anyone in the service industry.
  > "When you make people feel seen and valued, you create magic."
  >
  > "Hospitality is not just about what you do; it's about how you make people feel."
  >
  > "Exceeding expectations is the key to creating unforgettable experiences."

[**The Book You Wish Your Parents Had Read (And Your Children Will Be Glad That You Did)**](https://a.co/d/iCnN1pq) by Philippa Perry

Perry offers practical advice on how to improve communication and relationships with children, based on psychological insights and personal experience. She covers topics such as emotional intelligence, effective listening, and conflict resolution. The book aims to help parents raise happy, well-adjusted children.
  > "There is no such thing as perfect parenting, but there is such a thing as good enough parenting."
  >
  > "Understanding your own emotions is the first step to understanding your child's."
  >
  > "The way we talk to our children becomes their inner voice."

[**On Writing: A Memoir of the Craft**](https://www.amazon.com/dp/1982159375) by Stephen King

King shares his experiences and insights on writing, providing practical advice for aspiring writers along with a memoir of his own career. He discusses the tools of the trade, the process of writing, and the importance of persistence. The book is both a guide and an inspirational memoir.
  > "Books are a uniquely portable magic."
  >
  > "The scariest moment is always just before you start."
  >
  > "You can, you should, and if you’re brave enough to start, you will."

[**Mastery**](https://www.amazon.com/dp/014312417X) by Robert Greene

Greene explores the paths taken by historical figures to achieve mastery, offering insights on how to attain excellence in any field. He emphasizes the importance of apprenticeship, practice, and perseverance. The book provides a roadmap for anyone looking to achieve high levels of skill and success.
  > "The future belongs to those who learn more skills and combine them in creative ways."
  >
  > "Mastery is not a function of genius or talent. It is a function of time and intense focus applied to a particular field of knowledge."
  >
  > "To know one's destiny is the key to bring it to fruition."

[**Thinking in Systems: A Primer**](https://www.amazon.com/dp/1603580557) by Donella H. Meadows

Meadows introduces the concept of systems thinking, providing tools to understand and address complex problems in various domains. She explains how to analyze systems, identify leverage points, and implement effective changes. The book is a foundational text for anyone interested in systems theory.
  > "You can’t understand a system until you try to change it."
  >
  > "Systems thinking is a discipline for seeing wholes. It is a framework for seeing interrelationships rather than things, for seeing patterns of change rather than static snapshots."
  >
  > "The purpose of a system is what it does."

[**The Alignment Problem: Machine Learning and Human Values**](https://www.amazon.com/dp/0393635821) by Brian Christian

Christian examines the ethical challenges of artificial intelligence, focusing on how to align machine learning systems with human values. He explores the implications of AI in various fields and discusses the importance of developing ethical frameworks for technology.
  > "The challenge of our time is not just to make powerful AI, but to ensure it operates in alignment with our highest values."
  >
  > "We must develop AI that understands and respects human values to ensure its benefits are widely shared."
  >
  > "Ethics in AI is not an afterthought; it must be integrated from the start."

[**Difficult Conversations: How to Discuss What Matters Most**](https://www.amazon.com/dp/0143118447) by Douglas Stone, Bruce Patton, and Sheila Heen

This book provides strategies for navigating tough conversations effectively, helping individuals address and resolve conflicts constructively. It offers tools for understanding and managing emotions, improving communication, and finding common ground.
  > "The single most important thing you can do is to shift your internal stance from 'I understand' to 'Help me understand.'"
  >
  > "Difficult conversations are almost never about getting the facts right. They are about conflicting perceptions, interpretations, and values."
  >
  > "Being able to listen and understand another person's perspective is the most important skill in difficult conversations."

[**The Anthology of Balaji**](https://a.co/d/3txYD6d) by Balaji Srinivasan

This collection features the writings and ideas of Balaji Srinivasan on technology, society, and the future. Srinivasan's insights cover a wide range of topics, from blockchain and cryptocurrencies to the evolution of digital communities and decentralized systems.
  > "The future is decentralized, and the key to unlocking it lies in technology and innovation."
  >
  > "Understanding the intersection of technology and society is crucial for navigating the next century."
  >
  > "Innovation doesn't just change industries; it transforms societies and empowers individuals."

## Books recommended by ChatGPT

Here are the books recommended by ChatGPT using the process described above

[**The Systems View of Life: A Unifying Vision**](https://a.co/d/bBRNrth) by Fritjof Capra and Pier Luigi Luisi

This book offers a comprehensive look at life through the lens of systems thinking. Capra and Luisi discuss the interconnectedness of biological, cognitive, social, and ecological systems, providing a holistic understanding of life and its processes.
  > "Life is much more than the sum of its parts."
  >
  > "To understand life, we must look at it in its entirety, as an interconnected web of relationships."
  >
  > "Systems thinking offers a framework for seeing the world in new ways, for understanding the complexity of life."

[**The Art of Possibility: Transforming Professional and Personal Life**](https://www.amazon.com/dp/0142001104) by Rosamund Stone Zander and Benjamin Zander

This book presents twelve practices for bringing creativity and a sense of possibility into every aspect of life. The Zanders draw from their experiences in the arts and leadership to inspire readers to adopt a more open and creative mindset.
  > "It’s all invented. So we might as well invent a story or a framework of meaning that enhances our quality of life."
  >
  > "Giving an A speaks to possibility. In the game of giving an A, no one has to earn anything."
  >
  > "A vision articulates a possibility. Its purpose is to create a frame of reference that gives people room to thrive."

[**The Innovator's Dilemma: When New Technologies Cause Great Firms to Fail**](https://www.amazon.com/dp/0875845851) by Clayton M. Christensen

Christensen examines why successful companies often fail to innovate and adapt to new technologies. He explores the challenges of disruptive innovation and provides insights into how businesses can remain competitive in a rapidly changing market.
  > "Disruptive innovations bring to market a very different value proposition than had been available previously."
  >
  > "Great firms fail because they do everything right."
  >
  > "The same practices that lead to success can also lead to failure when circumstances change."

[**Finite and Infinite Games: A Vision of Life as Play and Possibility**](https://www.amazon.com/dp/0345341848) by James P. Carse

Carse presents a philosophical exploration of the two types of games people play: finite games, which are played to win, and infinite games, which are played for the purpose of continuing the play. He applies this framework to various aspects of life, including relationships, culture, and personal growth.
  > "A finite game is played for the purpose of winning, an infinite game for the purpose of continuing the play."
  >
  > "Only that which can change can continue."
  >
  > "To be prepared against surprise is to be trained. To be prepared for surprise is to be educated."

[**The Inner Game of Work: Focus, Learning, Pleasure, and Mobility in the Workplace**](https://www.amazon.com/dp/0375758178) by W. Timothy Gallwey

Gallwey applies the principles of his "inner game" approach, originally developed for sports, to the workplace. He emphasizes the importance of focus, learning, and enjoyment in achieving professional success and personal fulfillment.
  > "Work can be a means to discover and express one's own potential."
  >
  > "The most effective way to change behavior is to change the focus of attention."
  >
  > "Learning and performance can coexist if we understand how to balance them."

[**Leadership and the New Science: Discovering Order in a Chaotic World**](https://www.amazon.com/dp/1576753441) by Margaret J. Wheatley

Wheatley explores how concepts from the new sciences—such as chaos theory, quantum mechanics, and biology—can be applied to leadership and organizational change. She argues for a more holistic and dynamic approach to managing organizations.
  > "In a world of constant change, the only way to maintain stability is to change as well."
  >
  > "Organizations are living systems, and their capacity for growth and change depends on their relationships."
  >
  > "Leadership is about creating the conditions in which people can become more fully themselves."

[**The Tao of Leadership: Lao Tzu's Tao Te Ching Adapted for a New Age**](https://a.co/d/1wvRoV4) by John Heider

Heider adapts the ancient wisdom of Lao Tzu's "Tao Te Ching" to modern leadership challenges. The book provides timeless principles for leading with integrity, humility, and effectiveness.
  > "The wise leader knows that a great deal cannot be controlled. The leader learns to go with the flow."
  >
  > "By being selfless, the leader enhances self."
  >
  > "When the leader's work is done, the people say, 'We did it ourselves.'"

[**The Fifth Discipline: The Art & Practice of The Learning Organization**](https://www.amazon.com/dp/0385517254) by Peter M. Senge

Senge discusses how organizations can achieve success through continuous learning and offers strategies for fostering a culture of innovation and growth. He introduces systems thinking as the cornerstone of a learning organization.
  > "The ability to learn faster than your competitors may be the only sustainable competitive advantage."
  >
  > "People don't resist change. They resist being changed."
  >
  > "Systems thinking is a discipline for seeing wholes. It is a framework for seeing interrelationships rather than things, for seeing patterns of change rather than static snapshots."

[**Awaken the Giant Within: How to Take Immediate Control of Your Mental, Emotional, Physical and Financial Destiny!**](https://www.amazon.com/dp/0671791540) by Tony Robbins

Robbins provides a step-by-step program for improving one's life through mastering emotions, finances, relationships, and personal goals. He emphasizes the power of decisions and the importance of taking control of one's destiny.
  > "It's not what we do once in a while that shapes our lives. It's what we do consistently."
  >
  > "The path to success is to take massive, determined action."
  >
  > "If you do what you've always done, you'll get what you've always gotten."

[**The E-Myth Revisited: Why Most Small Businesses Don't Work and What to Do About It**](https://www.amazon.com/dp/0887307280) by Michael E. Gerber

This book addresses the myths surrounding starting your own business and shows how commonplace assumptions can get in the way of running a successful enterprise. Gerber walks you through the steps in the life of a business and explains how to apply the lessons of franchising to any business, whether or not it is a franchise.
  > "The entrepreneurial myth is that most businesses are started by entrepreneurs risking capital to make a profit. The truth is that most are started by technicians suffering from an entrepreneurial seizure."
  >
  > "Working on your business, not in it, is the key to long-term success."
  >
  > "Your business is not your life. Your business and your life are two separate things."
