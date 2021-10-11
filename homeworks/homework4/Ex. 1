using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace triangle
{
    static class Program
    {
        public class Triangle
        {
            protected double side1, side2, side3;
            public Triangle(double a, double b, double c)
            {
                side1 = a;
                side2 = b;
                side3 = c;
            }
            public double GetParam()
            {
                return side1 + side2 + side3;
            }
            public List<double> GetAngles()
            {
                double a = Math.Acos((side2 * side2 + side3 * side3 - side1 * side1) / (2 * side2 * side3));
                double b = Math.Acos((side1 * side1 + side3 * side3 - side2 * side2) / (2 * side1 * side3));
                double c = Math.Acos((side1 * side1 + side2 * side2 - side3 * side3) / (2 * side1 * side2));
                List<double> list = new List<double> { a, b, c };
                return list;
            }
            public void SetSides(double a, double b, double c)
            {
                side1 = a;
                side2 = b;
                side3 = c;
            }
        }

        public class RegularTriangle : Triangle
        {
            public RegularTriangle(double a) : base(a, a, a)
            {
            }
            private double Area;
            public double GetArea()
            {
                double A = Math.Sqrt(3) * 0.25 * side1 * side1;
                this.Area = A;
                return A;
            }
        }

        static void Main()
        {
            Application.EnableVisualStyles();
            Application.SetCompatibleTextRenderingDefault(false);
            Application.Run(new Form1());
        }
    }
}
