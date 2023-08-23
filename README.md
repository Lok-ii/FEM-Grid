# FEM-Grid

Hosted Link:- https://lok-ii.github.io/FEM-Grid/


![Screenshot 2023-08-23 181242](https://github.com/Lok-ii/FEM-Grid/assets/129180844/8ab7a6a6-d41c-4a78-b9f2-981dd2526500)
![Screenshot 2023-08-23 181247](https://github.com/Lok-ii/FEM-Grid/assets/129180844/b2982b03-18fa-4fe8-9ba7-5b6c8acde7af)
![Screenshot 2023-08-23 181254](https://github.com/Lok-ii/FEM-Grid/assets/129180844/8c3c5a6c-0f00-4e62-a2fd-8cc1b41f32e1)
![Screenshot 2023-08-23 181259](https://github.com/Lok-ii/FEM-Grid/assets/129180844/0d104bb4-2e5f-4bd0-ae8b-dd7e9c48c10f)
![Screenshot 2023-08-23 181304](https://github.com/Lok-ii/FEM-Grid/assets/129180844/f4c3ebd1-01a2-4548-98a5-283076115eef)

    <main>: Represents the main content area of the webpage.
        <div class="daniel reviews">: A <div> element with classes "daniel" and "reviews" for styling purposes.
            <div class="user">: A container for user details.
                <img src="./assets/image-daniel.jpg" alt="Daniel Clifford" />: An image of the user with alt text.
                <div class="username">: Contains user's name and status.
                    <h5>Daniel Clifford</h5>: User's name.
                    <p class="verified">Verified Graduate</p>: User's status.
            <h3>I received a job offer mid-course...</h3>: A heading for the user's review title.
            <p class="testimonial">“ I was an EMT for many years...</p>: A paragraph for the user's testimonial.
    
    The structure is repeated for other reviews (Jonathan, Jeanette, Patrick, Kira).

![Screenshot 2023-08-23 181525](https://github.com/Lok-ii/FEM-Grid/assets/129180844/6851d1df-aba7-49ae-8e47-1387c2eda0f3)

    CSS:
        body:
            
            background-color: #edf2f9: Sets the background color of the entire webpage to a light blueish-gray.
            font-family: "barlow semi condensed", sans-serif: Specifies the font family for the text content. It uses the "Barlow Semi Condensed" font if available, or falls back to a generic sans-serif font.
            
        main:
            
            display: grid: Turns the <main> element into a grid container, allowing its child elements to be arranged in a grid layout.
            grid-template-areas: Defines the grid structure of the main content for different screen widths using area names. This property changes based on media queries.
            gap: 1.5rem, gap: 2rem, ...: Adds spacing between the grid items (review sections) based on different screen widths.
            margin-inline: auto: Centers the main content horizontally by setting the left and right margins to "auto".
            padding: 1rem, padding: 2rem, ...: Adds internal padding to the main content area based on different screen widths.
            
        .reviews:
            
            border-radius: 0.5rem: Adds rounded corners to the review sections.
            padding: 2.5rem 2rem: Sets top and bottom padding to 2.5rem and left and right padding to 2rem.
            color: white: Sets the text color inside the review sections to white.
            box-shadow: 2.5rem 3.75rem 3rem -3rem rgba(0, 0, 0, 0.3): Applies a shadow effect to the review sections using box-shadow.
            
        .reviews img:
            
            border-radius: 50%: Makes the user profile images circular by setting their border-radius to 50%.
            width: 1.7rem, height: 1.7rem: Sets the width and height of the user profile images to 1.7rem.
            
        .reviews h5, .reviews h3, .verified, .testimonial:
            
            font-weight: 500: Specifies the font weight of these elements as 500 (semibold).
            opacity: 0.5, opacity: 0.7: Adjusts the opacity (transparency) of these elements to control their visibility.
            .daniel, .jonathan, .jeanette, .patrick, .kira:
            
            background-color: Sets the background color of each review section based on the reviewer's name.
            grid-area: Specifies the layout position of each review section using grid areas defined in the main element's grid-template-areas.
        
        .user:
            
            display: flex: Turns the .user element into a flex container, arranging its child elements horizontally in a row.
            gap: 1em: Adds spacing between the child elements (user image and username).
            align-items: center: Vertically aligns the child elements along their center points.
            margin-top: -0.4rem: Adjusts the top margin of the .user element to slightly overlap the review heading above it.


        Media Queries:
        
            @media only screen and (min-width: 528px): 
            
                This media query targets screens with a minimum width of 528 pixels and wider, typically including small tablets and larger smartphones in landscape mode.
                main: The grid-template-columns property is adjusted to create a grid layout with two equally sized columns.
                grid-template-areas: The grid areas for the review sections are defined based on the desired arrangement, using the names assigned to each section. The layout consists of five rows and two columns, where each area corresponds to a review section.
                padding: 1rem: A padding of 1rem is applied to the main element to provide spacing between the content and the edges of the screen.
                
            @media only screen and (min-width: 608px):
                
                This media query targets screens with a minimum width of 608 pixels and wider, encompassing larger tablets and small laptops.
                main: The grid-template-columns property remains unchanged from the previous media query, maintaining the two-column grid layout.
                grid-template-areas: The arrangement of review sections in the grid is adjusted. Now, the two and three sections are placed in the same row as the five section, providing a different visual layout.
                padding: 2rem: The padding around the main content is increased to 2rem, offering more space between the content and the edges of the screen.
               
            @media only screen and (min-width: 864px):
                
                This media query targets screens with a minimum width of 864 pixels and wider, generally covering larger laptops and desktop displays.
                main: The grid-template-columns property is updated to create a grid layout with three equally sized columns.
                grid-template-areas: The arrangement of review sections in the grid is further customized. The one, two, and five sections share the top row, while the three, four, and five sections are distributed across the remaining rows.
                padding: 2rem: The padding around the main content remains consistent at 2rem.
                
            @media only screen and (min-width: 1200px):
                
                This media query targets screens with a minimum width of 1200 pixels and wider, generally applicable to larger desktop monitors.
                main: The grid-template-areas property is defined to create a customized grid arrangement for the review sections. The layout consists of two rows and four columns.
                grid-template-columns: The grid columns are set to four, each occupying an equal fraction of the available space.
                padding: 4.5rem 13rem: The padding around the main content is significantly increased to provide ample spacing around the content.
