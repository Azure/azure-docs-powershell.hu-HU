---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158691"
---
# <span data-ttu-id="007dc-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="007dc-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="007dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="007dc-102">SYNOPSIS</span></span>
<span data-ttu-id="007dc-103">Társközi objektum be ARM.</span><span class="sxs-lookup"><span data-stu-id="007dc-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="007dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="007dc-104">SYNTAX</span></span>

### <span data-ttu-id="007dc-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="007dc-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="007dc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="007dc-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="007dc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="007dc-107">DESCRIPTION</span></span>
<span data-ttu-id="007dc-108">A PeerAsn-t lekérte egy előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="007dc-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="007dc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="007dc-109">EXAMPLES</span></span>

### <span data-ttu-id="007dc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="007dc-110">Example 1</span></span>
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

<span data-ttu-id="007dc-111">A PeerAsn-t kapja</span><span class="sxs-lookup"><span data-stu-id="007dc-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="007dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="007dc-112">PARAMETERS</span></span>

### <span data-ttu-id="007dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007dc-113">-DefaultProfile</span></span>
<span data-ttu-id="007dc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="007dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="007dc-115">-Name</span></span>
<span data-ttu-id="007dc-116">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="007dc-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="007dc-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="007dc-117">-ResourceId</span></span>
<span data-ttu-id="007dc-118">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="007dc-118">The resource id string name.</span></span>

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

### <span data-ttu-id="007dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007dc-119">CommonParameters</span></span>
<span data-ttu-id="007dc-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007dc-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="007dc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007dc-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="007dc-122">INPUTS</span></span>

### <span data-ttu-id="007dc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="007dc-123">System.String</span></span>

## <span data-ttu-id="007dc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="007dc-124">OUTPUTS</span></span>

### <span data-ttu-id="007dc-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="007dc-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="007dc-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="007dc-126">NOTES</span></span>

## <span data-ttu-id="007dc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="007dc-127">RELATED LINKS</span></span>
