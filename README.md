# **Modal Window**  
#### Inspired by [Jonas Schmedtmann](https://github.com/jonasschmedtmann) || See it live at [CodePen](https://codepen.io/shady-ashraf/pen/ZYzGWVK)
###### *Modal Window* is an interactive component that overlays the current page content, typically used to display important information or actions. This project demonstrates event-driven JavaScript and dynamic HTML-CSS interactions.

---

## **Table of Contents**  
- [Overview](#overview)  
- [Features](#features)  
- [File Structure](#file-structure)  
- [HTML Details](#html-details)  
- [CSS Styling](#css-styling)  
- [JavaScript Logic](#javascript-logic)  
- [Deployment](#deployment)  
- [Selectors Used in the Project](#selectors-used-in-the-project)  

---

## **Overview**  
The **Modal Window Project** showcases a modal component that can be triggered by multiple buttons. The modal overlay enhances user focus by dimming the rest of the screen.  

**Technologies used:**  
- HTML5  
- CSS3  
- JavaScript (ES6)  

---

## **Features**  
- **Modal Activation**: Multiple buttons open the same modal.  
- **Close Modal**: Users can close the modal via a close button, clicking outside the modal, or pressing the "Escape" key.  
- **Dynamic Styling**: Modal and overlay appear smoothly over the current content.  

---

## **File Structure**  
```plaintext
modal-window/
├── index.html  
├── style.css  
└── script.js  
```  

---

## **HTML Details**  
The HTML file (`index.html`) structures the modal and its triggers.

### Key Sections:  
1. **Trigger Buttons**:  
   Buttons with the `.show-modal` class open the modal window.  
   ```html  
   <button class="show-modal">Show modal 1</button>  
   <button class="show-modal">Show modal 2</button>  
   <button class="show-modal">Show modal 3</button>  
   ```  

2. **Modal Component**:  
   Includes a close button, heading, and descriptive text.  
   ```html  
   <div class="modal hidden">  
     <button class="close-modal">&times;</button>  
     <h1>I'm a modal window 😍</h1>  
     <p>  
       Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod  
       tempor incididunt ut labore et dolore magna aliqua.  
     </p>  
   </div>  
   ```  

3. **Overlay**:  
   A semi-transparent overlay (`.overlay`) dims the background.  

---

## **CSS Styling**  
The CSS file (`style.css`) provides a modern and responsive look.

### Key Styles:  
- **Modal and Overlay**:  
  - Modal appears centered on the screen.  
  - Overlay uses `rgba` for transparency and `backdrop-filter` for a blurred effect.  

- **Buttons and Typography**:  
  - Buttons have rounded corners and hover effects for interactivity.  
  - Typography uses a clean sans-serif font for readability.  

### Snippet:  
```css  
.modal {  
  position: absolute;  
  top: 50%;  
  left: 50%;  
  transform: translate(-50%, -50%);  
  width: 70%;  
  background-color: white;  
  padding: 6rem;  
  border-radius: 5px;  
  z-index: 10;  
}  

.overlay {  
  position: absolute;  
  top: 0;  
  left: 0;  
  width: 100%;  
  height: 100%;  
  background-color: rgba(0, 0, 0, 0.6);  
  backdrop-filter: blur(3px);  
}  
```  

---

## **JavaScript Logic**  
The JavaScript file (`script.js`) handles modal interactions.

### Key Functions:  
1. **Opening the Modal**:  
   Adds event listeners to `.show-modal` buttons to display the modal and overlay.  
   ```javascript  
   const openModal = function () {  
     modal.classList.remove("hidden");  
     overlay.classList.remove("hidden");  
   };  
   ```  

2. **Closing the Modal**:  
   Closes the modal via close button, overlay click, or "Escape" key.  
   ```javascript  
   const closeModal = function () {  
     modal.classList.add("hidden");  
     overlay.classList.add("hidden");  
   };  
   ```  

3. **Keydown Events**:  
   Detects the "Escape" key and closes the modal if open.  
   ```javascript  
   document.addEventListener("keydown", function (e) {  
     if (e.key === "Escape" && !modal.classList.contains("hidden")) {  
       closeModal();  
     }  
   });  
   ```  

---

## **Deployment**  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/shadyashraf174/Modal.git  
   ```  
2. Open `index.html` in a web browser to interact with the modal.  

---

## **Selectors Used in the Project**  

### **HTML Selectors**  
- **Element Selectors**:  
  - `<div>`: Defines modal and overlay containers.  
  - `<button>`: Triggers and closes the modal.  

- **Class Selectors**:  
  - `.show-modal`: Styles trigger buttons.  
  - `.modal`: Styles the modal container.  
  - `.overlay`: Styles the dimmed background.  

### **CSS Selectors**  
- **Pseudo-classes**:  
  - `button:hover`: Adds hover effects.  
- **Dynamic Styling**:  
  - `hidden` class toggles `display: none`.  

---

![image](https://github.com/user-attachments/assets/732c2a96-7135-44f2-afcc-fc85875d922f)
![image](https://github.com/user-attachments/assets/6b6d9941-32c0-4419-b992-c8c68aa0313a)

