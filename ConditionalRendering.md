## Conditional Rendering With If
```
const ConditionalRenderingWithIf = ()=>{
    const isLoggedIn = false;

    
//     if(isLoggedIn){
//         return(
//             <h1>dashboard page</h1>
//     )
// }else{
//         return(
//             <h1>Login page</h1>
//         )
//         }
//     }
return( //terninary operatory
    <>
        {isLoggedIn? <h1>welcome user</h1>: <h1>welcome guest   </h1>}
        <ConditionalRenderingWithAndAnd  fruits={["apple","banana","ball"]}/>
        <CRwithDefaultFallbackValue animals={[]} />
        <CRwithSwichCase role="user" />
        <CRwithMapAndFilter />
    </>
)
}
export default ConditionalRenderingWithIf
```
## Conditional Rendering with Map and Filter
```
const CRwithMapAndFilter =()=>{
    var arr=[1,2,3,4,5,6,7,8,9,10]
    return(
        <>
       <ul>
       {
            arr.filter((ele, index)=>{
                return ele >     5
            }).map((element, index)=>(
                <li key={index}>{element}</li>
            ))
        }
       </ul>
        </> 
    )
}

```

## Conditional Rendering with Fallback value
```
const CRwithDefaultFallbackValue = ({animals})=>{
    return (
    <>
    <h1>Animal Report</h1>
    {
        animals.length > 0 || <p>No Animals Found</p>
    }
    </>
    )
    
}
```
## Conditional Rendering with Switch case
```

const CRwithSwichCase=({ role })=>{
    switch(role){
        case "admin":
            return(
                <h1>
                    Admin Dashboard
                </h1>
            )
            case "user":
                return(
                    <h1> user dashboard</h1>
                )
                default:
                    return(
                        <h1>guest dashboard</h1>
                    )
    }
}

```

## Conditional Rendering with AndAnd
```
const ConditionalRenderingWithAndAnd = ({fruits})=>{

    return(     
        <>
        <h1>no of Fruits</h1>
        {
            fruits.length > 0 && <p>{fruits.length}</p>
        }
        </>
    )
}
```
