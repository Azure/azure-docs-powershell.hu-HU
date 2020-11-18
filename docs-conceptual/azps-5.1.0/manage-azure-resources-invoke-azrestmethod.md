---
title: Azure-erőforrások kezelése az Invoke-AzRestMethod használatával
description: Erőforrások kezelése az Invoke-AzRestMethod parancsmaggal az Azure PowerShellben.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715481"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="da87c-103">Azure-erőforrások kezelése az Invoke-AzRestMethod használatával</span><span class="sxs-lookup"><span data-stu-id="da87c-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="da87c-104">Az [Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) egy olyan Azure PowerShell-parancsmag, amely az Az PowerShell-modul 4.4.0-s verziójában lett bevezetve.</span><span class="sxs-lookup"><span data-stu-id="da87c-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="da87c-105">Lehetővé teszi, hogy egyéni HTTP-kéréseket küldjön az Azure Resource Management (ARM) végpontjára az Az környezet használatával.</span><span class="sxs-lookup"><span data-stu-id="da87c-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="da87c-106">Ez a parancsmag akkor hasznos, ha az Azure-szolgáltatások olyan funkcióit szeretné felügyelni, amelyek még nem érhetők el az Az PowerShell-modulban.</span><span class="sxs-lookup"><span data-stu-id="da87c-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="da87c-107">Az Invoke-AzRestMethod használata</span><span class="sxs-lookup"><span data-stu-id="da87c-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="da87c-108">Például engedélyezheti az Azure Container Registry (ACR) szolgáltatáshoz való hozzáférést megadott hálózatok számára, vagy letilthatja a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="da87c-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="da87c-109">Az Az PowerShell-modul 4.5.0-s verziójában ez a funkció még nem érhető el az [Az.ContainerRegistry PowerShell-modulban](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="da87c-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="da87c-110">Azonban ideiglenesen az `Invoke-AzRestMethod` használatával is felügyelhető.</span><span class="sxs-lookup"><span data-stu-id="da87c-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="da87c-111">Az Invoke-AzRestMethod használata GET műveletekkel</span><span class="sxs-lookup"><span data-stu-id="da87c-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="da87c-112">Az alábbi példa azt mutatja be, hogyan használható az `Invoke-AzRestMethod` parancsmag egy GET művelettel:</span><span class="sxs-lookup"><span data-stu-id="da87c-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="da87c-113">A minél nagyobb rugalmasság érdekében az `Invoke-AzRestMethod` legtöbb paraméterének megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="da87c-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="da87c-114">Azonban ha egy erőforráscsoport erőforrásait szeretné kezelni, akkor valószínűleg meg kell adnia az erőforráshoz tartozó teljes azonosítót, illetve olyan paramétereket, mint például az erőforráscsoport, az erőforrás-szolgáltató és az erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="da87c-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="da87c-115">A `ResourceType` és a `Name` paraméterek több értéket is felvehetnek, ha a célként kijelölt erőforrások egynél több nevet igényelnek.</span><span class="sxs-lookup"><span data-stu-id="da87c-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="da87c-116">A Log Analytics-munkaterület mentett keresésének módosításához az alábbi példához hasonlóan kell megadni a paramétereket: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="da87c-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="da87c-117">A parancsmag egy tömbpozíción alapuló leképzés használatával a következő erőforrást hozza létre: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="da87c-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="da87c-118">Az `APIVersion` paraméter lehetővé teszi egy adott API-verzió használatát, beleértve az előzetes verziókat is.</span><span class="sxs-lookup"><span data-stu-id="da87c-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="da87c-119">Az Azure-beli erőforrás-szolgáltatók által elérhető, támogatott API-verziókat az [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub-adattár tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="da87c-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="da87c-120">Az ACR 2019. 12. 01-i előzetes verziójának definíciója a következő helyen érhető el: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="da87c-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="da87c-121">Az Invoke-AzRestMethod használata PATCH műveletekkel</span><span class="sxs-lookup"><span data-stu-id="da87c-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="da87c-122">Az `Invoke-AzRestMethod` parancsmaggal letilthatja a `myresourcegroup` erőforráscsoport `myacr` elnevezésű, már létező ACR-hez való nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="da87c-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="da87c-123">A nyilvános hálózati hozzáférés letiltásához az alábbi példában látható módon egy olyan API felé irányuló **PATCH** hívást kell létrehoznia, amely módosítja a `publicNetwokAccess` paraméter értékét:</span><span class="sxs-lookup"><span data-stu-id="da87c-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="da87c-124">A `Payload` tulajdonság egy olyan JSON-karakterlánc, amely megjeleníti a módosítani kívánt tulajdonság elérési útját.</span><span class="sxs-lookup"><span data-stu-id="da87c-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="da87c-125">Az API összes paraméterének leírását a hozzá tartozó **rest-api-spec** fájl tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="da87c-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="da87c-126">A publicNetworkAccess paraméter konkrét definícióját az API 2019. 12. 01-i előzetes verziójának [tárolóregisztrációs adatbázisához tartozó JSON-fájl](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="da87c-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="da87c-127">Ha a beállításjegyzékhez való hozzáférést csak egy adott IP-cím számára szeretné engedélyezni, akkor a hasznos adatokat az alábbi példa szerint kell módosítani:</span><span class="sxs-lookup"><span data-stu-id="da87c-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="da87c-128">Összehasonlítás a Get-AzResource, New-AzResource és Remove-AzResource parancsmagokkal</span><span class="sxs-lookup"><span data-stu-id="da87c-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="da87c-129">Az `*-AzResource`-parancsmagok lehetővé teszik az Azure-hoz intézett REST API-hívás testreszabását az erőforrástípus, az API-verzió és a frissítendő tulajdonságok megadásával.</span><span class="sxs-lookup"><span data-stu-id="da87c-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="da87c-130">A tulajdonságokat azonban először `PSObject` objektumként kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="da87c-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="da87c-131">Ez összetettebbé teszi a folyamatot, amely könnyen bonyolulttá válhat.</span><span class="sxs-lookup"><span data-stu-id="da87c-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="da87c-132">Az `Invoke-AzRestMethod` azonban egyszerű módot kínál az Azure-erőforrások kezelésére.</span><span class="sxs-lookup"><span data-stu-id="da87c-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="da87c-133">Ahogy az előző példában láthatta, létrehozhat egy JSON-sztringet, amellyel testre szabhatja a REST API-hívást anélkül, hogy előre létre kellene hoznia bármilyen `PSObjects` objektumot.</span><span class="sxs-lookup"><span data-stu-id="da87c-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="da87c-134">Ha már van tapasztalata az `*-AzResource`-parancsmagok használatával kapcsolatban, továbbra is használhatja őket.</span><span class="sxs-lookup"><span data-stu-id="da87c-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="da87c-135">Nem tervezzük a támogatásuk megszüntetését.</span><span class="sxs-lookup"><span data-stu-id="da87c-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="da87c-136">Az eszközkészlet legújabb tagja az `Invoke-AzRestMethod` parancsmag.</span><span class="sxs-lookup"><span data-stu-id="da87c-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="da87c-137">Lásd még:</span><span class="sxs-lookup"><span data-stu-id="da87c-137">See Also</span></span>

* [<span data-ttu-id="da87c-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="da87c-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="da87c-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="da87c-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="da87c-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="da87c-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
