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
