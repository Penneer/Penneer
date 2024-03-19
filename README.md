namespace WinFormsApp1
{
    partial class Form1
    {
        /// <summary>
        ///  Required designer variable.
        /// </summary>
        private System.ComponentModel.IContainer components = null;

        /// <summary>
        ///  Clean up any resources being used.
        /// </summary>
        /// <param name="disposing">true if managed resources should be disposed; otherwise, false.</param>
        protected override void Dispose(bool disposing)
        {
            if (disposing && (components != null))
            {
                components.Dispose();
            }
            base.Dispose(disposing);
        }

        #region Windows Form Designer generated code

        /// <summary>
        ///  Required method for Designer support - do not modify
        ///  the contents of this method with the code editor.
        /// </summary>
        private void InitializeComponent()
        {
            button1 = new Button();
            textBox1 = new TextBox();
            textBox2 = new TextBox();
            label1 = new Label();
            button2 = new Button();
            button3 = new Button();
            button4 = new Button();
            SuspendLayout();
            // 
            // button1
            // 
            button1.Location = new Point(489, 49);
            button1.Margin = new Padding(4);
            button1.Name = "button1";
            button1.Size = new Size(121, 45);
            button1.TabIndex = 0;
            button1.Text = "ADD";
            button1.UseVisualStyleBackColor = true;
            button1.FontChanged += button1_FontChanged;
            button1.Click += button1_Click;
            // 
            // textBox1
            // 
            textBox1.Location = new Point(47, 50);
            textBox1.Name = "textBox1";
            textBox1.Size = new Size(132, 29);
            textBox1.TabIndex = 1;
            // 
            // textBox2
            // 
            textBox2.Location = new Point(226, 50);
            textBox2.Name = "textBox2";
            textBox2.Size = new Size(143, 29);
            textBox2.TabIndex = 2;
            // 
            // label1
            // 
            label1.AutoSize = true;
            label1.Location = new Point(386, 53);
            label1.Name = "label1";
            label1.Size = new Size(48, 21);
            label1.TabIndex = 3;
            label1.Text = "Total";
            label1.Click += label1_Click;
            // 
            // button2
            // 
            button2.Location = new Point(489, 101);
            button2.Name = "button2";
            button2.Size = new Size(121, 39);
            button2.TabIndex = 4;
            button2.Text = "MINUS";
            button2.UseVisualStyleBackColor = true;
            button2.Click += button2_Click;
            // 
            // button3
            // 
            button3.Location = new Point(489, 159);
            button3.Name = "button3";
            button3.Size = new Size(121, 41);
            button3.TabIndex = 5;
            button3.Text = "MULTIPLY";
            button3.UseVisualStyleBackColor = true;
            button3.Click += button3_Click;
            // 
            // button4
            // 
            button4.Location = new Point(489, 216);
            button4.Name = "button4";
            button4.Size = new Size(121, 43);
            button4.TabIndex = 6;
            button4.Text = "DIVIDE";
            button4.UseVisualStyleBackColor = true;
            button4.Click += button4_Click;
            // 
            // Form1
            // 
            AutoScaleDimensions = new SizeF(10F, 21F);
            AutoScaleMode = AutoScaleMode.Font;
            ClientSize = new Size(1143, 630);
            Controls.Add(button4);
            Controls.Add(button3);
            Controls.Add(button2);
            Controls.Add(label1);
            Controls.Add(textBox2);
            Controls.Add(textBox1);
            Controls.Add(button1);
            Font = new Font("Times New Roman", 14.25F, FontStyle.Regular, GraphicsUnit.Point, 0);
            Margin = new Padding(4);
            Name = "Form1";
            Text = "Jen Calculator";
            Load += Form1_Load;
            ResumeLayout(false);
            PerformLayout();
        }

        #endregion

        private Button button1;
        private TextBox textBox1;
        private TextBox textBox2;
        private Label label1;
        private Button button2;
        private Button button3;
        private Button button4;
    }
}




namespace WinFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            int textbox1 = Convert.ToInt32(textBox1.Text);
            int textbox2 = Convert.ToInt32(textBox2.Text);
            string total = Convert.ToString(textbox1 + textbox2);
            label1.Text = total;

        }


        private void button3_Click(object sender, EventArgs e)
        {
            int textbox1 = Convert.ToInt32(textBox1.Text);
            int textbox2 = Convert.ToInt32(textBox2.Text);
            string total = Convert.ToString(textbox1 * textbox2);
            label1.Text = total;
        }

        private void button2_Click(object sender, EventArgs e)
        {
            int textbox1 = Convert.ToInt32(textBox1.Text);
            int textbox2 = Convert.ToInt32(textBox2.Text);
            string total = Convert.ToString(textbox1 - textbox2);
            label1.Text = total;
        }

        private void button4_Click(object sender, EventArgs e)
        {
            int textbox1 = Convert.ToInt32(textBox1.Text);
            int textbox2 = Convert.ToInt32(textBox2.Text);
            string total = Convert.ToString(textbox1 / textbox2);
            label1.Text = total;
        }
        private void button1_FontChanged(object sender, EventArgs e)
        {

        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {
            textBox1.Text = "0";
            textBox2.Text = "0";

            textBox1.BackColor = Color.Yellow;
            textBox2.BackColor = Color.Yellow;

            button1.BackColor = Color.Red;
            button2.BackColor = Color.Blue;
            button3.BackColor = Color.Aqua;
            button4.BackColor = Color.Green;

        }
    }
}
