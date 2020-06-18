# React-Native
- Granting Access to location

06/05/2020

---







    const Main () => {
    const [user, setUsers] = useState([]);
    const [currentRegion, setCurrentRegion] = useState(null);
    const [techs, setTechs] = useState('');

    useEffect(() => {
    async function loadInitialPosition() {
      const { granted } = await requestPermissionsAsync(); </code>

      if (granted) {
        const { coords } = await getCurrentPositionAsync({
          enableHighAccuracy: true,
        })

        const { latitude, longitude } = coords;

        setCurrentRegion({
          latitude,
          longitude,
          latitudeDelta: 0.04,
          longitudeDelta: 0.04
        })
      }
    }

    loadInitialPosition()
  }, [])
  
  
  
  
  
  --------------------------------------------------------------
