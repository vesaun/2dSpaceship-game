# 2dSpaceship-game
Unity 3D developed 2d endless game using C#.

In order to allow the camera to follow the player, we used Vector3 (struct) in order to follow the X, Y, and Z positions of the player.
Game over scene displayed uses a tagged player object, with ability to replay game.
(using UniteEngine.SceneManagement;)

To loop the background image, we use Vector2 (object) to follow the X and Y positions of the object. 
Use a renderer to execute.

Used a musicManager in order to continue the music during and after "death" in the game.

Tagged obstacles with "border" and created a 2D rigidbody on each object. Froze y values of transform and used physics to create collision. Implemented gameOver script upon collision.

Allowed for user input to control a Vector2 object to manipulate the X and Y positions of the player, using Input.GetAxisRaw("Vertical").

Score kept track following time.deltaTime in order to follow the computer's refresh rate as opposed to FixedUpdate() which calls during each frame update. 
example : score += scoreRate * time.deltaTime;
