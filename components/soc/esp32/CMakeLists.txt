set(srcs
    "adc_periph.c"
    "dac_periph.c"
    "gpio_periph.c"
    "i2c_periph.c"
    "i2s_periph.c"
    "interrupts.c"
    "ledc_periph.c"
    "mcpwm_periph.c"
    "pcnt_periph.c"
    "rmt_periph.c"
    "rtc_io_periph.c"
    "sdio_slave_periph.c"
    "sdmmc_periph.c"
    "sigmadelta_periph.c"
    "spi_periph.c"
    "timer_periph.c"
    "touch_sensor_periph.c"
    "uart_periph.c")

add_prefix(srcs "${CMAKE_CURRENT_LIST_DIR}/" "${srcs}")

target_sources(${COMPONENT_LIB} PRIVATE "${srcs}")
target_include_directories(${COMPONENT_LIB} PUBLIC . include)
