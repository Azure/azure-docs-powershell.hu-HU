---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495053"
---
# <span data-ttu-id="442e2-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="442e2-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="442e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="442e2-102">SYNOPSIS</span></span>
<span data-ttu-id="442e2-103">Az Azure VpnSite-erőforrást név szerint kapja meg, vagy felsorolja a ResourceGroup vagy a SubscriptionId minden VpnSites.</span><span class="sxs-lookup"><span data-stu-id="442e2-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="442e2-104">Ez a cikk az Azure-ra feltöltött, a cortex virtuális központtal való S2S-kapcsolathoz feltöltött ügyfél-kirendeltségek RM-beli képviselete.</span><span class="sxs-lookup"><span data-stu-id="442e2-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442e2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="442e2-105">SYNTAX</span></span>

### <span data-ttu-id="442e2-106">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="442e2-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442e2-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442e2-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="442e2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="442e2-108">DESCRIPTION</span></span>
<span data-ttu-id="442e2-109">Az Azure VpnSite-erőforrást név szerint kapja meg, vagy felsorolja a ResourceGroup vagy a SubscriptionId minden VpnSites.</span><span class="sxs-lookup"><span data-stu-id="442e2-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="442e2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="442e2-110">EXAMPLES</span></span>

### <span data-ttu-id="442e2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="442e2-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="442e2-112">A fenti létrehoz egy erőforráscsoport, a Virtual WAN in West US in "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="442e2-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="442e2-113">Ezután létrehoz egy VpnSite, amely egy ügyfél-fióktelepet jelenít meg, és a virtuális WAN-ra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="442e2-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="442e2-114">A webhely létrehozása után a webhelyet a Get-AzureRmVpnSite parancs segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="442e2-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="442e2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="442e2-115">PARAMETERS</span></span>

### <span data-ttu-id="442e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442e2-116">-DefaultProfile</span></span>
<span data-ttu-id="442e2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="442e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="442e2-118">-Name</span></span>
<span data-ttu-id="442e2-119">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="442e2-119">The resource name.</span></span>

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

### <span data-ttu-id="442e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="442e2-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="442e2-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442e2-122">CommonParameters</span></span>
<span data-ttu-id="442e2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="442e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442e2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442e2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="442e2-125">INPUTS</span></span>

### <span data-ttu-id="442e2-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="442e2-126">None</span></span>

## <span data-ttu-id="442e2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="442e2-127">OUTPUTS</span></span>

### <span data-ttu-id="442e2-128">Microsoft. Azure. commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="442e2-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="442e2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="442e2-129">NOTES</span></span>

## <span data-ttu-id="442e2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="442e2-130">RELATED LINKS</span></span>
