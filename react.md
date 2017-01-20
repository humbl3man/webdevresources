##Unidirectional Data Flow

**Unidirectional Data Flow:** All data in our applications flow in a single direction. In React it flows down the tree from parent to child. This makes tracking the source and destination easy compared to other architectures where data may be coming from many parts of the application.

**Application State:** The state or data in our application that is core to the functionality of the application as a whole. This usually includes a list of the models and data being manipulated by the interface. If we were to reload our application, the Application state is what we would like to persist the most

**Local Component State:** This is state that is used to allow a component to function. Local component state is typically not used by other components in the application, and is less important to persist if the application resets.
