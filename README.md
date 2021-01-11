#broadlink cover

Home Assistant Custom Component for Broadlink Cover platform.
已支持 HACS(添加源https://github.com/zoranke/Hassio-broadlink_cover)

installation notes:
place this file in the following folder and restart home assistant:


/config/custom_components/broadlink_cover

##################################################################################
#
#       初次使用时如报错，可以屏蔽掉下方代码，运行一次后恢复代码，可记录上次重启轨道运行记录    
#
##################################################################################
    async def async_added_to_hass(self):
        await super().async_added_to_hass()
        last_state = await self.async_get_last_state()
        
        if last_state:
           self._position = last_state.attributes['current_position']
        else:
           self._position = None

配置实例见sample_cover.yaml
