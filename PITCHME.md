---?color=#222222

### Software Accessibility <br><br>
##### Bhanu Chamakuri<br>[@fa[twitter]@bhanuchamakuri](https://twitter.com/bhanuchamakuri)<br>

---

### @fa[rocket] Topics to Explore Today @fa[rocket]

1. What is Accessibility?
2. Why Accessibility?
3. Understand Accountability
4. Tools we can use
5. Accessibility with Angular

---?color=#8fa33b

### What is Accessibility?

---
Getting your [app, product or software] usable by as many people as humanly possible

---?color=#8fa33b

### Why Accessibility?

---?image=assets/img/population.PNG&size=contain&color=black

---
### Some people can't

@ul[squares]

- Use a mouse
- View a screen
- See low contrast text
- Hear dialouge and music
- Understand complex language

@ulend
---

### Some people need

@ul[squares]

- Keyboard support
- Screen reader support
- High contrast text
- Captions and transcripts
- Plain language

@ulend

---?image=assets/img/Accountability.PNG&size=contain&color=black

---?image=assets/img/tools.PNG&size=contain&color=black

---

### #Ally in Angular Apps?

@ul[squares]

- Write meaningful HTML
- Enable the keyboard
- Handle focus
- Alert the user
- coverage the tests

@ulend
---?image=assets/img/meaningful_1.PNG&size=contain&color=black

---?image=assets/img/meaningful_2.PNG&size=contain&color=black

---
### Angular Unit Test

Applying a text alternative with `aria-labelledby`

```typescript
describe('mdCheckbox with provided aria-labelledby ', () => {
    let checkboxDebugElement: DebugElement;
    let checkboxNativeElement: HTMLElement;
    let inputElement: HTMLInputElement;

    it('should use the provided aria-labelledby', () => {
      fixture = TestBed.createComponent(CheckboxWithAriaLabelledby);
      
      checkboxDebugElement = fixture.debugElement.query(By.directive(MdCheckbox));
      checkboxNativeElement = checkboxDebugElement.nativeElement;

      inputElement = <HTMLInputElement>checkboxNativeElement.querySelector('input');

      fixture.detectChanges();
      expect(inputElement.getAttribute('aria-labelledby')).toBe('some-id');
  });

  /** Simple test component with aria-labelledby set. */
  @Component({
    template: `<md-checkbox aria-labelledby="some-id"></md-checkbox>`
  })
  class CheckboxWithAriaLabelledby {}
```

---
### @fa[star] Thank you. Q&A Time! @fa[star]
