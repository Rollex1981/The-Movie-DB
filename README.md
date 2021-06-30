# The-Movie-D



import SwiftUI


let lightGreyColor = Color(red: 239.0/255.0, green: 243.0/255.0, blue: 244.0/255.0, opacity: 1.0)


struct ContentView: View {
    
   @State var username: String = ""
    @State var password: String = ""
    var body: some View {
        
        VStack {
            WelcomeText()
            UserImage()
            TextField("UserImage", text: $username)
                .padding()
                .background(lightGreyColor)
                .cornerRadius(5.0)
                .padding(.bottom, 20)
            SecureField("Password", text: $password)
                .padding()
                .background(lightGreyColor)
                .cornerRadius(5.0)
                .padding(.bottom, 20)
            Text("SING UP")
                .font(.headline)
                .foregroundColor(.white)
                .padding()
                .frame(width: 220, height: 60)
                .background(Color.accentColor)
                .cornerRadius(15.0)
        }
    }
            struct UsernameTextField: View {
                @Binding var username: String
             var body: some View {
                return TextField("Username", text: $username)
                    .padding()
                    .background(lightGreyColor)
                    .cornerRadius(5.0)
                    .padding(.bottom, 20)
            
      }
    }

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}

struct WelcomeText: View {
    var body: some View {
        Text("THE MOVIE DB")
            .foregroundColor(.accentColor)
            .font(.largeTitle)
            .fontWeight(.semibold)
            .padding(.bottom, 20)
    }
}

struct UserImage : View {
    var body: some View {
       Image("userImage")
    .resizable()
    .aspectRatio(contentMode: /*@START_MENU_TOKEN@*/.fill/*@END_MENU_TOKEN@*/)
    .frame(width: 150, height: 150)
    .clipped()
    .cornerRadius(150)
    .padding(.bottom, 75)
        
     }
   }
 
}
