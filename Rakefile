require 'yaml'

task :build do
  File.open('plugin/korean-typo-highlighter.vim', 'w') do  |f|
    f.puts 'function! KoreanTypoHighlight()'
    words = YAML.load_file('words.yml')
    wrongs = words.flat_map { |_, ws| ws }.sort.uniq
    f.puts "syn match Error '#{wrongs.join('\|')}'"
    f.puts 'endfunction'
  end
end

task default: :build
