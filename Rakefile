require 'yaml'
task :build do
  File.open("plugin/autocorrect-ko.vim", "w") do  |f|
    f.puts "function! AutoCorrectKo()"
    words = YAML.load_file('words.yml')
    words.each do |right, wrongs|
      wrongs.each do |wrong|
        f.puts "ia #{wrong} #{right}"
      end
    end
    f.puts "endfunction"
  end
end
