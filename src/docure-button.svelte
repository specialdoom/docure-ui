<svelte:options tag="docure-button" />

<slot />

<style>
  :host {
    font-family: "Quicksand";
    display: inline-flex;
    justify-content: center;
    align-items: center;
    min-width: 100px;
    width: auto;
    height: 30px;
    font-size: 16px;
    background: var(--docure-button-bg, #4392f1);
    color: var(--docure-button-text, #ffffff);
    border-radius: 4px;
    border: 1px solid transparent;
    cursor: pointer;
    padding: 0 16px;
  }

  :host([primary]) {
    --docure-button-bg: #4392f1;
    --docure-button-text: #ffffff;
  }

  :host([primary]:hover) {
    --docure-button-text: #4392f1;
    --docure-button-bg: #ffffff;
    border-style: solid;
    border-color: var(--docure-button-text);
  }

  :host([secondary]) {
    --docure-button-bg: #dc493a;
    --docure-button-text: #ffffff;
  }

  :host([secondary]:hover) {
    --docure-button-bg: #ffffff;
    --docure-button-text: #dc493a;
    border-style: solid;
    border-color: var(--docure-button-text);
  }

  :host([link]) {
    --docure-button-bg: #ffffff;
    --docure-button-text: #4392f1;
  }

  :host([link]:hover) {
    text-decoration: underline;
  }

  :host([icon]) {
    min-width: 30px;
    min-height: 30px;
    background: #fff;
    border-radius: 50%;
    padding: 2px;
    border-color: #cccccc6b;
    box-shadow: rgba(0, 0, 0, 0.016) 0px 2px 0px 0px;
  }

  :host([icon]:hover) {
    border-color: #4392f1;
  }
</style>
