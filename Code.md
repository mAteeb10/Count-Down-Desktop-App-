import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class CountdownGUI extends JFrame {
    private JLabel countdownLabel;

    public CountdownGUI() {
        setTitle("Countdown Timer");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 200);
        setLocationRelativeTo(null);

        countdownLabel = new JLabel("Countdown:");
        countdownLabel.setFont(new Font("Arial", Font.BOLD, 24));
        countdownLabel.setHorizontalAlignment(SwingConstants.CENTER);

        add(countdownLabel);

        setVisible(true);

        startCountdown();
    }

    private void startCountdown() {
        Thread countdownThread = new Thread(() -> {
            for (int i = 10; i >= 0; i--) {
                final int count = i;
                SwingUtilities.invokeLater(() -> countdownLabel.setText("Countdown: " + count));

                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        countdownThread.start();
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(CountdownGUI::new);
    }
}
