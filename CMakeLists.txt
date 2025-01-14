if ((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_INVERTING_KEY_PRESS app PRIVATE src/behaviors/behavior_inverting-key-press.c)
endif()
