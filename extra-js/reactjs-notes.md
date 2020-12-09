# React


### Install MaterialUi

$npx create-react-app my-app

$npm install react-router-dom  @material-ui/core  @material-ui/icons

**Roboto fonts**
$ npm install typeface-roboto --save

''' 
"import 'typeface-roboto';"
'''



#### Use Memo

```javascript

  const [arg, setArg] = React.useState("10");
  const [clients, setClients] = React.useState([]);


  useEffect(() => {
    getClients()
  },[arg])

  let myExpensiveResultObject = React.useMemo(async () => {
    const response = await axios.get(SERVER+ 'business/clients' )      
  
    let items = []
    if (response && response.data){  
      items = response.data
    }
    console.log("Done running expensive work");
    return items;
  }, [arg]);

  
  const getClients = async () => {
    const result = await myExpensiveResultObject;
    setClients(result);
  }

   
```
