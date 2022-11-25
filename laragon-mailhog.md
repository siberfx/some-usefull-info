1. Download MailHog: https://github.com/mailhog/MailHog/releases/download/v1.0.0/MailHog_windows_amd64.exe
2. Rename it to MailHog.exe
3. Move it to `C:\laragon\usr\bin\MailHog.exe
4. Open Laragon's Procfile (Menu > Laragon > Procfile) and add these lines:
  ```
    MailHog: MailHog.exe autorun
    MailHog Admin: http://localhost:8025 autorun
  ```
5. Open F:\laragon\bin\php\php-7.1.14-Win32-VC14-x64\php.ini
  ```
    SMTP = localhost
    smtp_port = 1025
    sendmail_path="F:\laragon\usr\bin\MailHog.exe sendmail"
  ```
6. Laragon settings, turn OFF Mail Catcher
7. Restart Laragon
8. Run "F:\laragon\usr\bin\MailHog.exe" and keep this open for the emails to be captured.
9. Launch http://localhost:8025/ which will only work when 8 is running.
