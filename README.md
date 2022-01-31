# calculator1
//Supported Libraries imported 
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JButton;
import java.util.Stack;
import javax.swing.text.BadLocationException;
import javax.swing.text.DefaultHighlighter;
import javax.swing.text.Highlighter;
import javax.swing.text.Highlighter.HighlightPainter;
import javax.swing.text.JTextComponent;
import java.awt.Color;
//Class defination with parent class Jframe and implememtation of ActionListener for buttons
public class calculatorClass extends javax.swing.JFrame implements ActionListener {
    //Defination of Buttons 
    private javax.swing.JButton backspace;
    private javax.swing.JButton cal0;
    private javax.swing.JButton cal1;
    private javax.swing.JButton cal2;
    private javax.swing.JButton cal3;
    private javax.swing.JButton cal4;
    private javax.swing.JButton cal5;
    private javax.swing.JButton cal6;
    private javax.swing.JButton cal7;
    private javax.swing.JButton cal8;
    private javax.swing.JButton cal9;
    private javax.swing.JButton calDivide;
    private javax.swing.JButton calDot;
    private javax.swing.JButton calEqual;
    private javax.swing.JButton calFactorial;
    private javax.swing.JLabel calHeading;
    private javax.swing.JButton calMinus;
    private javax.swing.JButton calMultiply;
    private javax.swing.JButton calPlus;
    private javax.swing.JTextField calTextBox;
    private javax.swing.JButton clear;
    private javax.swing.JButton exit;
    private javax.swing.JButton extra;
    private javax.swing.JButton leftParenthesis;
    private javax.swing.JButton rightParenthesis;
    //DATA memebers
    private int index=0;
    //Constructor
    public calculatorClass() {
        //Draw UI
        initComponents();
        //Set Action Commnads
        cal1.setActionCommand("1");
        cal2.setActionCommand("2");
        cal3.setActionCommand("3");
        cal4.setActionCommand("4");
        cal5.setActionCommand("5");
        cal6.setActionCommand("6");
        cal7.setActionCommand("7");
        cal8.setActionCommand("8");
        cal9.setActionCommand("9");
        cal0.setActionCommand("0");
        calPlus.setActionCommand("+");
        calMinus.setActionCommand("-");
        calMultiply.setActionCommand("*");
        calDivide.setActionCommand("/");
        calFactorial.setActionCommand("!");
        backspace.setActionCommand("bk");
        clear.setActionCommand("clr");
        rightParenthesis.setActionCommand("rightP");
        leftParenthesis.setActionCommand("leftP");
        calEqual.setActionCommand("=");
        exit.setActionCommand("exit");
        //Set ActionListeners to buttons
        cal1.addActionListener(this);
        cal2.addActionListener(this);
        cal3.addActionListener(this);
        cal4.addActionListener(this);
        cal5.addActionListener(this);
        cal6.addActionListener(this);
        cal7.addActionListener(this);
        cal8.addActionListener(this);
        cal9.addActionListener(this);
        cal0.addActionListener(this);
        calPlus.addActionListener(this);
        calMinus.addActionListener(this);
        calMultiply.addActionListener(this);
        calDivide.addActionListener(this);
        calFactorial.addActionListener(this);
        backspace.addActionListener(this);
        clear.addActionListener(this);
        rightParenthesis.addActionListener(this);
        leftParenthesis.addActionListener(this);
        calEqual.addActionListener(this);
        exit.addActionListener(this);
    }
    //Main Method
    public static void main(String[] args) {
        // TODO code application logic here
        calculatorClass clas=new calculatorClass();
        clas.setVisible(true);
    }
    //Draw UI
    private void initComponents() {
        //Initoalize Buttons/ Controls
        calHeading = new javax.swing.JLabel();
        calTextBox = new javax.swing.JTextField();
        cal1 = new javax.swing.JButton();
        cal2 = new javax.swing.JButton();
        cal3 = new javax.swing.JButton();
        calPlus = new javax.swing.JButton();
        backspace = new javax.swing.JButton();
        cal4 = new javax.swing.JButton();
        cal5 = new javax.swing.JButton();
        cal6 = new javax.swing.JButton();
        calMinus = new javax.swing.JButton();
        clear = new javax.swing.JButton();
        cal8 = new javax.swing.JButton();
        cal7 = new javax.swing.JButton();
        rightParenthesis = new javax.swing.JButton();
        calMultiply = new javax.swing.JButton();
        cal9 = new javax.swing.JButton();
        cal0 = new javax.swing.JButton();
        extra = new javax.swing.JButton();
        leftParenthesis = new javax.swing.JButton();
        calDivide = new javax.swing.JButton();
        calDot = new javax.swing.JButton();
        calEqual = new javax.swing.JButton();
        calFactorial = new javax.swing.JButton();
        exit = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        calHeading.setText("MYPROG5001-CALCULATOR");

        cal1.setText("1");

        cal2.setText("2");

        cal3.setText("3");

        calPlus.setText("+");

        backspace.setText("<<");

        cal4.setText("4");

        cal5.setText("5");

        cal6.setText("6");

        calMinus.setText("_");

        clear.setText("C");

        cal8.setText("8");

        cal7.setText("7");

        rightParenthesis.setText(")");

        calMultiply.setText("*");

        cal9.setText("9");

        cal0.setText("0");

        extra.setText("+/-");

        leftParenthesis.setText("(");

        calDivide.setText("/");

        calDot.setText(".");

        calEqual.setText("=");

        calFactorial.setText("!");

        exit.setText("OFF");

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(calTextBox)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(cal7, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal8, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal9, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(calMultiply, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(18, 18, 18)
                        .addComponent(rightParenthesis, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(cal1, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal2, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal3, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(calPlus, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(18, 18, 18)
                        .addComponent(backspace, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(cal4, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal5, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(cal6, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(calMinus, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(18, 18, 18)
                        .addComponent(clear, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                    .addGroup(layout.createSequentialGroup()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING, false)
                            .addComponent(calEqual, javax.swing.GroupLayout.Alignment.LEADING, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addGroup(javax.swing.GroupLayout.Alignment.LEADING, layout.createSequentialGroup()
                                .addComponent(extra, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(cal0, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(calDot, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(calDivide, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(18, 18, 18)
                                .addComponent(leftParenthesis, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(calFactorial, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(18, 18, 18)
                                .addComponent(exit, javax.swing.GroupLayout.DEFAULT_SIZE, 77, Short.MAX_VALUE)))))
                .addGap(0, 41, Short.MAX_VALUE))
            .addComponent(calHeading, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addComponent(calHeading, javax.swing.GroupLayout.PREFERRED_SIZE, 36, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(1, 1, 1)
                .addComponent(calTextBox, javax.swing.GroupLayout.PREFERRED_SIZE, 34, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(cal1)
                    .addComponent(cal2)
                    .addComponent(cal3)
                    .addComponent(calPlus)
                    .addComponent(backspace, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(cal4)
                    .addComponent(cal5)
                    .addComponent(cal6)
                    .addComponent(calMinus)
                    .addComponent(clear, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(cal7)
                    .addComponent(cal8)
                    .addComponent(cal9)
                    .addComponent(calMultiply)
                    .addComponent(rightParenthesis, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(extra)
                    .addComponent(cal0)
                    .addComponent(calDot)
                    .addComponent(calDivide)
                    .addComponent(leftParenthesis, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(calEqual)
                    .addComponent(calFactorial)
                    .addComponent(exit, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addGap(0, 40, Short.MAX_VALUE))
        );

        pack();
    }
    //Perform Action on Buttons
    @Override
    public void actionPerformed(ActionEvent e) {
        JButton button = (JButton) e.getSource();
        String action = button.getActionCommand();
        switch (action) {
            case "1":
                calTextBox.setText(calTextBox.getText() + "1");
                break;
            case "2":
                calTextBox.setText(calTextBox.getText() + "2");
                break;
            case "3":
                calTextBox.setText(calTextBox.getText() + "3");
                break;
            case "4":
                calTextBox.setText(calTextBox.getText() + "4");
                break;
            case "5":
                calTextBox.setText(calTextBox.getText() + "5");
                break;
            case "6":
                calTextBox.setText(calTextBox.getText() + "6");
                break;
            case "7":
                calTextBox.setText(calTextBox.getText() + "7");
                break;
            case "8":
                calTextBox.setText(calTextBox.getText() + "8");
                break;
            case "9":
                calTextBox.setText(calTextBox.getText() + "9");
                break;
            case "0":
                calTextBox.setText(calTextBox.getText() + "0");
                break;
            case "+":
                calTextBox.setText(calTextBox.getText() + "+");
                break;
            case "-":
                calTextBox.setText(calTextBox.getText() + "-");
                break;
            case "*":
                calTextBox.setText(calTextBox.getText() + "*");
                break;
            case "/":
                calTextBox.setText(calTextBox.getText() + "/");
                break;
            case "!":
                calTextBox.setText(calTextBox.getText() + "!");
                break;
            case "bk":
                if (calTextBox.getText().length() > 0) {
                    calTextBox.setText(calTextBox.getText().substring(0, calTextBox.getText().length() - 1));
                }
                break;

            case "clr":
                calTextBox.setText("");
                break;

            case "rightP":
                calTextBox.setText(calTextBox.getText() + ")");
                break;

            case "leftP":
                calTextBox.setText(calTextBox.getText() + "(");
                break;
            case "=":
                int result = (evaluate(calTextBox.getText().trim()));
                if (result == -1) {
                    String data = calTextBox.getText().substring(this.index);
                    calTextBox.setText(calTextBox.getText().substring(0, this.index));
                    highlightErrors(calTextBox, data, true);
                } else {
                    calTextBox.setText(result + "");
                }
                break;
            case "exit":
                System.exit(0);

        }
    }
    //Highlight Errors in Expresions
    private int highlightErrors(JTextComponent area, String text, boolean highlight) {
        //int start= EvaluateString.index;
        int start = area.getDocument().getLength();

        if (text == null || text.length() == 0) {
            return start;
        }

        int end = start + text.length();

        try {

            area.getDocument().insertString(start, text, null);

            if (highlight) {
                Highlighter hilite = area.getHighlighter();
                HighlightPainter painter
                = new DefaultHighlighter.DefaultHighlightPainter(Color.RED);
                hilite.addHighlight(start, end - 1, painter);
            }

        } catch (BadLocationException e) {
            //  logger.error(e.getMessage(), e);
        }
        return end;
    }
    //Solve Expression
    public int evaluate(String expression) {
        char[] tokens = expression.toCharArray();

        // Stack for numbers: 'values'
        Stack<Integer> values = new Stack<Integer>();

        // Stack for Operators: 'ops'
        Stack<Character> ops = new Stack<Character>();
        try{
            for (int i = 0; i < tokens.length; i++) {
                this.index=i;
                if (tokens[i] == ' ') {
                    continue;
                }
                if (tokens[i] >= '0' && tokens[i] <= '9') {
                    StringBuilder sbuf = new StringBuilder();

                    while (i < tokens.length && tokens[i] >= '0' && tokens[i] <= '9') {
                        sbuf.append(tokens[i++]);
                    }
                    values.push(Integer.parseInt(sbuf.toString()));
                    i--;
                } else if (tokens[i] == '(') {
                    ops.push(tokens[i]);
                } else if (tokens[i] == ')') {
                    while (ops.peek() != '(') {
                        values.push(applyOp(ops.pop(), values.pop(), values.pop()));
                    }
                    ops.pop();
                } else if (tokens[i] == '+' || tokens[i] == '-' || tokens[i] == '*' || tokens[i] == '/') {
                    while (!ops.empty() && hasPrecedence(tokens[i], ops.peek())) {
                        values.push(applyOp(ops.pop(), values.pop(), values.pop()));
                    }

                    ops.push(tokens[i]);
                }else if(tokens[i]=='!'){
                    values.push(factorial(values.pop()));
                }
            }

            while (!ops.empty()) {
                values.push(applyOp(ops.pop(), values.pop(), values.pop()));
            }

        }catch(Exception e){
            return -1;
        }

        return values.pop();
    }
    //Check Precedence
    public boolean hasPrecedence(char op1, char op2) {
        if (op2 == '(' || op2 == ')') {
            return false;
        }
        if ((op1 == '*' || op1 == '/')
        && (op2 == '+' || op2 == '-')) {
            return false;
        } else {
            return true;
        }
    }
    //Apply Operations
    public int applyOp(char op,int b, int a) {
        switch (op) {
            case '+':
                return a + b;
            case '-':
                return a - b;
            case '*':
                return a * b;
            case '/':
                if (b == 0) {
                    throw new UnsupportedOperationException(
                        "Cannot divide by zero");
                }
                return a / b;
        }
        return 0;
    }
    //Calculate Factorial
    public int factorial(int num){
        int fact=1;
        for(int i=1;i<=num;i++){    
            fact=fact*i;    
        } 
        return fact;
    }

}
