<?php
namespace ThemeName\Contexts;

use IO\Helper\ContextInterface;
use Ceres\Contexts\SingleItemContext;

use IO\Services\ItemSearch\Services\ItemSearchService;
use IO\Services\ItemSearch\SearchPresets\CrossSellingItems;

class MyThemeContext extends SingleItemContext implements ContextInterface
{
	public $accessory;
  public $similar;

	public function init($params)
	{
		parent::init($params);
		$options = array(
        			"itemId" => $this->item['documents'][0]['data']['item']['id'],
        			"relation" => "Accessory"      // Use the list accessory
       		);
     		$searchfactory = CrossSellingItems::getSearchFactory( $options );
     		$searchfactory->setPage(1, 4); // Limit to 4 items
      		$result = pluginApp(ItemSearchService::class)->getResult($searchfactory);
      		$this->accessory = $result['documents'];

    $options = array(
              "itemId" => $this->item['documents'][0]['data']['item']['id'],
              "relation" => "Similar"      // Use the list similar
          );
        $searchfactory = CrossSellingItems::getSearchFactory( $options );
      	$searchfactory->setPage(1, 4); // Limit to 4 items
        	$result = pluginApp(ItemSearchService::class)->getResult($searchfactory);
        	$this->similar= $result['documents'];
	}
}
