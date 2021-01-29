# Igor Lyatskiy

## Contacts:
- E-mail: 
	- igor.lyatskiy@gmail.com
	- igor.lyatskiy@mail.ru
- Phone number: +375296564832

## Short information about me:

Studying is my aim. I really want to get some new professional skills in Frontend-development, I really like this direction. That's why I'm here.
I don't have any experince, I'm just a student from the BSU who wants to develop his skills and who can do this, I hope. I think, I'm a hardworking person.

## My skills:
- HTML5
- CSS3
- Basic Git practise
- Basic C++
- Basic JS, also node.js
- Some simple frameworks (for example, Bootstrap)

## Code:
    	location /streets {
        
        lua_code_cache off;
        content_by_lua_block { 
            response = ngx.location.capture (
                                    '/api/v1/streets', { 
                                    always_forward_body = true, 
                                    copy_all_vars = true})

            if response.status > 500 then 
                ngx.exit(response.status)
            end

            local cjson = require("cjson")
            streets = cjson.decode(response.body)


            local template = require "resty.template";
            local template_string = ngx.location.capture("/templates/lua/streets.html")

            template.render(template_string.body, {
                items = streets
      	      })          
    	    }
   	 }

## Courses:
- Summer camp from "ШАГ", 2016
- IT-camp MyFreedom, 2017
- BSU IT-school for high school students, 2019

## Education:
- Belarusian State University, 1st year

## English: 
**CEFR level B1, Streamline, 2016**