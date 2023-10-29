<h1>VoteHub - Secure Online Voting Platform</h1>
<p>VoteHub is an online voting platform designed to ensure secure and efficient voting processes. It leverages the power of Laravel as the back-end framework, offering robust algorithms for vote management. In addition, VoteHub provides multiple layers of secure voter authentication, including Facial Recognition, Speech Recognition, and Fingerprint Scanning. With VoteHub, you can trust in a reliable and trusted online voting solution for all your election needs.</p>

<h2>Admin Features</h2>
<ul>
    <li>Create Positions: Admins can create new positions by providing a position name.</li>
    <li>Delete Positions: Admins can delete created positions.</li>
    <li>Edit Positions: Admins can modify position details.</li>
    <li>Export Positions: Admins can copy, export to Excel or PDF, and print position lists.</li>
    <li>Authorize Candidates: Admins can activate or deactivate registered candidates.</li>
    <li>Delete Candidates: Admins can remove registered candidates.</li>
    <li>Change Phase: Admins can switch the election phase between registration (default), voting, or over.</li>
    <li>Change Phase Time Restriction: Admins can't change the election phase until one hour after the last change.</li>
    <li>Voting Results: Admins can view voting results during the voting or post-election phase.</li>
    <li>Profile Update: Admins can edit their profiles.</li>
</ul>

<h2>Candidate Features</h2>
<ul>
    <li>Registration: Candidates can sign up and await admin approval for dashboard access.</li>
    <li>Voting Results: Candidates can check voting results during voting or post-election phases.</li>
    <li>Profile Update: Candidates can edit their profiles.</li>
</ul>

<h2>Voter Features</h2>
<ul>
    <li>Registration: Voters can register themselves.</li>
    <li>Cast Vote: Voters can cast their votes for preferred candidates using biometric authentication.</li>
    <li>Voting Results: Voters can view voting results during the voting or post-election phases.</li>
    <li>Profile Update: Voters can edit their profiles.</li>
</ul>

## Composer Installation (Windows)

To set up your development environment for the Laravel-based VoteHub application on a Windows system, you'll need to install Composer. Composer is a dependency management tool for PHP that helps manage libraries and packages.

Follow these steps to install Composer:

1. **Download the Composer Installer:**

   - Open your web browser and visit the Composer download page: [Composer Download](https://getcomposer.org/download/).

2. **Download and Run the Composer-Setup.exe:**

   - On the Composer download page, locate the installer named "Composer-Setup.exe."
   - Click on the installer to download it to your computer.
   - After the download is complete, run the installer by double-clicking the "Composer-Setup.exe" file.

3. **Install Composer:**

   - The installation process is straightforward. Follow these steps:

     - **Step 1**: Click "Next" to begin the installation.
     - **Step 2**: Choose whether to install Composer globally (for all users) or only for the current user. It's recommended to choose "Just Me" (local) to avoid permission issues.
     - **Step 3**: Select the PHP executable used by your web server. If you're using XAMPP or WAMP, it's typically located in the "php" subdirectory of your installation. If you're unsure, you can check your PHP location by running `php -v` in your command prompt.
     - **Step 4**: Choose whether to check for Composer updates. It's a good idea to leave this option enabled to ensure you have the latest version.
     - **Step 5**: Click "Install" to start the installation.

4. **Finish the Installation:**

   - The Composer installer will download and install Composer and its dependencies. Once completed, you'll see a message indicating a successful installation.

5. **Verify the Installation:**

   - To verify that Composer has been installed correctly, open your command prompt and run the following command:

     ```sh
     composer --version
     ```

     - This command should display the installed version of Composer, indicating that the installation was successful.

With Composer successfully installed on your Windows machine, you can now proceed with the installation of the VoteHub Laravel application.

<h2>Installation</h2>
Now that you have Composer installed, you can proceed to set up the VoteHub Laravel application by following the steps below:

<ol>
    <li>Clone the repository to your local environment.</li>
    <li>Make sure you have PHP and Composer installed on your system.</li>
    <li>Run the following command to install the Laravel dependencies:</li>
    <pre><code>composer install</code></pre>
    <li>Copy the .env.example file to .env and configure your database settings.</li>
    <li>Replace <code>FACE_PLUS_PLUS_API_KEY</code> and <code>FACE_PLUS_PLUS_SECRET_KEY</code> to your own faceplusplus credential.</li>
    <li>Run the following command to generate a key for your application:</li>
    <pre><code>php artisan key:generate</code></pre>
    <li>Run the following command to migrate the database:</li>
    <pre><code>php artisan migrate</code></pre>
    <li>Run the following command to seed the database with sample data:</li>
    <pre><code>php artisan db:seed</code></pre>
    <li>Run the following command to create an admin account:</li>
<pre>
    <code>
    \App\Models\Admin::factory()->create([
        'name' => 'ADMIN_NAME',
        'email' => 'ADMIN_EMAIL',
        'password' => Hash::make('ADMIN_PASSWORD'),
    ]);
    </code>
</pre>
<li>Run the following command to start the Laravel development server:</li>
<pre><code>php artisan serve</code></pre>

<li>Open your web browser and access the application at <code>http://localhost:8000</code>.</li>

</ol>
