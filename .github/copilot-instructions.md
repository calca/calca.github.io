# Calca's Personal Website
Personal Jekyll website using the Minimal Mistakes theme, hosted on GitHub Pages.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively
- Bootstrap and build the repository:
  - Install Ruby (3.2.3+ works): `ruby --version`
  - Install Bundler: `gem install bundler --user-install`
  - Add Bundler to PATH: `export PATH="$HOME/.local/share/gem/ruby/3.2.0/bin:$PATH"`
  - Configure local bundle installation: `bundle config set --local path 'vendor/bundle'`
  - Install dependencies: `bundle install` -- takes 22 seconds. NEVER CANCEL. Set timeout to 60+ seconds.
- Build the Jekyll site:
  - `bundle exec jekyll build` -- takes 3 seconds. NEVER CANCEL. Set timeout to 30+ seconds.
- Run the development server:
  - `bundle exec jekyll serve --host=0.0.0.0` -- starts in 3 seconds, serves on http://localhost:4000
- Validate configuration:
  - `bundle exec jekyll doctor` -- checks for Jekyll configuration issues

## Validation
- Always manually validate changes by building and serving the site locally.
- Test site accessibility: `curl -s -o /dev/null -w "%{http_code}" http://localhost:4000/` should return 200.
- ALWAYS run through at least one complete end-to-end scenario after making changes:
  - Build the site and ensure no errors
  - Start the development server 
  - Navigate to http://localhost:4000 in a browser
  - Verify homepage loads with correct title "Welcome to My Personal Website"
  - Check navigation links work (Home, GitHub, Buy Me a Coffee, Instagram)
  - Verify site footer and author profile display correctly
- Run `bundle exec jekyll doctor` before committing changes to catch configuration issues.

## Common Tasks
The following are outputs from frequently run commands. Reference them instead of viewing, searching, or running bash commands to save time.

### Repository Structure
```
/home/runner/work/calca.github.io/calca.github.io/
├── _config.yml          # Jekyll configuration
├── _data/
│   └── navigation.yml   # Site navigation links
├── Gemfile              # Ruby dependencies
├── index.md             # Homepage content
├── README.md            # Repository documentation
├── .gitignore           # Git ignore patterns
└── vendor/bundle/       # Local gem installation (after setup)
```

### Key Files Content

#### _config.yml highlights:
- Title: "Calca's Personal Website"
- Theme: mmistakes/minimal-mistakes (remote theme)
- URL: https://calca.github.io
- Author: Calca with GitHub, Buy Me a Coffee, Instagram links

#### Gemfile dependencies:
- github-pages gem (includes Jekyll and GitHub Pages compatible gems)
- jekyll-include-cache for performance

#### Navigation (_data/navigation.yml):
- Home, GitHub, Buy Me a Coffee, Instagram links

### Common Command Results

#### bundle install (successful):
```
Bundle complete! 6 Gemfile dependencies, 98 gems now installed.
Bundled gems are installed into `./vendor/bundle`
```

#### bundle exec jekyll build (successful):
```
Configuration file: /path/_config.yml
Remote Theme: Using theme mmistakes/minimal-mistakes
Jekyll Feed: Generating feed for posts
done in 2.917 seconds.
```

#### bundle exec jekyll serve (successful):
```
Server address: http://0.0.0.0:4000/
Server running... press ctrl-c to stop.
```

#### bundle exec jekyll doctor (successful):
```
Your test results are in. Everything looks fine.
```

## Technology Stack
- **Jekyll 3.10.0** - Static site generator
- **Minimal Mistakes Theme** - Remote theme from mmistakes/minimal-mistakes
- **GitHub Pages** - Hosting platform (automatic deployment)
- **Ruby 3.2.3+** - Runtime environment
- **Bundler** - Dependency management

## Troubleshooting
- **Permission errors during gem install**: Use `gem install bundler --user-install` and update PATH
- **Bundle install fails**: Run `bundle config set --local path 'vendor/bundle'` first
- **Site not loading**: Check Jekyll server is running on correct host with `--host=0.0.0.0`
- **Build errors**: Run `bundle exec jekyll doctor` to identify configuration issues
- **Theme not loading**: Verify internet connection for remote theme download

## File Locations
- Site configuration: `_config.yml`
- Homepage content: `index.md`
- Navigation menu: `_data/navigation.yml`
- Generated site files: `_site/` (created after build)
- Local gems: `vendor/bundle/` (created after bundle config)
- Dependency lock: `Gemfile.lock` (auto-generated)

## GitHub Pages Deployment
- Automatic deployment on push to main branch
- No build scripts or workflows required - GitHub Pages handles Jekyll build
- Live site: https://calca.github.io
- Uses GitHub Pages compatible gems only (defined by github-pages gem)

## Development Notes
- This is a simple personal website with minimal customization
- Content is primarily in index.md with basic Markdown
- No custom plugins or complex build processes
- Follows standard Jekyll/GitHub Pages conventions
- No test suite or linting tools configured
- Clean, responsive design works on all device sizes