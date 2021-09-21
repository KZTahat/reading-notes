# Read 22

## Component Lifecycle / useEffect() Hook

1. Why do we not need more .html pages in a multi-page React app?
    because we keep changing the content on the same html page, so onlu one to render all data.

2. If we wanted a component to show up on every page, where would we put it and why?
    Inside the <BrowserRouter />, outside a <Route /> because I want it to be inside the browser but I don't want to restrict it with some sort of route.

3. What does routing do with the components that were rendered when a new route is requested
    if we have a match with a route, the app will only render the components that lays under that route scope.

4. What does props.children contain?
    it contains all the infprmation that were passed from the child component.

5. How do useState() and this.setState() differ?
    useState() can only be used inside a functional components where it provides the state and the method to update this state BUT this.setState() is used inside class components and it manage to update any states that exists in that class constructor.


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)