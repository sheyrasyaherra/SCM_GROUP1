# SCM_GROUP1
This is Software Configuration Management Group 1 (Repository).

//This is change made by Khairul

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

public partial class AhgodaBookingService : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {

    }
    protected integer DropDownList1_SelectedIndexChanged(object sender, EventArgs e)
    {

    }
    protected void CalendarCheckIN_SelectionChanged(object sender, EventArgs e)
    {
        TBcheckin.Text = CalendarCheckIN.SelectedDate.ToString("dd/MM/yyyy");
    }
    protected void CalendarCheckOut_SelectionChanged(object sender, EventArgs e)
    {
        TBcheckout.Text = CalendarCheckOut.SelectedDate.ToString("dd/MM/yyyy");
    }
    protected void BTNsubmit_Click(object sender, EventArgs e)
    {
        float discount;
        float price;
        float afterdiscount;
        int day;
        int number1;


        LBnotice.Text = "Thankyou for your booking, here is your details booking information";
        LBtype.Text = "Type Of Customer :";
        LBhotel.Text = "Hotel :";
        LBcheckin.Text = "Check-in Date : ";
        LBcheckout.Text = "Check-out Date : ";
        LBday.Text = "Number of day/night : ";
        LBadults.Text = "Number of Adults : ";
        LBchildren.Text = "Number of Children : ";
        LBroom.Text = "Number of Room : ";
        LBbeforediscount.Text = "Rate Before Discount (RM) : ";

        LBtype0.Text = DDLtypeofcustomer.SelectedValue.ToString();
        LBhotel0.Text = DDLhotel.SelectedValue.ToString();
        LBcheckin0.Text = TBcheckin.Text;
        LBcheckout0.Text = TBcheckout.Text;
        LBday0.Text = TBday.Text;
        LBadults0.Text = TBadult.Text;
        
        
        ok
        LBchildren0.Text = TBchildren.Text;
        LBroom0.Text = TBroom.Text;


        number = int.Parse(TBadult.Text);
        if (number <= 2)
        {
            TBroom.Text = "1";
        }
        if (number > 2)
        {
            TBroom.Text = "2";
        }


        if (DDLtypeofcustomer.SelectedValue == "New Customer")
        {
            LBbeforediscount0.Text = " No Discount ";
            LBafterdiscount.Text = " Rate (RM) : ";
            if (DDLhotel.SelectedValue == "Ramama Malacca")
            {
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBafterdiscount0.Text = Convert.ToString(price);
            }

            if (DDLhotel.SelectedValue == "Rio Malacca")
            {
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBafterdiscount0.Text = Convert.ToString(price);
            }

            if (DDLhotel.SelectedValue == "Hill KL")
            {
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBafterdiscount0.Text = Convert.ToString(price);
            }
            if (DDLhotel.SelectedValue == "Nullman KL")
            {
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBafterdiscount0.Text = Convert.ToString(price);
            }
        }




        else 
        {
            LBafterdiscount.Text = "Rate After Discount (RM) : ";
            
            if (DDLhotel.SelectedValue == "Ramama Malacca")
            {
            
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBbeforediscount0.Text = Convert.ToString(price);
                discount = price * 25/100;
                afterdiscount = price - discount;
                LBafterdiscount0.Text = Convert.ToString(afterdiscount);

            }

            if (DDLhotel.SelectedValue == "Rio Malacca")
            {
                day = int.Parse(TBday.Text);
                price = day * 250;
                LBbeforediscount0.Text = Convert.ToString(price);
                discount = price * 30 / 100;
                afterdiscount = price - discount;
                LBafterdiscount0.Text = Convert.ToString(afterdiscount);
            }

            if (DDLhotel.SelectedValue == "Hill KL")
            {
                day = int.Parse(TBday.Text);
                price = day * 250;
                LBbeforediscount0.Text = Convert.ToString(price);
                discount = price * 30 / 100;
                afterdiscount = price - discount;
                LBafterdiscount0.Text = Convert.ToString(afterdiscount);
            }
            if (DDLhotel.SelectedValue == "Nullman KL")
            {
                day = int.Parse(TBday.Text);
                price = day * 150;
                LBbeforediscount0.Text = Convert.ToString(price);
                discount = price * 25 / 100;
                afterdiscount = price - discount;
                LBafterdiscount0.Text = Convert.ToString(afterdiscount);
            }
        }
        



    }
    protected void BTNclear_Click(object sender, EventArgs e)
    {
        LBnotice.Text = "";
        LBtype.Text = "";
        LBhotel.Text = "";
        LBcheckin.Text = "";
        LBcheckout.Text = "";
        LBday.Text = "";
        LBadults.Text = "";
        LBchildren.Text = "";
        LBroom.Text = "";
        LBbeforediscount.Text = "";
        LBafterdiscount.Text = "";

       
        LBtype0.Text = "";
        LBhotel0.Text = "";
        LBcheckin0.Text = "";
        LBcheckout0.Text = "";
        LBday0.Text = "";
        LBadults0.Text = "";
        LBchildren0.Text = "";
        LBroom0.Text = "";
        LBbeforediscount0.Text = "";
        LBafterdiscount0.Text = "";

        TBadult.Text = "";
        TBchildren.Text = "";
        TBday.Text = "";
        TBroom.Text = "";
        TBcheckin.Text = "";
        TBcheckout.Text = "";
    }
}

// we need to add a new function here.
// edited by nasrullah
