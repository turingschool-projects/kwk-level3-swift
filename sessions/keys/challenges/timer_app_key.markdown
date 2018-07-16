# Timer App

StoryBoard needs to be created with appropriate actions and outlets.

Code in ViewController:

```swift
import UIKit

class ViewController: UIViewController {

    var timer = Timer()
    var time = 210

    @IBOutlet weak var timeLeft: UILabel!

    @objc func decreaseTimer() {
        if time > 0 {
            time -= 1
            timeLeft.text = String(time)
        } else {
            timer.invalidate()
        }
    }

    override func viewDidLoad() {
        super.viewDidLoad()
    }

    @IBAction func pauseTapped(_ sender: Any) {
        timer.invalidate()
    }

    @IBAction func playTapped(_ sender: Any) {
        timer = Timer.scheduledTimer(timeInterval: 1, target: self, selector: #selector(ViewController.decreaseTimer), userInfo: nil, repeats: true)
    }

    @IBAction func resetTapped(_ sender: Any) {
        time = 210
        timeLeft.text = String(time)
    }

    @IBAction func decreaseTapped(_ sender: Any) {
        time -= 10
        timeLeft.text = String(time)
    }

    @IBAction func increaseTapped(_ sender: Any) {
        time += 10
        timeLeft.text = String(time)
    }

}

```
