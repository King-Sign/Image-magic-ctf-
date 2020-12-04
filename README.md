# Image-magic-ctf-
#!/usr/bin/python import PIL from PIL import Image  o = Image.open('out copy.jpg') n = Image.new('RGB', (400, 400)) n_x = n_y = 0  for i in range(0, o.size[0]):     r, g, b = o.getpixel((i, 0))     n_x = (i % 92)          if i % 92 == 0:         n_y = n_y + 1      print "(%d, %d) ~> (%d, %d)"%(i, 0, n_x, n_y)          n.putpixel((n_x, n_y), (r, g, b))     n.save('test.jpg')
