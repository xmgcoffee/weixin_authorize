module WeixinAuthorize
  module Api
    module Tags
        
        #创建标签
        #https://api.weixin.qq.com/cgi-bin/tags/create?access_token=ACCESS_TOKEN
        def create_tag(tag_name)
          create_url = "#{tag_base_url}/create"
          http_post(create_url, {tag: {name: tag_name}})
        end
        
        #获取公众号已创建的标签
        #https://api.weixin.qq.com/cgi-bin/tags/get?access_token=ACCESS_TOKEN
        def tags
          tags_url = "#{tag_base_url}/get"
          http_get(tags_url)
        end
        
        #编辑标签
        #https://api.weixin.qq.com/cgi-bin/tags/update?access_token=ACCESS_TOKEN
        def update_tag_name(tag_id, new_tag_name)
          tag_url = "#{tag_base_url}/update"
          http_post(tag_url, {tag: {id: tag_id, name: new_tag_name}})
        end
        
        #删除标签
        #https://api.weixin.qq.com/cgi-bin/tags/delete?access_token=ACCESS_TOKEN
        def delete_tag(tag_id)
          tag_url = "#{tag_base_url}/delete"
          http_post(tag_url, {tag: {id: tag_id}})
        end
        
        #批量为用户打标签
        #https://api.weixin.qq.com/cgi-bin/tags/members/batchtagging?access_token=ACCESS_TOKEN
        def batchtagging(tagid,openid_list)
          tag_url = "#{tag_base_url}//members/batchtagging"
          http_post(tag_url, {tagid: tagid,openid_list:openid_list})
        end
        
        #批量为用户取消标签
        #https://api.weixin.qq.com/cgi-bin/tags/members/batchuntagging?access_token=ACCESS_TOKEN
        def batchuntagging(tagid,openid_list)
          tag_url = "#{tag_base_url}//members/batchuntagging"
          http_post(tag_url, {tagid: tagid,openid_list:openid_list})
        end
        
        
        
        private
        def tag_base_url
          "/tags"
        end

    end
  end
end
