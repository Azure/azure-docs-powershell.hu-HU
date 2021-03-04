---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940257"
---
# <span data-ttu-id="f242a-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f242a-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="f242a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f242a-102">SYNOPSIS</span></span>
<span data-ttu-id="f242a-103">Olyan privát hivatkozásszolgáltatás-azonosító tömböt kap, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="f242a-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f242a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f242a-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f242a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f242a-105">DESCRIPTION</span></span>
<span data-ttu-id="f242a-106">A **Get-AzAutoApprovedPrivateLinkService** egy privát hivatkozásszolgáltatás-azonosító tömbje, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="f242a-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f242a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f242a-107">EXAMPLES</span></span>

### <span data-ttu-id="f242a-108">Példa</span><span class="sxs-lookup"><span data-stu-id="f242a-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="f242a-109">Ez a példa egy privát hivatkozásszolgáltatás-azonosító tömböt ad vissza, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="f242a-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f242a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f242a-110">PARAMETERS</span></span>

### <span data-ttu-id="f242a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f242a-111">-DefaultProfile</span></span>
<span data-ttu-id="f242a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f242a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f242a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f242a-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f242a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f242a-114">-ResourceGroupName</span></span>
<span data-ttu-id="f242a-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f242a-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f242a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f242a-116">CommonParameters</span></span>
<span data-ttu-id="f242a-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f242a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f242a-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f242a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f242a-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f242a-119">INPUTS</span></span>

### <span data-ttu-id="f242a-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="f242a-120">None</span></span>

## <span data-ttu-id="f242a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f242a-121">OUTPUTS</span></span>

### <span data-ttu-id="f242a-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f242a-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="f242a-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f242a-123">NOTES</span></span>

## <span data-ttu-id="f242a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f242a-124">RELATED LINKS</span></span>
