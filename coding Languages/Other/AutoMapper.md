# AutoMapper

## simple example

```c#
            CreateMap<FormRelatedDTO, FormRelatedEntity>().ReverseMap();
```

## if have instance inside other instance

example and we want class A and from B just the id

```C#
A a = new A
{
    AId = 1,
    AName = "Instance of A",
    BInstance = new B
    {
        BId = 10,
        BName = "Instance of B", 

    }
};
```

```c#
   //form
            CreateMap<FormRelatedDTO, FormRelatedEntity>()
                .ForMember(dest => dest.RelatedForm,
                    opt => opt.MapFrom(src => new FormEntity { ID = src.RelatedFormID }))
                .ReverseMap()
                .ForMember(dest => dest.RelatedFormID,
                    opt => opt.MapFrom(src => src.RelatedForm.ID));
```
