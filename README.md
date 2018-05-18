# SystemInformation
系统信息
 @ModelAttribute
    public Receipt get(@RequestParam(required = false) String id){
        Receipt entity = null;
        if(StringUtils.isNotBlank(id)){
            entity = receiptService.get(id);
        }
        if(null==entity){
            entity = new Receipt();
        }
        return entity;
    }
