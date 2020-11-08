---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014492"
---
# <span data-ttu-id="4387e-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="4387e-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="4387e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4387e-102">SYNOPSIS</span></span>
<span data-ttu-id="4387e-103">Segítségével örökölt társközi erőforrásokat konvertálhat az Azure Resource Management (ARM) erőforrásaira.</span><span class="sxs-lookup"><span data-stu-id="4387e-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="4387e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4387e-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4387e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4387e-105">DESCRIPTION</span></span>
<span data-ttu-id="4387e-106">A parancs segítségével megtekintheti azokat az örökölt társközi erőforrásokat, amelyek mindegyike az Azure erőforrás-kezelési (ARM) erőforrásokra konvertálja őket.</span><span class="sxs-lookup"><span data-stu-id="4387e-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="4387e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4387e-107">EXAMPLES</span></span>

### <span data-ttu-id="4387e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4387e-108">Example 1</span></span>
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

<span data-ttu-id="4387e-109">A korábbi peering for Seattle</span><span class="sxs-lookup"><span data-stu-id="4387e-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="4387e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4387e-110">PARAMETERS</span></span>

### <span data-ttu-id="4387e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4387e-111">-DefaultProfile</span></span>
<span data-ttu-id="4387e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4387e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4387e-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="4387e-113">-Kind</span></span>
<span data-ttu-id="4387e-114">A teljes egyenrangú erőforrást jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4387e-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="4387e-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="4387e-115">-PeeringLocation</span></span>
<span data-ttu-id="4387e-116">A teljes egyenrangú erőforrást jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4387e-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="4387e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4387e-117">CommonParameters</span></span>
<span data-ttu-id="4387e-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4387e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4387e-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4387e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4387e-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4387e-120">INPUTS</span></span>

### <span data-ttu-id="4387e-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="4387e-121">None</span></span>

## <span data-ttu-id="4387e-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4387e-122">OUTPUTS</span></span>

### <span data-ttu-id="4387e-123">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="4387e-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="4387e-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4387e-124">NOTES</span></span>

## <span data-ttu-id="4387e-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4387e-125">RELATED LINKS</span></span>
