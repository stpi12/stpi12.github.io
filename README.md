
  
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
