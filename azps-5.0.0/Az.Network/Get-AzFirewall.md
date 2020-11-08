---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194554"
---
# <span data-ttu-id="69c90-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="69c90-101">Get-AzFirewall</span></span>

## <span data-ttu-id="69c90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69c90-102">SYNOPSIS</span></span>
<span data-ttu-id="69c90-103">Azure-tűzfalat kap.</span><span class="sxs-lookup"><span data-stu-id="69c90-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="69c90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69c90-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69c90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69c90-105">DESCRIPTION</span></span>
<span data-ttu-id="69c90-106">A **Get-AzFirewall** parancsmag egy vagy több tűzfalat kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="69c90-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="69c90-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69c90-107">EXAMPLES</span></span>

### <span data-ttu-id="69c90-108">1: az összes tűzfal lekérése egy erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="69c90-108">1:  Retrieve all Firewalls in a resource group</span></span>
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

<span data-ttu-id="69c90-109">Ebben a példában a "rgName" erőforráscsoporthoz tartozó összes tűzfalat beolvassa.</span><span class="sxs-lookup"><span data-stu-id="69c90-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="69c90-110">2: tűzfal beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="69c90-110">2:  Retrieve a Firewall by name</span></span>
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

<span data-ttu-id="69c90-111">Ez a példa a "azFw" nevű tűzfalat olvassa be a "rgName" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="69c90-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="69c90-112">3: az összes tűzfal lekérése szűréssel</span><span class="sxs-lookup"><span data-stu-id="69c90-112">3:  Retrieve all Firewalls with filtering</span></span>
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

<span data-ttu-id="69c90-113">Ez a példa beolvassa az összes "azFw" kezdetű tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="69c90-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="69c90-114">4: a tűzfal lekérése, majd az alkalmazási szabályok gyűjteményének hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="69c90-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="69c90-115">Ez a példa beolvassa a tűzfalat, majd felvesz egy alkalmazási szabályt a tűzfalba a hívási mód AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="69c90-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="69c90-116">5: a tűzfal lekérése, majd a hálózati szabályok gyűjteményének hozzáadása a tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="69c90-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="69c90-117">Ez a példa beolvassa a tűzfalat, majd egy hálózati szabály gyűjteményt ad a tűzfalhoz a hívási mód AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="69c90-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="69c90-118">6: a tűzfal lekérése, majd egy alkalmazási szabály gyűjteményének beolvasása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="69c90-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="69c90-119">Ez a példa beolvassa a tűzfalat, és a GetApplicationRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="69c90-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="69c90-120">A szabály GetApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="69c90-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="69c90-121">7: a tűzfal lekérése, majd egy hálózati szabály-gyűjtemény beolvasása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="69c90-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="69c90-122">Ez a példa beolvassa a tűzfalat, és a GetNetworkRuleCollectionByName a tűzfal objektumon név szerint begyűjti a szabályok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="69c90-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="69c90-123">A szabály GetNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="69c90-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="69c90-124">8: a tűzfal lekérése, majd az alkalmazás szabály-gyűjteményének eltávolítása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="69c90-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="69c90-125">Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveApplicationRuleCollectionByName a tűzfal objektumon.</span><span class="sxs-lookup"><span data-stu-id="69c90-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="69c90-126">A szabály RemoveApplicationRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="69c90-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="69c90-127">9: tűzfal beolvasása és a hálózati szabály gyűjteményének eltávolítása a tűzfalból</span><span class="sxs-lookup"><span data-stu-id="69c90-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="69c90-128">Ez a példa beolvassa a tűzfalat, majd eltávolítja a szabályok gyűjteményét név szerint, a hívási mód RemoveNetworkRuleCollectionByName a tűzfal objektumon.</span><span class="sxs-lookup"><span data-stu-id="69c90-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="69c90-129">A szabály RemoveNetworkRuleCollectionByName a kis-és nagybetűk megkülönböztetésére használható.</span><span class="sxs-lookup"><span data-stu-id="69c90-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="69c90-130">10: a tűzfal lekérése, majd a tűzfal lefoglalása</span><span class="sxs-lookup"><span data-stu-id="69c90-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="69c90-131">Ebben a példában egy tűzfal és a hívások lefoglalása a tűzfalon a tűzfalhoz társított konfiguráció (alkalmazás és hálózati szabály gyűjtemény) segítségével indítható el.</span><span class="sxs-lookup"><span data-stu-id="69c90-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="69c90-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69c90-132">PARAMETERS</span></span>

### <span data-ttu-id="69c90-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c90-133">-DefaultProfile</span></span>
<span data-ttu-id="69c90-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69c90-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c90-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69c90-135">-Name</span></span>
<span data-ttu-id="69c90-136">Annak a tűzfalnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="69c90-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69c90-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c90-137">-ResourceGroupName</span></span>
<span data-ttu-id="69c90-138">Annak a csoportnak a neve, amelyhez a tűzfal tartozik.</span><span class="sxs-lookup"><span data-stu-id="69c90-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="69c90-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c90-139">CommonParameters</span></span>
<span data-ttu-id="69c90-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69c90-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c90-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69c90-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c90-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c90-142">INPUTS</span></span>

### <span data-ttu-id="69c90-143">System. String</span><span class="sxs-lookup"><span data-stu-id="69c90-143">System.String</span></span>

## <span data-ttu-id="69c90-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c90-144">OUTPUTS</span></span>

### <span data-ttu-id="69c90-145">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="69c90-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="69c90-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="69c90-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="69c90-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69c90-147">NOTES</span></span>

## <span data-ttu-id="69c90-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c90-148">RELATED LINKS</span></span>

[<span data-ttu-id="69c90-149">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="69c90-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="69c90-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="69c90-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="69c90-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="69c90-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)