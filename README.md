# Philippine Geography in .json format based 
 https://github.com/flores-jacob/philippine-regions-provinces-cities-municipalities-barangays

## Json Mapping Classes

```   
public class Region 
    {
        [JsonProperty("region_name")]
        public string Name { get; set; }
        
        [JsonProperty("province_list")]
        private Dictionary<string,Province> ProvinceList { get; set; }
    }

    public class Province
    {
       [JsonProperty("municipality_list")]
        public Dictionary<string,Municipality> Municipalities { get; set; }
    }

    public class Municipality
    { 
        [JsonProperty("barangay_list")]
        public List<string> Barangays { get; set; }
    }
```
