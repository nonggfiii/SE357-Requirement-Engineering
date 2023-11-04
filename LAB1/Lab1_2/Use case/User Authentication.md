@startuml left to right direction

actor Admin as "Admin" actor Customer as "Customer"

rectangle "User Authentication" { usecase (Sign In) as "Sign In" usecase (Sign Up) as "Sign Up" usecase (Reset Password) as "Reset Password" usecase (Create Account) as "Create Account" usecase (Send Recovery Mail) as "Send Recovery Mail" }

Customer --> (Sign In) Customer --> (Sign Up) Customer --> (Reset Password)

Admin --> (Sign In) Admin --> (Sign Up) Admin --> (Reset Password) Admin --> (Create Account) (Reset Password) .> (Send Recovery Mail) : include

@enduml
