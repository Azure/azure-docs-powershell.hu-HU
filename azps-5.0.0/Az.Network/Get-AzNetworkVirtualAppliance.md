---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185984"
---
# <span data-ttu-id="6584b-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6584b-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6584b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6584b-102">SYNOPSIS</span></span>
<span data-ttu-id="6584b-103">Hálózati virtuális berendezések beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="6584b-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="6584b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6584b-104">SYNTAX</span></span>

### <span data-ttu-id="6584b-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6584b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6584b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6584b-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6584b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6584b-107">DESCRIPTION</span></span>
<span data-ttu-id="6584b-108">A Get-AzNetworkVirtualAppliance parancsok hálózati virtuális eszközökhöz tartozó erőforrásokat nyernek vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="6584b-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="6584b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6584b-109">EXAMPLES</span></span>

### <span data-ttu-id="6584b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6584b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="6584b-111">Szerezzen be egy hálózati virtuális készülék erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6584b-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6584b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6584b-112">PARAMETERS</span></span>

### <span data-ttu-id="6584b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6584b-113">-DefaultProfile</span></span>
<span data-ttu-id="6584b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6584b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6584b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6584b-115">-Name</span></span>
<span data-ttu-id="6584b-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6584b-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6584b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6584b-117">-ResourceGroupName</span></span>
<span data-ttu-id="6584b-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6584b-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6584b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6584b-119">-ResourceId</span></span>
<span data-ttu-id="6584b-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6584b-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6584b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6584b-121">CommonParameters</span></span>
<span data-ttu-id="6584b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6584b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6584b-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6584b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6584b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6584b-124">INPUTS</span></span>

### <span data-ttu-id="6584b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6584b-125">System.String</span></span>

## <span data-ttu-id="6584b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6584b-126">OUTPUTS</span></span>

### <span data-ttu-id="6584b-127">Microsoft. Azure. commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6584b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6584b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6584b-128">NOTES</span></span>

## <span data-ttu-id="6584b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6584b-129">RELATED LINKS</span></span>