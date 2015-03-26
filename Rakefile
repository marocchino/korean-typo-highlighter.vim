require 'yaml'

task :build do
  File.open("plugin/korean-typo-highlighter.vim", "w") do  |f|
    f.puts "function! KoreanTypoHighlight()"
    words = YAML.load_file('words.yml')
    wrongs = words.flat_map { |_, ws| ws }.sort.uniq
    wrongs.each do |wrong|
      f.puts "syn match Error '#{wrong}'"
    end
    f.puts "endfunction"
  end
end
