---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3ca8c522e3aa4d31e5718d09fffe0ff22fd4cab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006294"
---
# <span data-ttu-id="ee0df-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ee0df-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ee0df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0df-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0df-103">Virtuális hálózati készülékek be- vagy listába való be- vagy listába való be szereznie.</span><span class="sxs-lookup"><span data-stu-id="ee0df-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="ee0df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee0df-104">SYNTAX</span></span>

### <span data-ttu-id="ee0df-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee0df-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee0df-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee0df-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee0df-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee0df-107">DESCRIPTION</span></span>
<span data-ttu-id="ee0df-108">A Get-AzNetworkVirtualAppliance parancsok a hálózati virtuális eszköz erőforrásait kapják vagy sorolják fel.</span><span class="sxs-lookup"><span data-stu-id="ee0df-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="ee0df-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee0df-109">EXAMPLES</span></span>

### <span data-ttu-id="ee0df-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ee0df-110">Example 1</span></span>
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

<span data-ttu-id="ee0df-111">Hálózati virtuális eszköz típusú erőforrás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ee0df-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ee0df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee0df-112">PARAMETERS</span></span>

### <span data-ttu-id="ee0df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0df-113">-DefaultProfile</span></span>
<span data-ttu-id="ee0df-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee0df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee0df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0df-115">-Name</span></span>
<span data-ttu-id="ee0df-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ee0df-116">The resource name.</span></span>

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

### <span data-ttu-id="ee0df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0df-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee0df-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee0df-118">The resource group name.</span></span>

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

### <span data-ttu-id="ee0df-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee0df-119">-ResourceId</span></span>
<span data-ttu-id="ee0df-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee0df-120">The resource Id.</span></span>

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

### <span data-ttu-id="ee0df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0df-121">CommonParameters</span></span>
<span data-ttu-id="ee0df-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0df-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee0df-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0df-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee0df-124">INPUTS</span></span>

### <span data-ttu-id="ee0df-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ee0df-125">System.String</span></span>

## <span data-ttu-id="ee0df-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee0df-126">OUTPUTS</span></span>

### <span data-ttu-id="ee0df-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ee0df-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ee0df-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee0df-128">NOTES</span></span>

## <span data-ttu-id="ee0df-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee0df-129">RELATED LINKS</span></span>
