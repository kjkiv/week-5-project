# week-5-project
week 5 project
class Car {
    constructor(make, model) {
      this.make = make;
      this.model = model;  
    }
    
    descrcribe() {
        return '${this.make} car ${this.model}.' ;

}
}

class type {
    constructor(make) {
        this.make = make;
        this.car = [];

        
    }
    addCar(car) {
        if (car instanceof car) {
            this.car.push(car);
        }else {
            throw new Error('You can only add an instance of car. Argument is not a car: ${car}');
        }
    }

    describe() {
       return '${this.make} has $'{this.car.length} car. ';
     }
    
}
class Menu {
    constructor() {
        this.model =[];
        this.selectedmodel = num;

    }
    start() {
        let selectrion = this.showMainMenuOption
        while (selectrion != 0) {
            switch (selection ) {
                case '1' :
                  this.creatcar()
                  break;
                  case '2':
                     this.viewcar();
                      break;
                      case '3':
                        this.deletecar();
                        break;
                        case '4':
                            this.displaycar();
                            break;
                            default:
                                selectrion = 0

            }
            selectrion = this.showMainMenuOptions();
        }
        alert('see ya!');

    }
    showMainMenuOption() {
        return prompt(;'
        0) exit
        1) create new car
        2) view car
        3) delete car
        4) display all Car

        ');

    }
    displayCars() {
        let carString = '';
        for (let i = 0; i < this.car.length; i++) {
            carstring += i + ')' + this.car[i].name + '\n';
    } 
    alert(carstring);


}
creatcar() {
    let name = prompt('Enter name for new car:');
    this.car.push(new car(name));

}
viewCar() {
    let index = prompt('Enter the index of the car you wish to view');
    if (index > -1 && index < this.car.length) {
        this.selectedCar = this.car[index];
        let desctription = 'Car Name: ' + this.selectedCar.name + '\n';
        
        for(let i= 0; i < this.selectedCar.make.length; i++) {
            description += i + ') ' + this.selectedCar.make[i].model + '-' + 
            this.selectedCar.make[i].model + '\n';

        }
        let selection = this.showCarMenuOptions(desctription);
        switch (selection) {
            case '1':
                this.createCar();
                break;
                case '2':
                this.deleteCar();
            


        }
        showCarMenuOptions(carInfo) {
            return prompt('
            0) back
            1) create car
            2) delete car
            -----------------------
            ${teamInfo}
            ')

        }

    }

    this.creatcar() {
        let model = prompt('Entername of new car:');
        let make = prompt( 'Enter make for new car:');
        this.selectedCar.make.push(new car(make, model));

    }
    deleteCar() {
        let index = prompt('Enter the index of the car you wish to delete:');
        if (index > -1 && index <this.selectedCar.make.length){
            this.selectedCar.make.splice(index,1);
        }
        
    }
    deletemake() {
        let index = prompt('Eneter the index of the make you wish to delete: ');
        if (index > -1 && index < this.make.length) {
            this.make.splice(index, 1);
            
        }
    }
}

let menu = new Menu();
menu.start()
