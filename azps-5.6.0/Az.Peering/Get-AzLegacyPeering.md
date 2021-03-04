---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 2f1bdfd317a5578c5ce3a023f1c3cd0151026b80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937794"
---
# <span data-ttu-id="b1d42-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="b1d42-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="b1d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d42-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d42-103">Régi társviszony-kezelő erőforrások azure-erőforrás-kezelési (ARM) típusú erőforrásokká alakítása.</span><span class="sxs-lookup"><span data-stu-id="b1d42-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="b1d42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1d42-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1d42-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1d42-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d42-106">A parancs a régi társviszony-létesítő erőforrások megtekintésére szolgál, amelyeket Ön mindössze Azure Resource Management (ARM) erőforrásokká konvertál.</span><span class="sxs-lookup"><span data-stu-id="b1d42-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="b1d42-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1d42-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d42-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b1d42-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="b1d42-109">Seattle örökölt társviszony-létesítését kapja meg</span><span class="sxs-lookup"><span data-stu-id="b1d42-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="b1d42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1d42-110">PARAMETERS</span></span>

### <span data-ttu-id="b1d42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d42-111">-DefaultProfile</span></span>
<span data-ttu-id="b1d42-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1d42-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d42-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="b1d42-113">-Kind</span></span>
<span data-ttu-id="b1d42-114">Az összes társviszony-létesítő erőforrást megjeleníti kind szerint.</span><span class="sxs-lookup"><span data-stu-id="b1d42-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d42-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b1d42-115">-PeeringLocation</span></span>
<span data-ttu-id="b1d42-116">Az összes társviszony-létesítő erőforrást megjeleníti kind szerint.</span><span class="sxs-lookup"><span data-stu-id="b1d42-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d42-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d42-117">CommonParameters</span></span>
<span data-ttu-id="b1d42-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d42-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d42-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1d42-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d42-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1d42-120">INPUTS</span></span>

### <span data-ttu-id="b1d42-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1d42-121">None</span></span>

## <span data-ttu-id="b1d42-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1d42-122">OUTPUTS</span></span>

### <span data-ttu-id="b1d42-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="b1d42-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b1d42-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1d42-124">NOTES</span></span>

## <span data-ttu-id="b1d42-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1d42-125">RELATED LINKS</span></span>
