### QR-code
---
.rb
https://github.com/whomwah/rqrcode

```
gem install rqrcode

```

```ruby
require 'rqrcode'
qrcode = RQRCode::QRCode.new("http://github.com")
image = qrcode.as_png
svg = qrcode.as_svg
html = qrcode.as_html
string = qrcode.as_ansi
string = qrcode.to_s


qrcode = RQRCode::QRCode.new("http://github.com/")
svg = qrcode.as_svg(offset: 0, color: '000',
                    shape_rendering: 'crispEdges',
                    module_size: 11)


qrcode = RQRCode::QRCode.new("http://github.com")
svg qrcode.as_ansi_(light: "\033[47m", dark: "\033[40m",
                  fill_character: ' ',
                  quiet_zone_size: 4)

qrcode = RQRCode.QRCode.new("http://github.com")
png = qrcode.as_png(
  resize_gte_to: false,
  resize_exactly_to: false,
  fill: 'white',
  color: 'black',
  size: 120,
  border_modules: 4,
  module_px_size: 6,
  file: nil
)
IO.write("/tmp/github-qrcode.png", png.to_s)

@qr = RQRCode::QRCode.new('https://github.com/whomwah/rqrcode', :size => 4, :level => :h)

qr = RQRCode::QRCode.new( 'my string to generate', :size => 4, :level => :h )
puts qr.to_s

qr = RQRCode::QRCode.new( 'my string to generate', :size => 4, :level => :h )
qr.modules.each do |row|
  row.each do |col|
    print col ? "X" : " "
  end
  print "\n"
end

qr = RQRCode::QRCode.new( '1234567890', :size => 2, :level => :m, :mode => :number )

```

```
<%= raw @qr.as_html %>

```

```css
table{
  border-width: 0;
  border-style: none;
  border-color: #0000ff;
  border-collapse: collapse;
}
td {
  border-left: solid 10px #000;
  padding: 0;
  margin: 0;
  width: 0px;
  height: 10px;
}
td.black { border-color: #000; }
td.white { border-color: #fff; }
```

