# Image-Converter-DLL

C# Code:
using image0x1;

namespace xxx
{
    public partial class main : Form
    {
        public main()
        {
            InitializeComponent();
        }

        images0 save = new images0();
        OpenFileDialog o = new OpenFileDialog();
        SaveFileDialog s = new SaveFileDialog();
        Image img;

        private void button1_Click(object sender, EventArgs e)
        {
            o.ShowDialog();
            img = Image.FromFile(o.FileName);
        }

        private void button2_Click(object sender, EventArgs e)
        {
            s.Filter = "JPG |*.jpg";
            s.ShowDialog();
            save.SaveToJpg(img, s.FileName);
        }
    }
}
