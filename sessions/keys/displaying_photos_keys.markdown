The following code, when connected to buttons via actions and outlets, will complete the expected and extension (functionality-wise):

```
import UIKit

class ViewController: UIViewController, UIImagePickerControllerDelegate, UINavigationControllerDelegate {

    @IBOutlet weak var newImageView: UIImageView!
    var imagePicker = UIImagePickerController()

    override func viewDidLoad() {
        super.viewDidLoad()
        imagePicker.delegate = self
    }

    func imagePickerController(_ picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [String : Any]) {

        if let selectedImage = info[UIImagePickerControllerOriginalImage] as? UIImage {
            newImageView.image = selectedImage
        }
        imagePicker.dismiss(animated: true, completion: nil)
    }

    @IBAction func choosePhotoTapped(_ sender: Any) {
        imagePicker.sourceType = .photoLibrary
        present(imagePicker, animated: true, completion: nil)
    }

}
```
