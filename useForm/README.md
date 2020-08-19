# useForm

```
    const initForm = {
        name: '',
        age: 0,
        email: ''
    };

    const [ formValues, handleInputChange, reset ] = useForm( initialForm );

    EJEMPLO:


    
export const SearchScreen = () => {

    const heroesFiltered = heroes;
    const [ formValues, handleInputChange, reset ] = useForm( { 
        searchText: ''
    } );
    
    const {searchText} = formValues;
    
    const handleSearch = (e) => {
        e.preventDefault();
        console.log('searchText');
    }


            return (
                    <form >
                        <input 
                            type="text"
                            placeholder="Buscar Héroe"
                            name="searchText"
                            className="form-control"
                            autoComplete="off"
                            onChange={handleInputChange}
                            value = {searchText}
                        />
                        <button
                            type="submit"
                            className="btn btn-block btn-outline-success my-2"
                        >
                            Buscar...
                        </button>


                    </form>


                        )
}

```