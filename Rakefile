task :emoji do  
  ENV['SET'] ||= 'iphone'

  if !ENV['DEST']
    raise ArgumentError, "DEST=/path/to/destination"
  end

  icons = ENV['ICONS'].to_s.split(',').each { |s| s.strip! }
  icons = nil if icons.empty?

  require File.expand_path(File.join(File.dirname(__FILE__), 'lib/emoji_css_builder'))
  EmojiCSSBuilder.build(ENV['SET'].to_sym, ENV['DEST'], icons)

  name = "emoji-#{ENV['SET']}"
  %w(gif css html).each do |ext|
    puts "Wrote #{ENV['DEST']}/#{name}.#{ext}"
  end
end