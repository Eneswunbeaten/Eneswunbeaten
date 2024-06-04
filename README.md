```csharp
using DevExpress.Mvvm.Native;
using System;
using System.Collections.Generic;
using System.Linq;

namespace GithubProfile
{
    class Program
    {
        static void Main(string[] args)
        {
            var profile = new Dictionary<string, string>
            {
                ["Name"] = "Hasan Enes",
                ["Location"] = "Turkey/Antalya",
                ["Occupation"] = ".Net Developer",
                ["Software_Languages"] = "C#, Python, Javascript, Typescript, ",
                ["Areas_of_Interest"] = "Backend, Web Development, Cyber Sec."
            };

            Console.WriteLine("Hello! I'm {0}, I'm a {1} in {2}",
                profile["Name"], profile["Occupation"], profile["Location"]);

            Console.WriteLine("Programming languages I am proficient in: {0}.",
                profile["Software_Languages"]);

            Console.WriteLine("Areas of interest to me: {0}.",
                profile["Areas_of_Interest"]);

            var best_projects = new Dictionary<string, string>
            {
                ["Menu Plus"] = @"You can switch the menus in the restaurant to qr system and place orders through this system.
                                 It is not open source but you can access it from https://menuplus.com.tr.",

                ["Csv Tool"] = @"You can upload the csv file and convert it to C# Model, Mongo Insert Command, Sql Insert Commands.
                                 In addition, even if the column names are not available in the first line of the csv file,
                                 you can continue your operations by manually entering them.",

                ["CarBook"] = @"It is a car rental project I made with mvc.
                               You can update many detailed sections such as vehicle, brand via the admin panel."
            };

            Console.WriteLine("Some of my projects:");
            best_projects.ForEach(proje => Console.WriteLine("- {0}", proje));

            Console.WriteLine("Don't forget to check out the other repositories in my profile!");
        }
    }
}
```
