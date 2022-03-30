
## Preparation tasks (done before the lab at home)

A common way to control multiple displays is to gradually switch between them. We control (connect to supply voltage) only one of the displays at a time, as can be seen [here](https://engineeringtutorial.com/seven-segment-display-working-principle/).

Due to the physiological properties of human vision, it is necessary that the time required to display the whole value is a maximum of 16&nbsp;ms. If we display four digits, then the duration of one of them is 4&nbsp;ms. If we display eight digits, the time is reduced to 2&nbsp;ms, etc.

1. See [schematic](https://github.com/tomas-fryza/Digital-electronics-1/blob/master/docs/nexys-a7-sch.pdf) or [reference manual](https://reference.digilentinc.com/reference/programmable-logic/nexys-a7/reference-manual) of the Nexys A7 board, find out the connection of 7-segment displays, and complete the signal timing to display four-digit value `3.142`.
![Screenshot 2022-03-30 135634](https://user-images.githubusercontent.com/99871518/160829116-d8fd5978-f10e-4e7c-a236-75675888b92f.png)

  ![Screenshot 2022-03-30 135623](https://user-images.githubusercontent.com/99871518/160829131-14ba76af-e886-41e8-a271-c51dded20eaf.png)


  > The figure above was created in [WaveDrom](https://wavedrom.com/) digital timing diagram online tool. The figure source code is as follows:
  >
  ```javascript
  {
    signal:
    [
      ['Digit position',
        {name: 'Common anode: AN(3)', wave: 'xx01..01..01'},
        {name: 'AN(2)', wave: 'xx101'},
        {name: 'AN(1)', wave: 'xx1.'},
        {name: 'AN(0)', wave: 'xx1.'},
      ],
      ['Seven-segment data',
        {name: '4-digit value to display', wave: 'xx3333555599', data: ['3','1','4','2','3','1','4','2','3','1']},
        {name: 'Cathod A: CA', wave: 'xx01.0.1.0.1'},
        {name: 'Cathod B: CB', wave: 'xx0.'},
        {name: 'CC', wave: 'xx0.'},
        {name: 'CD', wave: 'xx01'},
        {name: 'CE', wave: 'xx1.'},
        {name: 'CF', wave: 'xx1.'},
        {name: 'Cathod G: CG', wave: 'xx01'},
      ],
      {name: 'Decimal point: DP', wave: 'xx01..01..01'},
    ],
    head:
    {
      text: '                    4ms   4ms   4ms   4ms   4ms   4ms   4ms   4ms   4ms   4ms',
    },
  }
  ```

