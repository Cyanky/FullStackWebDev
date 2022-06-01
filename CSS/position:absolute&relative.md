![image](https://user-images.githubusercontent.com/91872964/171334826-f99e3656-6f9b-4ce1-a2c7-aff974006512.png)
What happens when we want to move the GreenBox but do not want to affect the layout around it?

position: relative
This is where position relative comes in. Move the green box relative to its current position to 20px from the left and top without changing the layout around it. Thus, leaving a gap for the green box where it would have been had it not been position.

Position: absolute is the opposite.

position: absolute
By applying position: absolute to the GreenBox, it will not leave any gap where it would have been. The position of the GreenBox is based on its parent position (the dotted border). Thus, moving 20px to the left and bottom from the top-left origin of the dotted border.


