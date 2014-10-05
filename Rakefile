require 'html/proofer'

task :default => [:test]

task :test do
        sh "bundle exec jekyll build"
        # href ignoring mailto links with query strings
        HTML::Proofer.new("./_site", href_ignore: [/^mailto:.*\?/]).run
end

