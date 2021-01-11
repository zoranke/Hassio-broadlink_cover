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
