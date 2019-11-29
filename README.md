# Pink Trombone Timeline Editor
Video - https://twitter.com/ConcreteSciFi/status/1200218613669449728
 
## Setup
Click anywhere on the screen to start the various audio contexts (there's 3: one for the pink trombone, one for the pitch detector, and one for the phoneme classifier. The latter 2 each use different versions of TensorFlow so I had to put them in their own iFrames)
 
## Basic Controls
- ctrl+click on the timeline to add a key phoneme
- alt+click a key phoneme to select it
- after selecting a phoneme, you can change values and select "set" to apply changes

## Creating your own Teachable Machine to detect phonemes
1. Download the template .tm file at https://github.com/zakaton/pink-trombone-editor/blob/master/phoneme-classifier-template.tm
2. Go to https://teachablemachine.withgoogle.com/train/audio
3. Select "Open project from file" and choose the downloaded template file
4. For each phoneme classification (including "Background Noise"), select "Remove all Samples" and replace them with your own recordings.
5. Select "Train Model" and wait for it to finish
6. Select "Export Model" and choose "Upload my Model"
7. Copy the sharable link and assign it to the URL constant in the phoneme classifier file at https://github.com/zakaton/pink-trombone-editor/blob/master/phoneme-classifier/index.html
