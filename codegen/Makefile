
TARGET= ../mrubybind.h

all: $(TARGET)

clean:
	rm -rf $(TARGET)

../mrubybind.h:	mrubybind.1.h mrubybind.3.h mrubybind_types.1.h mrubybind_types.3.h gen_template.rb
	(echo "// Do not modify this file directly, this is generated" && \
	 cat mrubybind.1.h mrubybind_types.1.h && \
	 ruby gen_template.rb && \
	 cat mrubybind_types.3.h mrubybind.3.h) > $@

#
