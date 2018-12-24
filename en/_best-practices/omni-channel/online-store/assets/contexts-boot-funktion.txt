$eventDispatcher->listen('IO.ctx.item', function (TemplateContainer $templateContainer, $templateData = [])
   {
       $templateContainer->setContext( MyThemeContext::class);
       return false;
   }, 0);
