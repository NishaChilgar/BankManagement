# BankManagement
#This is my First Repository


package bank.management.system;
<br>
import javax.swing.*;<br>
import java.awt.*;
<br>
import java.awt.event.*;
 
public class Login extends JFrame implements ActionListener{
    
    
    JButton Login,signup,clear;
    JTextField  cardTextField, pinTextField;
    JLabel text,cardno,pin;
    Login(){
         
         setTitle("Automated Tailer Machine");
         setLayout(null);
         ImageIcon i1 = new ImageIcon(ClassLoader.getSystemResource("icons/logo.jpg"));
         Image i2 = i1.getImage().getScaledInstance(100,100, Image.SCALE_DEFAULT);
         ImageIcon i3=new ImageIcon(i2);
         JLabel label=new JLabel(i3);
         label.setBounds(70,10,100,100);
         add(label); 
         
         text=new JLabel("Welcome to ATM");
         text.setFont(new Font("Onward",Font.BOLD,38));
         text.setBounds(200,40,400,40);
         add(text);
         
         cardno=new JLabel("Card No.");
         cardno.setFont(new Font("Railway",Font.BOLD,25));
         cardno.setBounds(120,150,150,40);
         add(cardno);
         
        cardTextField=new JTextField();
        cardTextField.setBounds(300,150,250,30);
        cardTextField.setFont(new Font("Arial", Font.BOLD,14));
        add(cardTextField);
         
        pin=new JLabel("PIN:");
        pin.setFont(new Font("Railway",Font.BOLD,25));
        pin.setBounds(120,200,400,40);
        add(pin);
         
        pinTextField=new JPasswordField();
        pinTextField.setBounds(300,200,250,30);
        pinTextField.setFont(new Font("Arial", Font.BOLD,14));
        add(pinTextField);
         
         Login=new JButton("Sign In");
         Login.setBounds(300,300,100,30);
         Login.setBackground(Color.BLACK);
         Login.setForeground(Color.WHITE);
         Login.addActionListener(this);
         add(Login);
         
         clear=new JButton("Clear");
         clear.setBounds(410,300,100,30);
         clear.setBackground(Color.BLACK);
         clear.setForeground(Color.WHITE);
         clear.addActionListener(this);
         add(clear);
                 
         signup=new JButton("Sign Up");
         signup.setBounds(520,300,100,30);
         signup.setBackground(Color.BLACK);
         signup.setForeground(Color.WHITE);
         signup.addActionListener(this);
         add(signup);         
         
         getContentPane().setBackground(Color.WHITE);
           
         setSize(800,480);
         setVisible(true);
         setLocation(350,200);
    }
    public void actionPerformed(ActionEvent ae){
        if(ae.getSource() == clear){ 
            cardTextField.setText("");
            pinTextField.setText("");
    }else if(ae.getSource()== Login){      
    }else if(ae.getSource()== signup){    
    }
    }
    public static void main(String args[]){
      new Login();  
    }
}
