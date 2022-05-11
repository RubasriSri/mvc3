# mvc3                                                                                                                                                               using System;

using System.Collections.Generic;

using System.Linq;

using System.Web;

using System.Web.Mvc;


namespace ASP_App1.Controllers //DO NOT change the namespace name

{

  public class Ex1Controller : Controller //DO NOT change the class name

  {

    List<String> breakingNews = new List<String>() //DO NOT change this declaration and values

    {

      "PM visit brings business",

      "10% slash in GST",

      "Top Player announced retirement",

      "India wins series"

    };


    // Implement 'NewsByChoice' action  

    public ActionResult NewsByChoice(int id)

    {

     string news=breakingNews[id-1];

     return Content(news,"text/html");

    }

    

    // Implement 'AllNews' action

    public ActionResult AllNews()

    {

      string allNews="";

      foreach(string news in breakingNews)

      {

        allNews=allNews+"/n"+news;

      }

      return Content(allNews,"text/html");

    }

    

  }

}
