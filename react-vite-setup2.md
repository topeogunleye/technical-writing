Boost your React projects by combining Vite’s fast development server, ESLint’s strong linting features, and Prettier’s consistent formatting. With these tools, your VSCode becomes a productivity powerhouse.

As you read this article, you’ll learn how to set up Prettier and ESLint to automatically format your files when you save them, maintaining a polished codebase.

**Prerequisites**

- Ensure Node.js and npm (Node Package Manager) are installed on your computer.
- If they’re not already set up, visit the Node.js official website to download and install them.

## **Step 1: Initializing the Project with Vite**

To kick off our project, follow these steps:

1. **Create a new project directory and initialize it:**

`mkdir vs
cd rvs
npm init -y`

2. **Install Vite with the React template:**

Use the following command to set up Vite, which also includes the ESLint configuration:

```.bash
npx create-vite@latest my-react-app --template react
cd my-react-app
```

## **Step 2: Installing the ESLint Plugin for VSCode:**

Enhance your coding experience by integrating ESLint into VSCode. Follow these steps:

1. **Open VSCode Extensions:**

Access the Extensions view by clicking the VSCode sidebar’s square icon or pressing `Ctrl+Shift+X`.

2. **Search for ESLint:**

Type `ESLint` into the search bar.

3. **Install the Plugin:**

Find the ESLint plugin by Microsoft and click ‘Install’. This will help you maintain code quality and adhere to best practices directly within your editor.

By adding the ESLint plugin to VSCode, you can automatically lint and format your code as you write, ensuring consistency and readability.


## **Step 3: Setting Up Prettier**

1. **Install Prettier:**

Run `npm install --save-dev prettier` to add Prettier to your project.

2. **Create and Configure `.prettierrc.json`:**

Use `touch prettierrc.json` to create the configuration file, then define your formatting preferences within. For example, to use single quotes, your `.prettierrc.json` would look like this:
`{
 "singleQuote": true
}`
This file will instruct Prettier to format your code with single quotes instead of double quotes.


## Step 4: Sync Prettier & ESLint

To make Prettier and ESLint work together without issues.

1. **Install eslint-config-prettier:**

Run `npm install--save-dev eslint-config-prettier` to install the necessary package.

2. **Update `.eslintrc.cjs`:**

Add prettier to the end of the extends array in your `.eslintrc.cjs` file like so:

```.json
extends: [
 'eslint:recommended',
 'plugin:@typescript-eslint/recommended',
 'plugin:react-hooks/recommended',
 'prettier'
]
```

This ensures that Prettier’s formatting doesn’t conflict with ESLint rules.

3. **Check for Conflicts:**

Execute `npx eslint-config-config-prettier ./src/main.jsx`. If there are no messages, Prettier and ESLint are in sync. If there are messages, it indicates potential rule conflicts that have been successfully overridden.

## **Step 5: Integrating Prettier for Code Formatting**

To ensure consistent code style across your project, integrate Prettier by adding a format script to your package.json:

```.json
"scripts": {
  "dev": "vite",
  "build": "tsc && vite build",
  "lint": "eslint . --ext ts,tsx --report-unused-disable-directives --max-warnings 0",
  "preview": "vite preview",
  "format": "prettier --write \"src/**/*.{ts,tsx,js,jsx,json,css}\""
}
```
**Usage:**
Execute the command `npm run format` to automatically format all files in the `src` directory, including subdirectories. Prettier will apply formatting rules to TypeScript, JavaScript, JSON, and CSS files, ensuring a uniform coding style throughout your project.

## **Step 6: Installing the Prettier Plugin for VSCode**
To streamline your development workflow, install the Prettier extension for Visual Studio Code. This will allow you to automatically format your code as you write, ensuring consistent style without manual effort.

1. **Open VSCode Extensions:**

Launch Visual Studio Code and navigate to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window, or by pressing `Ctrl+Shift+X`.

2. **Search for Prettier:** 

In the Extensions view, type Prettier-Code Formaterin the search bar. Look for the official extension published by Prettier.

3. **Install Extension:**

Click on the Install button to add the Prettier extension to your Visual Studio Code.

4. **Executing Code Formatting with Prettier:**

To format your code using Prettier within Visual Studio Code, utilize the Command Palette for quickly accessing all available commands.

1. **Open Command Palette:** Press `Ctrl+Shift+P` to open the Command Palette. This shortcut brings up a search bar where you can run various commands.
2. **Run Format Document:** Type `Format Document` into the Command Palette’s search bar. Select the command when it appears in the dropdown menu. This action will apply Prettier formatting to your currently open file.
3. **Verify Formatting:** After executing the command, check your code to ensure that Prettier has formatted it according to your project’s style guide.

By incorporating this step, you can quickly format individual files using Prettier right from the Command Palette, streamlining your development process.

This step focuses on using Visual Studio Code’s Command Palette to execute Prettier formatting, providing a convenient method for developers to maintain code consistency.

5. **Optional Settings: Customizing Prettier Behavior in VSCode:**

To fine-tune how Prettier formats your code in Visual Studio Code, follow these steps:

1. **Set Prettier as Default Formatter:**

Go to `File > Preferences > Settings`(or `Code > Preferences > Settings on macOS`), search for `Default Formatter`, and select `Prettier-Code Formatter` from the dropdown menu.

2. **Enable Format On Save:**

Still, in Settings, find `Format On Save` and check the box to have Prettier format your files each time you save.

3. **Activate Format On Paste:**

Look for Format On Pastein the Settings and enable it to format content automatically when you paste it into your document.

**Conclusion**

Adopting Vite, ESLint, and Prettier in VSCode enhances our development with efficiency and quality. These tools help us maintain and scale projects, keeping us at the forefront of technology.

As developers, we must continually evolve with the ever-changing tech landscape, and leveraging tools like Vite, ESLint, and Prettier helps us stay ahead of the curve. Thanks for exploring these tools with me. Happy coding!