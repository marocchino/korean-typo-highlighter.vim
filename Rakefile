require 'yaml'
WITH_FINAL =    "{은,이,을,과,아,이여,}"
WITHOUT_FINAL = "{는,가,를,와,야,여,}"

task :build do
  File.open("plugin/autocorrect-ko.vim", "w") do  |f|
    f.puts "function! AutoCorrectKo()"
    words = YAML.load_file('words.yml')
    words.each do |right, wrongs|
      wrongs.each do |wrong|
        f.puts "syn match Error '#{wrong}'"
      end
    end
    words.each do |right, wrongs|
      f.puts "Abolish #{right}#{has_final?(right) ? WITHOUT_FINAL : WITH_FINAL} #{right}#{has_final?(right) ? WITH_FINAL : WITHOUT_FINAL}"
      wrongs.each do |wrong|
        f.puts "Abolish #{wrong}#{WITHOUT_FINAL} #{right}#{has_final?(right) ? WITH_FINAL : WITHOUT_FINAL}"
        f.puts "Abolish #{wrong}#{WITH_FINAL} #{right}#{has_final?(right) ? WITH_FINAL : WITHOUT_FINAL}"
      end
    end
    f.puts "endfunction"
  end
end


def has_final?(str)
  !((str[str.size - 1].unpack("U").last - 44032) % 28).zero?
end
