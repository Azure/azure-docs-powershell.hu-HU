---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159186"
---
# <span data-ttu-id="f7c2e-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f7c2e-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f7c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c2e-103">Virtuális hálózati készülékek be- vagy listába való be- vagy listába való be szereznie.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="f7c2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7c2e-104">SYNTAX</span></span>

### <span data-ttu-id="f7c2e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7c2e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c2e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c2e-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7c2e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7c2e-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c2e-108">A Get-AzNetworkVirtualAppliance parancsok a hálózati virtuális eszköz erőforrásait kapják vagy sorolják fel.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="f7c2e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7c2e-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c2e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7c2e-110">Example 1</span></span>
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

<span data-ttu-id="f7c2e-111">Hálózati virtuális eszköz típusú erőforrás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f7c2e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7c2e-112">PARAMETERS</span></span>

### <span data-ttu-id="f7c2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c2e-113">-DefaultProfile</span></span>
<span data-ttu-id="f7c2e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7c2e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c2e-115">-Name</span></span>
<span data-ttu-id="f7c2e-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-116">The resource name.</span></span>

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

### <span data-ttu-id="f7c2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7c2e-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-118">The resource group name.</span></span>

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

### <span data-ttu-id="f7c2e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7c2e-119">-ResourceId</span></span>
<span data-ttu-id="f7c2e-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-120">The resource Id.</span></span>

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

### <span data-ttu-id="f7c2e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c2e-121">CommonParameters</span></span>
<span data-ttu-id="f7c2e-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c2e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c2e-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7c2e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c2e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7c2e-124">INPUTS</span></span>

### <span data-ttu-id="f7c2e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f7c2e-125">System.String</span></span>

## <span data-ttu-id="f7c2e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7c2e-126">OUTPUTS</span></span>

### <span data-ttu-id="f7c2e-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f7c2e-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f7c2e-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7c2e-128">NOTES</span></span>

## <span data-ttu-id="f7c2e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7c2e-129">RELATED LINKS</span></span>
