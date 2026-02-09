# symmetrical-waddle
using UnityEngine;

public class BikeActivityLoop : MonoBehaviour
{
    public float speed = 10f;
    public float turnSpeed = 50f;

    void Update()
    {
        // This loop runs once per frame (Unity handles the looping for us)
        // Let's simulate some activity: move forward and check inputs

        // Forward movement
        transform.Translate(Vector3.forward * speed * Time.deltaTime);

        // Turn based on player input
        float horizontal = Input.GetAxis("Horizontal"); // A/D or Left/Right arrows
        transform.Rotate(Vector3.up * horizontal * turnSpeed * Time.deltaTime);

        // Activity: print the bike's position every frame
        Debug.Log("Bike position: " + transform.position);
    }
}
