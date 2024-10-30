# Junior Full-stack Developer
## Presman Vadim <img src="/5219997956596426698.jpg" alt="photo" height = 300px width = 300px>
### Contact information:
* phone number: +375(25)620-81-11/+48(500)254-227
* e-mail: vadim.presman@gmail.com
* linkedIn: [linkedIn](https://www.linkedin.com/in/vadimpresman/)
### About my self
Enthusiastic and motivated full-stack developer with a strong foundation in programming and a keen interest in leveraging technologies to build robust and scalable applications. Eager to learn and grow in a dynamic and challenging environment where I can contribute my skills and gain valuable industry experience.
### Skills
**Front-end** Technologies: **JavaScript, HTML, CSS**
===
**Back-end** Technologies: **C#, SQL, ASP.NET Core, Entity Framework, RESTful APIs**
### Code example
**Admin controller for my API:**
```
public class AdminController : ControllerBase
{
    private readonly DishDeliveryContext _dishDeliveryContext;
    private readonly GetAllDishesService _dishGetAllDishesService;

    private readonly IMapper _mapper;

    public AdminController(DishDeliveryContext dishDeliveryContext)
    {
        _dishDeliveryContext = dishDeliveryContext;
    }

    [HttpGet("api/admin/getDishs")]
    public async Task<ICollection<GetAllDishesDto>> GetDishs()
    {
        return await _dishGetAllDishesService.GetAllDishes();
    }

    [HttpPost("api/admin/addDishs")]
    public async Task<ActionResult> AddDishs(string dishName, int price)
    {
        var dish = new Dish
        {
            DishName = dishName,
            Price = price
        };

        await _dishDeliveryContext.AddAsync(dish);
        var lineCount = await _dishDeliveryContext.SaveChangesAsync();

        return Ok();
    }

    [HttpDelete("api/admin/deleteDish/{deleteDishId:int}")]
    public async Task<ActionResult> DeleteDishs(int deleteDishId)
    {
        List<Dish> dishList = _dishDeliveryContext.Dishes.ToList();
        
        foreach (var dish in dishList)
        {
            
        }

        return Ok();
    }
}
```
### Experience
**Software Developer | TWNSD**				*September 2023 – December 2023*
- Developed an admin panel, implementing filters for rapid product identification on the website, accelerating the search process and ensuring timely data updates. Also increased the efficiency of some requests through optimization.

**Software Developer | RUE Belpochta**				*January 2021 – March 2022*
- Engineered a parcel tracking system with automatic report generation and storage, replacing an outdated system. Resulted in a significant boost in parcel processing speed and report generation efficiency.
### Education
* Akademia Finansów i Biznesu Vistula				*October 2024 – April 2027*
  Faculty of Information Technology

* Tinkoff Algorithms and Data Structures Course			*February 2024 – June 2024*
  Algorithms and Data Structures

* Advanced Web Development Course at TeachMeSkills 		*October 2022 – May 2023*
  Back-end technology with ASP.NET Core

* Belarussian State Academy of Communications			*Sept. 2019 – April 2022*
  Faculty of Information Technology
### Language skills
* ***Russian(native)***
* ***English(B2)***
* ***Polish(B1)***