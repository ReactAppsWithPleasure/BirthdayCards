# Birthday-useState

Creates basic React project.

Example of using:
- useState - get data from file
```jsx
  const [people, setPeople] = useState(data)
```
- setState - to clear List on button click
```jsx
  <List people={people} />
  <button onClick={() => setPeople([])}>Clear All</button>
```
- .map data-array - to render array of entities(person)
```jsx
  const List = ({ people }) => {
    return (
      <>
        {people.map(person => (
          <Person key={person.id} {...person} />
        ))}
      </>
    )
  }
```
- destructuring object person
```jsx
  const Person = ({ id, name, age, image }) => {
    return (
      <article key={id} className='person'>
        <img src={image} alt={name} />
        <div>
          <h4>{name}</h4>
          <p>{age} years</p>
        </div>
      </article>
    )
  }
```
  

Create List component and Person component(to hold person details)
