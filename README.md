# Lab-8_202001129

**Name: Deep Jaimesh Shah**  
**ID: 202001129**  

### Creating a new Eclipse project, and within the project, create a package and defining the class

![image](https://user-images.githubusercontent.com/77284852/233316713-eb1bf1f2-0a67-436e-8612-941d6a328ad5.png)


### Adding the Test Case

    public class BoaTest {
      Boa jen;
      Boa ken;

      @Before
      public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa ("Kenneth", 3, "granola bars");
      }

      @After
      public void tearDown() throws Exception {
      }

      @Test
        public void testIsHealthy() {
            assertTrue(ken.isHealthy()); // kens favourite food is granola bars
            assertFalse(jen.isHealthy());
        }

        @Test
        public void testFitsInCage() {
            assertFalse(ken.fitsInCage(2));
            assertFalse(ken.fitsInCage(3));
            assertTrue(ken.fitsInCage(5));

            assertFalse(jen.fitsInCage(1));
            assertFalse(jen.fitsInCage(2));
            assertTrue(jen.fitsInCage(3));
        }
    }

### Running the Test Case

![image](https://user-images.githubusercontent.com/77284852/233316489-ade24cd5-4c6e-4659-a069-3944d36546c1.png)


### Adding a new method to the Boa class

	public int lengthInInches(){
		// 1 foot is 12 inches
		return this.length*12;
	}

![image](https://user-images.githubusercontent.com/77284852/233317319-8ad5162c-0b21-4cc2-935b-0701b0bef6a7.png)


### Adding new test cases to test lengthInInches()

    @Test
    public void testlengthInInches() {
    	assertEquals("error in lengthInInches()",  36, ken.lengthInInches());
    	assertNotEquals("error in lengthInInches()",  35, ken.lengthInInches());
        
    	assertEquals("error in lengthInInches()",  24, jen.lengthInInches());
    	assertNotEquals("error in lengthInInches()",  30, jen.lengthInInches());
    }
    
### Running the new Test Case

![image](https://user-images.githubusercontent.com/77284852/233317554-473aeeca-9267-4595-a700-eebfbad05dff.png)
