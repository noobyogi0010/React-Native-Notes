# Introduction to React Native

React native is an open source JavaScript framework which is used to develop Android and iOS applications using React and the native capabilities of these platforms as well.

With React native, you can use JavaScript to access the APIs and describe the UI and it's behavior for your app.

## Views
In mobile development, every element on UI is some kind of a view. A view is the smallest rectangular element which can be used to display images, text or simply show user some message.

In other words, consider your mobile's screen as a pin board. Now you want to add posters, advertisements, notices, letters, etc on it. But before pinning anything on this board you need to make sure that attach your document on some rectangular sheet. Now, let's say Jaya wrote an article about *Twitter Trends* she affixed her article on a rectangular sheet and then pinned it to the board. Next, Dina came with her new *Anime Drawing* cut into a cicular shape. As she knows that she cannot affix it directly on the board, she first paste it on a rectangular sheet and then pin that sheet on the board.
Similarly, in **Mobile Development** this **pin board** is your **mobile screen** and the **rectangular sheets** are **views**. You can affix any amount, shape and size of elements on your views.

## Native and Core Components

In react native, we basically have two types of components:
1. **Native Components** - These are the components of native platforms, i.e., Android and iOS platform. We can't directly use them here in React Native. In order to use them  we have to call them from JavaScript using the React components. We can firmly say that all the components that we use and create in React Native invoke these views using the underlying JavaScript. Some of them are ImageView, TextView, ScrollView, etc.
2. **Core Components** - These are the components that React Native provide us to get started with. We can use these core components to build literally anything. We can use them to create our own custom components with as many complexity as we like. Some of them are View, Text, Image, etc.
