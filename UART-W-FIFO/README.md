62.5 MHz frekansında 9600 baudrate ile çalışan, 1-bit start biti, 8-bit veri, 1-bit stop biti ve 1-bit odd parity bitine sahip bir UART Receiver Interface tasarladım. Bu receiver, alınan UART mesajlarında start bit hatası, stop bit hatası veya parity hatası gibi hatalar tespit ettiğinde hatalı mesajları göz ardı ederek iletmez. Ayrıca, 50 MHz frekansında 115200 baudrate ile çalışan, 1-bit start biti, 8-bit veri, 1-bit stop biti ve 1-bit odd parity bitine sahip bir UART Transmitter Interface tasarladım. Bu tasarımlar arasında veri iletimi, FIFO (First In First Out) arabellek ile gerçekleştirilir. FIFO, receiver tarafından alınan veriyi yazdığı bir buffer işlevi görür ve FIFO'ya yazılan bu veri, transmitter aracılığıyla başka bir sisteme iletilir. FIFO, çift clock ile çalışacak şekilde tasarlanmıştır.
I designed a UART Receiver Interface that operates at a frequency of 62.5 MHz and a baud rate of 9600, with a 1-bit start bit, 8-bit data, 1-bit stop bit, and a 1-bit odd parity bit. This receiver ignores and does not transmit erroneous messages when it detects errors in the received UART message, such as start bit errors, stop bit errors, or parity errors. Additionally, I designed a UART Transmitter Interface that operates at a frequency of 50 MHz and a baud rate of 115200, with a 1-bit start bit, 8-bit data, 1-bit stop bit, and a 1-bit odd parity bit. Data transmission between these designs is handled by a FIFO (First In First Out) buffer. The FIFO functions as a buffer where the receiver writes the received data, and the data written to the FIFO is transmitted to another system via the transmitter. The FIFO is designed to operate with dual clocking.