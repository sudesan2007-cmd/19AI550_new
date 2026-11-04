# Ex.No: 6  Implementation of Jumping  behaviour- Unity
### DATE:  04/11/26                                                             
### REGISTER NUMBER : 212225240161
### AIM: 
To write a program to simulate the process of jumping in Unity.
### Algorithm:
```
1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground
```
###
**Program **
```
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;
    
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space) )
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
            
        }
    }

   
}
```
### Output:

<img width="1917" height="1078" alt="Screenshot 2026-10-31 085451" src="https://github.com/user-attachments/assets/2798c0e7-6a74-4039-8e78-005608309dbb" />

<img width="1808" height="1078" alt="Screenshot 2026-10-31 085526" src="https://github.com/user-attachments/assets/36604f43-7d71-4073-a523-d7dd10789bd2" />


<img width="1917" height="1070" alt="Screenshot 2026-10-31 085553" src="https://github.com/user-attachments/assets/97d3004c-767c-47a5-a1a3-74072c1848e0" />





### Result:
Thus the simple jumping behavior was implemented successfully.
