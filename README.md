Target:
 - Learning about CUBE CSS (Composition, Utility, Block, Exception in order)
 - Learning the way Kevin approach css project

 Note on the usage of custom property in css
 - numbers on property name indicates the level of the property
 - ranging from 100 -> 900 from lowest to highest
 - 400 is the normal level of the property
 - Example: --fs-400 = normal font-size used in the website 

 CUBE CSS
 - use the css component that comes with css itself
 - inheritance, cascade, the way css works
 - always start at the body, since it sets majority of the base style
   
		/* first level css: doing as much as you can at your regular css */
		body {
		  font-family: "Red Hat", sans-serif;
		  font-size: var(--fs-400);
		  font-weight: var(--fw-400);
		  line-height: 1.6;
		  color: var(--c-neutral-400);
		  background: var(--c-primary-200);
		}
		
		h1,
		h2,
		h3 {
		  line-height: 1.1;
		}
		
		h2 {
		  font-size: var(--fs-700);
		  color: var(--c-neutral-800);
		}


- Composition and Utility
  - composition vs utility => separation of concern (layout and other styling)
  - utility class allows us to take advantage of the cascade
    - this is a styling class
  - composition: spacing + cascade
    - sort of utility class in a way
    - this is a layout class!

- Grouping (Andy Bell's strategy to make classes more clear)
  - add [ ] around the classes that you wanna group
  - separate the composition, utility, block and exceptions classes 
  - [ xxx ]: make sure there are 1 space around the classes, otherwise it wouldn't work

- Exception: instead of using a modifier, it use a data attribute
  - why called exception?
    - sometimes a button can have different versions:
      - some with background on, some don't
      - some with color white, some don't
      - those that are different are called "exception"!

  - In BEM
    - we used modifier to address this issue
    - Benefit:
      - we can add multiple modifier on the element (also a bad thing)

  - In CUBE CSS
    - we used data attribute to address this issue
    - Benefit:
      - we can add one type of data modifier on the element (a good thing)
      - we can use data attribute as a hook to hook into js and change it


Conclusion:
- composition class allows us to plug the html elements within the composition class without worries about breaking the structure (no rigid)
- this approach allows us to reduce the styling on the block component!
