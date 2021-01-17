---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365971"
---
# <span data-ttu-id="5ca29-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5ca29-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="5ca29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca29-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca29-103">Egy Azure VpnSite-erőforrást kap név vagy név szerint egy ResourceGroup vagy SubscriptionId szolgáltatásban található összes VpnSites-listában.</span><span class="sxs-lookup"><span data-stu-id="5ca29-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="5ca29-104">Ez egy rm representation of customer branches that are uploaded to Azure for S2S connectivity with a Virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="5ca29-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5ca29-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ca29-105">SYNTAX</span></span>

### <span data-ttu-id="5ca29-106">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ca29-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca29-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca29-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ca29-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ca29-108">DESCRIPTION</span></span>
<span data-ttu-id="5ca29-109">Egy Azure VpnSite-erőforrást kap név vagy név szerint egy ResourceGroup vagy SubscriptionId szolgáltatásban található összes VpnSites-listában.</span><span class="sxs-lookup"><span data-stu-id="5ca29-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="5ca29-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ca29-110">EXAMPLES</span></span>

### <span data-ttu-id="5ca29-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5ca29-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="5ca29-112">A fenti létrehoz egy erőforráscsoportot (Virtuális WAN az Egyesült Államok nyugati részén, "testRG" erőforráscsoportként az Azure-ban).</span><span class="sxs-lookup"><span data-stu-id="5ca29-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="5ca29-113">Ezután létrehoz egy VpnSite-t, amely egy ügyfélágat képvisel, és a virtuális WAN-hoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="5ca29-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="5ca29-114">A webhely létrehozása után a webhelyet a Get-AzVpnSite paranccsal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca29-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="5ca29-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="5ca29-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="5ca29-116">Ez a parancsmag az összes "teszt" kezdetú webhelyet beveszi.</span><span class="sxs-lookup"><span data-stu-id="5ca29-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="5ca29-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca29-117">PARAMETERS</span></span>

### <span data-ttu-id="5ca29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca29-118">-DefaultProfile</span></span>
<span data-ttu-id="5ca29-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ca29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5ca29-120">-Name</span></span>
<span data-ttu-id="5ca29-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5ca29-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca29-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ca29-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ca29-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca29-124">CommonParameters</span></span>
<span data-ttu-id="5ca29-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca29-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca29-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca29-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca29-127">INPUTS</span></span>

### <span data-ttu-id="5ca29-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="5ca29-128">None</span></span>

## <span data-ttu-id="5ca29-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca29-129">OUTPUTS</span></span>

### <span data-ttu-id="5ca29-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="5ca29-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="5ca29-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ca29-131">NOTES</span></span>

## <span data-ttu-id="5ca29-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca29-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ca29-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5ca29-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="5ca29-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5ca29-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="5ca29-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5ca29-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
