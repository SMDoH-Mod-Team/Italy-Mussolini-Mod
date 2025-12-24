	focus = {
		id = ITA_enter_the_high_stage_of_imperialism
		icon = GFX_focus_generic_motor_cycle
		relative_position_id = ITA_national_economy_fascismful
		x = 0
		y = 10
		#prerequisite = {
		#	focus = ITA_national_economy_fascismful
		#}
		available = {
			always = no
		}
		allow_branch = { is_ai = yes }
		cost = 8.6
		completion_reward = {
			#custom_effect_tooltip = ITA_enter_the_high_stage_of_imperialism_tt_1
			every_core_state = {
				limit = {
					is_fully_controlled_by = ROOT
					free_building_slots = {
						building = industrial_complex
						size > 0
						include_locked = yes
					}
				}
				random_select_amount = 2
				add_extra_state_shared_building_slots = 1
				add_building_construction = {
					type = industrial_complex
					level = 1
					instant_build = yes
				}
			}
			custom_effect_tooltip = generic_skip_one_line_tt
			#add_ideas = idea_ITA_state_monopoly_capitalism
			#add_political_power = -15
			custom_effect_tooltip = ITA_enter_the_high_stage_of_imperialism_tt
			ITA_state_monopoly_capitalism_reforming = yes
			custom_effect_tooltip = generic_skip_one_line_tt
			custom_effect_tooltip = ITA_national_economy_fascismful_tt
			show_ideas_tooltip = ITA_autarkic_economy
		}
	}