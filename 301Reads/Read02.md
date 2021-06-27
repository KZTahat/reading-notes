# Discussions
## React lifecycle

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?<br />
    Based off the diagram the 'render' happens befor 'componentDidMount'.
<br />

2. What is the very first thing to happen in the lifecycle of React?<br />
    The static getDerivedStateFromProps is the first React lifecycle method to be invoked during the updating phase.
<br />

3. Put the following things in the order that they happen:<br />
    those will be in this order : <br />
    - constructor.<br />
        The constructor for a React component is called before it is mounted.If the component is a subclass you should call super(props), or the props will be undefined. constructors can be used to assign state using this.state or to bind event handle methods to an instance.
        
        ``` 
        class FishTableRow extends React.Component {
            constructor() {
            super(props); //gives us access to props
            //Don’t call this.setState() here
            this.state = { //intitialize local state
            showDescription: false
        }; }
        ```
        <br />
    - render.<br />
        Render is the only required method in a class component. It will examine this.props and this.state when called. The render function should not modify the component state because it would cause a lot of bugs by changing the state every time it rerenders. I also should not directly interact with the browser. render will not be invoked if shouldComponentUpdate() returns false. Here is an example of using render.
            
            ReactDOM.render(

                    <FishTable fishes= {fishData}/>,//set fishes document.getElementById(‘app’)

                    );
        <br />
    - React Updates.<br />
    - componentDidMount.<br />
        This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount().<br />
        
        setState() can be called here, but it should be used sparingly, because it will cause a rerender, which can lead to perfomance issues.<br />
        
        Here we use componentDidMount() to connect to the YouTube API and get videos when the components is rendered.
        <br />

    - componentWillUnmount.<br />
        This method allows you to clean up the DOM and netwrok requests/ subscriptions.
        <br />

4. What types of things can you pass in the props?<br />
    Props is kind of for things that you passed like a function, thier what you want to initilize your component to or what you want your component to render like, or we can use props to send the things we need to show to the user like a title or a subtitle.<br />

5. What is the big difference between props and state?<br />
    The big difference between props and state is props you pass into a component and state is handled inside of that component and props is handeled outside, we use props to send the parameters and we use state for making changes to that, state is handeled in the component and we can update it inside component while props is handeled outside the component and must be updated outside the component.<br />

6. When do we re-render our application?<br />
    Another thing about props vs state is when you change the state inside of your application it's going to re-render that part of your application whiel props we can't acually change them we need to do it outside.<br />

7. What are some examples of things that we could store in state?<br />
    - Counter Application.<br />
    - Inside of a form (input element, check box, select boc).<br />

<br />
<br />

[Home]( https://kztahat.github.io/reading-notes/)