---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024509"
---
# <span data-ttu-id="b48f5-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b48f5-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="b48f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b48f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b48f5-103">A PeerAsn objektum lesz a KARJÁN.</span><span class="sxs-lookup"><span data-stu-id="b48f5-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="b48f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b48f5-104">SYNTAX</span></span>

### <span data-ttu-id="b48f5-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b48f5-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b48f5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b48f5-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b48f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b48f5-107">DESCRIPTION</span></span>
<span data-ttu-id="b48f5-108">Az előfizetéshez tartozó PeerAsn kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b48f5-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="b48f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b48f5-109">EXAMPLES</span></span>

### <span data-ttu-id="b48f5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b48f5-110">Example 1</span></span>
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

<span data-ttu-id="b48f5-111">Megkapja a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b48f5-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="b48f5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b48f5-112">PARAMETERS</span></span>

### <span data-ttu-id="b48f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48f5-113">-DefaultProfile</span></span>
<span data-ttu-id="b48f5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b48f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48f5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b48f5-115">-Name</span></span>
<span data-ttu-id="b48f5-116">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="b48f5-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b48f5-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b48f5-117">-ResourceId</span></span>
<span data-ttu-id="b48f5-118">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="b48f5-118">The resource id string name.</span></span>

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

### <span data-ttu-id="b48f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48f5-119">CommonParameters</span></span>
<span data-ttu-id="b48f5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b48f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48f5-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b48f5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48f5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b48f5-122">INPUTS</span></span>

### <span data-ttu-id="b48f5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b48f5-123">System.String</span></span>

## <span data-ttu-id="b48f5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b48f5-124">OUTPUTS</span></span>

### <span data-ttu-id="b48f5-125">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b48f5-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="b48f5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b48f5-126">NOTES</span></span>

## <span data-ttu-id="b48f5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b48f5-127">RELATED LINKS</span></span>
