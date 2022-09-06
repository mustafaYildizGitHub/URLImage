# URLImage
Using the Data Struct to Download Images
```swift
    override func viewDidLoad() {
        super.viewDidLoad()

        // Create URL
        let url = URL(string: "https://cdn.cocoacasts.com/cc00ceb0c6bff0d536f25454d50223875d5c79f1/above-the-clouds.jpg")!

        DispatchQueue.global().async {
            // Fetch Image Data
            if let data = try? Data(contentsOf: url) {
                DispatchQueue.main.async {
                    // Create Image and Update Image View
                    self.myImage.image = UIImage(data: data)
                }
            }
        }
    }
```

