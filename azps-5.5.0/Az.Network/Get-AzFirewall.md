---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161114"
---
# <span data-ttu-id="850c0-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="850c0-101">Get-AzFirewall</span></span>

## <span data-ttu-id="850c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850c0-102">SYNOPSIS</span></span>
<span data-ttu-id="850c0-103">Azure tűzfalat kap.</span><span class="sxs-lookup"><span data-stu-id="850c0-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="850c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="850c0-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="850c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="850c0-105">DESCRIPTION</span></span>
<span data-ttu-id="850c0-106">A **Get-AzFirewall** parancsmag egy vagy több tűzfalat kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="850c0-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="850c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="850c0-107">EXAMPLES</span></span>

### <span data-ttu-id="850c0-108">1: Erőforráscsoport összes tűzfalának beolvasása</span><span class="sxs-lookup"><span data-stu-id="850c0-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="850c0-109">Ez a példa beolvassa az "rgName" erőforráscsoport összes tűzfalát.</span><span class="sxs-lookup"><span data-stu-id="850c0-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="850c0-110">2: Tűzfal beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="850c0-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="850c0-111">Ez a példa beolvassa az "azFw" nevű tűzfalat az "rgName" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="850c0-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="850c0-112">3: Az összes tűzfal beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="850c0-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="850c0-113">Ez a példa beolvassa az összes tűzfalat, amely az "azFw" kezdetekkel kezdődik</span><span class="sxs-lookup"><span data-stu-id="850c0-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="850c0-114">4: Tűzfal lekérése, majd alkalmazásszabálygyűjtemény hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="850c0-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="850c0-115">Ez a példa beolvas egy tűzfalat, majd hozzáad egy alkalmazásszabálygyűjteményt a tűzfalhoz az AddApplicationRuleCollection hívási módszerrel.</span><span class="sxs-lookup"><span data-stu-id="850c0-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="850c0-116">5: Tűzfal lekérése, majd hálózati szabálygyűjtemény hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="850c0-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="850c0-117">Ez a példa beolvas egy tűzfalat, majd hozzáad egy hálózati szabálygyűjteményt a tűzfalhoz az AddNetworkRuleCollection hívási módszerrel.</span><span class="sxs-lookup"><span data-stu-id="850c0-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="850c0-118">6: Tűzfal lekérése, majd egy alkalmazásszabálygyűjtemény beolvasása név szerint a tűzfalról</span><span class="sxs-lookup"><span data-stu-id="850c0-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="850c0-119">Ez a példa beolvas egy tűzfalat, majd név szerint beolvas egy szabálygyűjteményt, amely a GetApplicationRuleCollectionByName hívási módszert használja a tűzfalobjektumon.</span><span class="sxs-lookup"><span data-stu-id="850c0-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="850c0-120">A GetApplicationRuleCollectionByName metódus szabálygyűjteményének neve a kis- és</span><span class="sxs-lookup"><span data-stu-id="850c0-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="850c0-121">7: Tűzfal lekérése, majd hálózati szabálygyűjtemény beolvasása név szerint a tűzfalról</span><span class="sxs-lookup"><span data-stu-id="850c0-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="850c0-122">Ez a példa beolvas egy tűzfalat, majd név szerint beolvas egy szabálygyűjteményt, amely a GetNetworkRuleCollectionByName hívási módszert használja a tűzfalobjektumon.</span><span class="sxs-lookup"><span data-stu-id="850c0-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="850c0-123">A GetNetworkRuleCollectionByName metódus szabálygyűjteményének neve nem ékezetes.</span><span class="sxs-lookup"><span data-stu-id="850c0-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="850c0-124">8: Tűzfal lekérése, majd egy alkalmazásszabálygyűjtemény eltávolítása név szerint a tűzfalról</span><span class="sxs-lookup"><span data-stu-id="850c0-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="850c0-125">Ez a példa beolvassa a tűzfalat, majd név szerint eltávolítja a szabálygyűjteményt, a removeApplicationRuleCollectionByName hívási módszert a tűzfalobjektumon.</span><span class="sxs-lookup"><span data-stu-id="850c0-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="850c0-126">A RemoveApplicationRuleCollectionByName metódus szabálygyűjteményének neve a kis- és</span><span class="sxs-lookup"><span data-stu-id="850c0-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="850c0-127">9: Tűzfal lekérése, majd egy hálózati szabálygyűjtemény eltávolítása név szerint a tűzfalról</span><span class="sxs-lookup"><span data-stu-id="850c0-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="850c0-128">Ez a példa beolvassa a tűzfalat, majd név szerint eltávolítja a szabálygyűjteményt a RemoveNetworkRuleCollectionByName hívási módszerrel a tűzfalobjektumon.</span><span class="sxs-lookup"><span data-stu-id="850c0-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="850c0-129">A RemoveNetworkRuleCollectionByName metódus szabálygyűjteményének neve nem ékezetes.</span><span class="sxs-lookup"><span data-stu-id="850c0-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="850c0-130">10: Tűzfal lekérése és a tűzfal kiosztása</span><span class="sxs-lookup"><span data-stu-id="850c0-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="850c0-131">Ez a példa beolvas egy tűzfalat, és felhívja a Tűzfal kiosztása szolgáltatást a tűzfalhoz társított konfiguráció (alkalmazás- és hálózati szabálygyűjtemények) használatával való indításhoz.</span><span class="sxs-lookup"><span data-stu-id="850c0-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="850c0-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="850c0-132">PARAMETERS</span></span>

### <span data-ttu-id="850c0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850c0-133">-DefaultProfile</span></span>
<span data-ttu-id="850c0-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="850c0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850c0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="850c0-135">-Name</span></span>
<span data-ttu-id="850c0-136">Annak a tűzfalnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="850c0-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850c0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850c0-137">-ResourceGroupName</span></span>
<span data-ttu-id="850c0-138">Annak az erőforráscsoportnak a neve, amelyhez a tűzfal tartozik.</span><span class="sxs-lookup"><span data-stu-id="850c0-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850c0-139">CommonParameters</span></span>
<span data-ttu-id="850c0-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850c0-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="850c0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850c0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="850c0-142">INPUTS</span></span>

### <span data-ttu-id="850c0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="850c0-143">System.String</span></span>

## <span data-ttu-id="850c0-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="850c0-144">OUTPUTS</span></span>

### <span data-ttu-id="850c0-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="850c0-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="850c0-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="850c0-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="850c0-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="850c0-147">NOTES</span></span>

## <span data-ttu-id="850c0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="850c0-148">RELATED LINKS</span></span>

[<span data-ttu-id="850c0-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="850c0-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="850c0-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="850c0-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="850c0-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="850c0-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
