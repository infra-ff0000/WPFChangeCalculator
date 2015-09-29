using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace _06ChangeCalculator
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
      //  private object labelHundreds;

        public MainWindow()
        {
            InitializeComponent();
        }


        private void Enter (object sender, RoutedEventArgs e)
        {

            decimal price = decimal.Parse(textBox.Text);
			//string priceinput = textBox.text;
			//Message.Box("Please enter change");
            decimal givenAmount = decimal.Parse(textBox_Copy.Text);

            decimal change = decimal.Parse(textBox1.Text);

            decimal _change = givenAmount - price;

         

            decimal Hundreds = System.Math.Floor(change / 100.00m);
            decimal numberofFifties = System.Math.Floor((change % 100.00m) / 50.00m);
            decimal numberofTwenties = System.Math.Floor((change % 50.00m) / 20.00m);
            decimal numberofTens = System.Math.Floor((change % 20.00m) / 10.00m);
            decimal numberofFives = System.Math.Floor((change % 10.00m) / 5.00m);
            decimal numberofDollars = System.Math.Floor(change % 5.00m / 1.00m);
            decimal numberofHalfDollars = System.Math.Floor(change % 1.00m / 0.50m);
            decimal numberofQuarters = System.Math.Floor((change % 0.50m) / 0.25m);
            decimal numberofDimes = System.Math.Floor((change % 0.25m) / 0.10m);
            decimal numberofNickels = System.Math.Floor(change % 0.10m / 0.05m);
            decimal numberofPennies = System.Math.Floor(change % .05m / 0.01m);

            // numberofHundredsdenom.Content = numberofHundreds.ToString();
          

            object labelChange = null;
          //  _change.Content = "" + _change.ToString;
           // labelHundreds.textBox("Hundreds:" + Hundreds);
          //  labelHundreds.Content("Fifties:" + numberofFifties);
           // labelHundreds.Content("Twenties:" + numberofTwenties);
           // labelHundreds.Content("Tens:" + numberofTens);
           // labelHundreds.Content("Fives:" + numberofFives);
           // labelHundreds.Content("Dollars:" + numberofDollars);
            //labelHundreds.Content("Half Dollars:" + numberofHalfDollars);
           // labelHundreds.Content("Quarters:" + numberofQuarters);
           // labelHundreds.Content("Dimes:" + numberofDimes);
           // labelHundreds.Content("Nickels:" + numberofNickels);
            //labelHundreds.Content("Pennies:" + numberofPennies);
            
        }
            private void Close_Click(object sender, RoutedEventArgs e)
        {
            Environment.Exit(0);

        }
            }
        }
