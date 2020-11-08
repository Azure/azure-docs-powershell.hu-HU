---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 559d2d8c069d7e36630600d0fcdc16ea475da9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014491"
---
# <span data-ttu-id="94c3c-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="94c3c-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="94c3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="94c3c-103">A PeerAsn objektum lesz a KARJÁN.</span><span class="sxs-lookup"><span data-stu-id="94c3c-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="94c3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94c3c-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="94c3c-106">Az előfizetéshez tartozó PeerAsn kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94c3c-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="94c3c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="94c3c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94c3c-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="94c3c-109">Megkapja a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="94c3c-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="94c3c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="94c3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c3c-111">-DefaultProfile</span></span>
<span data-ttu-id="94c3c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94c3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c3c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94c3c-113">-Name</span></span>
<span data-ttu-id="94c3c-114">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="94c3c-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c3c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c3c-115">CommonParameters</span></span>
<span data-ttu-id="94c3c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94c3c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c3c-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94c3c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c3c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94c3c-118">INPUTS</span></span>

### <span data-ttu-id="94c3c-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="94c3c-119">None</span></span>

## <span data-ttu-id="94c3c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94c3c-120">OUTPUTS</span></span>

### <span data-ttu-id="94c3c-121">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="94c3c-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="94c3c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94c3c-122">NOTES</span></span>

## <span data-ttu-id="94c3c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94c3c-123">RELATED LINKS</span></span>
