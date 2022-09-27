
  
    Button("Click here"){
    
    }

    var body: some View {
        
        VStack{
            Ellipse().fill(RadialGradient(gradient: Gradient(colors: [.blue, .yellow]), center: .top, startRadius: 10, endRadius: 65))
            Image("flag").resizable().aspectRatio(contentMode: .fill).frame(width: 150, height: 50)
        
        }
    }
