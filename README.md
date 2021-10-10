# Web-Scraper - Transgender issues in The New York Times

## Description 

Visibility is key to understanding, acceptance, and ultimately, hopefully, equality.  I wanted to measure how transgender representation has evolved over the decades. So, I scraped The New York Times' archives, seeing them as a valid barometer for the cutural milieu.
  



## Table of Contents
* [Tools](#Tools)
* [Methodology](#methodology)
* [Results](#results)
  

## Tools

Web-Scraper: Jupyter Notebook, BeautifulSoup, Splinter
Database:Pandas
Graphs: Matplotlib

## Usage 

(images/readme-demo.png)

When you run `node index.js`, the application uses the `inquirer` package to prompt you in the command line with a series of questions about your GitHub and about your project.

The application then takes your responses and uses `axios` to fetch your GitHub profile from the [GitHub API](https://developer.github.com/v3/), including your GitHub profile picture (avatar) and email.
From there, the application will generate markdown and a table of contents for the README conditionally based on your responses to the Inquirer prompts (so, if you don't answer the optional questions, such as Installation, an Installation section will not be included in your README). The README will also include badges for your GitHub repo.

Finally, `fs.writeFile` is used to generate your project's README.md file. Check out the [`ExampleREADME.md`](https://github.com/connietran-dev/readme-generator/blob/master/ExampleREADME.md) in this repo as an example on the final output. 

The lorem ipsum is generated thanks to [Social Good Ipsum](http://socialgoodipsum.com/#/).


## Methodology

![Gif demo of README-generator](/images/j_notebook)

The application utilizes modularization by separating the GitHub API call and generation of the markdown into separate modules: `api.js` and `generateMarkdown.js`, respectively, inside the `utils` folder.

The application also utilizes, as much as possible, syntax and paradigms introduced in ES6 and beyond, including:

- Arrow functions, 
- `const`, `let`, 
- Template literals, and
- `async/await` to handle `inquirer`, `axios`, and `fs.writeFile` promises.


## License

MIT License

---

## Questions?

<img src="https://avatars3.githubusercontent.com/u/61371242?v=4" alt="Connie Tran, Full-Stack Web Developer" width="40%" />


If you utilize this app to generate a README for your project, I'd love to see. Feel free to contact me with examples or any questions via the information below:

GitHub: [@connietran-dev](https://api.github.com/users/connietran-dev)

Email: connietrandev@gmail.com
