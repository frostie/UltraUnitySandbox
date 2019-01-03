# UltraUnitySandbox
A repository for some important game development algorithms organized in scripts.

## ToString()
Converts an int to a string:

    textField.text = myInt.ToString();
    // Where textField = TMPro text box; text = text component of textField; myInt = an int variable
        
## FindObjectOfType<>()
Allows an object to access another class:

    private void Start()
    {
	FindObjectOfType<PlayerScore>().AddPoints(); // Accesses PlayerScore class and calls AddPoints() method
    }

## Time.timeScale()
Sets time scale / game speed:
    
    [Range(0.1f, 10f)] [SerializeField] float gameSpeed = 1f;

	void Update () 
    {
        Time.timeScale = gameSpeed;
    }

## DontDestroyOnLoad()
Ensures game object is not destroyed when transitioning to next scene:

	DontDestroyOnLoad(gameObject);

## transform.position
Moves paddle from left to right using mouse pointer direction:

    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class Paddle : MonoBehaviour {

    // Configuration Parameters
    [SerializeField] float screenWidthInUnits = 16f;
    [SerializeField] float minX = 1.28f;
    [SerializeField] float maxX = 14.71f;

	void Start () 
    {
		
	}
	
	void Update () 
    {
        float mousePosInUnits = Input.mousePosition.x / Screen.width * screenWidthInUnits;
        Vector2 paddlePos = new Vector2(mousePosInUnits, transform.position.y);
        paddlePos.x = Mathf.Clamp(mousePosInUnits, minX, maxX);
        transform.position = paddlePos;
	}
}
