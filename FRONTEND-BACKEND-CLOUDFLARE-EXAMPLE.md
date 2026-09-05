# Frontend & Backend: Using Cloudflare Example

This is an example using only the `POST` http method, as the rest are more for ease of reading (I think, not sure).

##   BACKEND CODE:

Understand that stuff below us!
```
export default {  
    async fetch(request, env) {  
        const corsHeaders = {  
            "Access-Control-Allow-Origin": "https://frontend.com",  
            "Access-Control-Allow-Methods": "POST, OPTIONS",  
            "Access-Control-Allow-Headers": "Content-Type",  
        };  
  
        // Handle CORS preflight  
        if (request.method === "OPTIONS") {  
            return new Response(null, {  
                status: 204,  
                headers: corsHeaders  
                });  
        }  
  
        const data = await request.json();  
  
        return Response.json(  
            {  
                success: true,  
                message: "API is working!",  
                received: "'" + data.message + "', was received!",  
            },  
            { headers: corsHeaders }  
        );  
    }  
};
```

Done?

Good! Now time for the easy one!

## FRONTEND CODE:

Hi

```
const output = document.getElementById("output");  
  
async function postBackend() {  
    const response = await fetch("https://api.etkcompany.com/", {  
        method: "POST",  
  
        headers: {  
            "Content-Type": "application/json"  
  },  
  
        body: JSON.stringify({  
            message: "Ehan"  
  })  
    });  
    const data = await response.json();  
    return data;  
}  
const data = await postBackend();

console.log(data.message)
console.log(data.received)  
```

Bye
