---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 9498183e66a0991f7a724065bb5a88e954cd6594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937793"
---
# <span data-ttu-id="faa4c-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="faa4c-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="faa4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa4c-102">SYNOPSIS</span></span>
<span data-ttu-id="faa4c-103">Társközi objektum be ARM.</span><span class="sxs-lookup"><span data-stu-id="faa4c-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="faa4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="faa4c-104">SYNTAX</span></span>

### <span data-ttu-id="faa4c-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="faa4c-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faa4c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="faa4c-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faa4c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="faa4c-107">DESCRIPTION</span></span>
<span data-ttu-id="faa4c-108">A PeerAsn-t lekérte egy előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="faa4c-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="faa4c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="faa4c-109">EXAMPLES</span></span>

### <span data-ttu-id="faa4c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="faa4c-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="faa4c-111">A PeerAsn lekérte</span><span class="sxs-lookup"><span data-stu-id="faa4c-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="faa4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faa4c-112">PARAMETERS</span></span>

### <span data-ttu-id="faa4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa4c-113">-DefaultProfile</span></span>
<span data-ttu-id="faa4c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faa4c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa4c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="faa4c-115">-Name</span></span>
<span data-ttu-id="faa4c-116">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="faa4c-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa4c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faa4c-117">-ResourceId</span></span>
<span data-ttu-id="faa4c-118">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="faa4c-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa4c-119">CommonParameters</span></span>
<span data-ttu-id="faa4c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa4c-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faa4c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa4c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faa4c-122">INPUTS</span></span>

### <span data-ttu-id="faa4c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="faa4c-123">System.String</span></span>

## <span data-ttu-id="faa4c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faa4c-124">OUTPUTS</span></span>

### <span data-ttu-id="faa4c-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="faa4c-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="faa4c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="faa4c-126">NOTES</span></span>

## <span data-ttu-id="faa4c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faa4c-127">RELATED LINKS</span></span>
