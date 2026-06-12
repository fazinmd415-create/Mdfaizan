using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed = 5.0f;

    void Update()
    {
        // Keyboard arrow keys ya WASD se input lene ke liye
        float moveHorizontal = Input.GetAxis("Horizontal");
        float moveVertical = Input.GetAxis("Vertical");

        // Movement direction tayar karna
        Vector3 movement = new Vector3(moveHorizontal, 0.0f, moveVertical);

        // Player ko move karna
        transform.Translate(movement * speed * Time.deltaTime, Space.World);
    }
}

