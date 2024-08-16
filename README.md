#include<iostream>
#include<iomanip>
using namespace std ;

// function to convert celsius to fahrenheit
// cels- celsius & fahren - fahrenheit

double cels_to_fahren( double cels){
    return (cels*9.0/5.0)+32.0 ;
}

// function to convert celsius to kelvin 
// k-kelvin 

double cels_to_k(double cels){
    return (cels + 273.15) ;

}

// function to convert fahrenheit to kelvin
// fahren-fahrenheit and k-kelvin 

double fahren_to_k( double fahren) {
    return (fahren - 32.0) * 5.0/9.0 +273.15 ;
}

// function to convert fahrenheit to celsius

double fahren_to_cels( double fahren ){
    return (fahren -32.0) * 5.0/9.0 ;
}

// function to convert kelvin to celsius

double k_to_cels( double k ){
    return (k - 273.15 );
}

// function to convert kelvin to fahrenheit

double k_to_fahren( double k ){
    return (k - 273.15 ) * 9.0/5.0 +32.0 ;
}

int main(){
    double value ;
    char unit ;

    cout << "Temperature Conversion "<< endl;
    cout << " Enter the temperature value :" ;
    cin >> value ;
    cout<< "Enter the unit of measurement (C/F/K): ";
    cin >> unit ;

// setting precision for ouput 
cout<< fixed << setprecision(2);

if(unit == 'C' || unit =='c'){
    double fahren=cels_to_k(value);
    double k= cels_to_k(value);

    cout << value << "deg celsius is" << fahren <<  "deg fahrenheit is"<< k << "kelvin" << endl ;


}

else if( unit =='f' || unit == 'F'){
    double cels= fahren_to_cels(value);
    double k=fahren_to_k(value);

    cout<< value << "deg fahrenheit is " << cels <<"deg celsius and "<< k << "kelvin " << endl;
}

else if( unit == 'k' || unit=='K' ){
    double cels=k_to_cels(value);
    double fahren=k_to_fahren(value);

    cout<<value << "kelvin is" << cels << "deg celsius and " << fahren << "deg f" << endl ;

}

else{
    cout << "INVALID UNIT .Please use 'C' for celsius , 'F' for fahrenheit , or 'k' for kelvin. "<< endl;
}

return 0; 

}
