# UltraUnitySandbox
A repository for some important game development algorithms organized in scripts.

## ToString()
Converts an int to a string:

        textField.text = myInt.ToString();
        // Where textField = TMPro text box; text = text component of textField; myInt = an int variable;
        
## FindObjectOfType<>()
Allows an object to access another class:

    // Cached references
    PlayerScore playerscore;

    private void Start()
    {
        playerscore = FindObjectOfType<PlayerScore>();
    }
