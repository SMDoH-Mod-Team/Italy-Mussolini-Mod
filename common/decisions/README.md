在文件前边添加 A(a) 前缀的作用是让此文件在整个游戏要读取的文件列表中排名靠上，从而可以实现类似于 replace 的效果(与MOD读取方式不同，整个文件列表完成后是越靠上的文件中的条目覆盖靠下的文件中的条目)

MODDED:
    from_fasces_subjet_decision = {
		icon = GFX_decision_generic_nationalism
		target_array = IPUnion_subject_fasces_countries

		cost = 35
		
		available = {
			any_country = {
				OR = {
					original_tag = ITA
					is_subject_of = ITA
				}
				controls_state = FROM.core_states
			}
		}

		allowed = {
			original_tag = ITA
		}

		complete_effect = {
			if = {
				limit = {
					country_exists = FROM
				}
				set_autonomy = {
					target = FROM
					autonomy_state = autonomy_satellite
				}
				if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_USA_flag
						}
					}
					FROM = {
						set_cosmetic_tag = USAPF
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_CUB_flag
						}
					}
					FROM = {
						set_cosmetic_tag = CUB_fasces
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_COL_flag
						}
					}
					FROM = {
						set_cosmetic_tag = COL_fasces
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_ECU_flag
						}
					}
					FROM = {
						set_cosmetic_tag = ECU_fasces
					}
				}
			}
			else_if = {
				limit = {
					NOT = {
						country_exists = FROM
					}
				}
				FROM = {
					transfer_state = FROM.core_states
				}
				set_autonomy = {
					target = USA
					autonomy_state = autonomy_satellite
				}
				if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_USA_flag
						}
					}
					FROM = {
						set_cosmetic_tag = USAPF
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_CUB_flag
						}
					}
					FROM = {
						set_cosmetic_tag = CUB_fasces
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_COL_flag
						}
					}
					FROM = {
						set_cosmetic_tag = COL_fasces
					}
				}
				else_if = {
					limit = {
						FROM = {
							has_country_flag = IPUnion_ECU_flag
						}
					}
					FROM = {
						set_cosmetic_tag = ECU_fasces
					}
				}
			}
		}
	}