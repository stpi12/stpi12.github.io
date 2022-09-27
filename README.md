
  
    Button("Click here"){
    
    }
    @State var colorMe = false
    var body: some View {
        
        VStack{
            Ellipse().fill(RadialGradient(gradient: Gradient(colors: [.blue, .yellow]), center: .top, startRadius: 10, endRadius: 65))
            Image("flag").resizable().aspectRatio(contentMode: .fill).frame(width: 150, height: 50)
            Button {
                // code to run
            } label: {
                Label("Image button", systemImage: "hare.fill").font(.largeTitle).foregroundColor(.purple).padding().border(Color.blue, width: 6)
            }
            
            // don't forget @State var
            Button {
                colorMe.toggle()
            } label: {
                Label("Image button", systemImage: "hare.fill").font(.largeTitle).foregroundColor(.purple).padding().border(Color.blue, width: 6)
            }
        
        }
    }
    
    struct ContentView: View {
        @State private var selectedColor = Color.gray
        var body: some View {
            VStack (spacing: 28) {
                Rectangle().fill(selectedColor)
                Picker("Favorite Color", selection: $selectedColor, content: { 
                    Text("Red").tag(Color.red)
                    Text("Green").tag(Color.green)
                    Text("Blue").tag(Color.blue)
                }).pickerStyle(SegmentedPickerStyle())
        }
        
    }
    
    struct ContentView: View {
    @State private var message = ""
    var body: some View {
        VStack (spacing: 28) {
            Text(message)
            Picker("", selection: $message, content: {
                Text("Happy").tag("happy")
                Text("Sad").tag("sad")
                Text("Bored").tag("bored")
            }).pickerStyle(SegmentedPickerStyle()).onChange(of: message) { newValue in switch newValue {
            case "happy": message = "Be happy and joyous"
            case "sad": message = "Life can be a struggle at times"
            case "bored": message = "Look for your purpose"
            default:
                break
            }}
            }
        
        }
    }
}
