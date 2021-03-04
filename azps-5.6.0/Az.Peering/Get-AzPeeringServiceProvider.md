---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937713"
---
# <span data-ttu-id="c684d-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c684d-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="c684d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c684d-102">SYNOPSIS</span></span>
<span data-ttu-id="c684d-103">A Microsofttal partneri partnerként elérhető társviszony-szolgáltatók listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c684d-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="c684d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c684d-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c684d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c684d-105">DESCRIPTION</span></span>
<span data-ttu-id="c684d-106">Társviszony-szolgáltatók felsorolása</span><span class="sxs-lookup"><span data-stu-id="c684d-106">List peering service providers</span></span>

## <span data-ttu-id="c684d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c684d-107">EXAMPLES</span></span>

### <span data-ttu-id="c684d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c684d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="c684d-109">Elérhető társviszony-szolgáltatók</span><span class="sxs-lookup"><span data-stu-id="c684d-109">Gets available peering service providers</span></span>

## <span data-ttu-id="c684d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c684d-110">PARAMETERS</span></span>

### <span data-ttu-id="c684d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c684d-111">-DefaultProfile</span></span>
<span data-ttu-id="c684d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c684d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c684d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c684d-113">CommonParameters</span></span>
<span data-ttu-id="c684d-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c684d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c684d-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c684d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c684d-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c684d-116">INPUTS</span></span>

### <span data-ttu-id="c684d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="c684d-117">None</span></span>

## <span data-ttu-id="c684d-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c684d-118">OUTPUTS</span></span>

### <span data-ttu-id="c684d-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c684d-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="c684d-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c684d-120">NOTES</span></span>

## <span data-ttu-id="c684d-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c684d-121">RELATED LINKS</span></span>
