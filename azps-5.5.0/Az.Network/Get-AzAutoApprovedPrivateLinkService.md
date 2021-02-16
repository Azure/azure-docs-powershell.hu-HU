---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157050"
---
# <span data-ttu-id="92425-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92425-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="92425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92425-102">SYNOPSIS</span></span>
<span data-ttu-id="92425-103">Olyan privát hivatkozásszolgáltatás-azonosító tömböt kap, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="92425-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="92425-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92425-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92425-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92425-105">DESCRIPTION</span></span>
<span data-ttu-id="92425-106">A **Get-AzAutoApprovedPrivateLinkService** egy privát hivatkozásszolgáltatás-azonosító tömbje, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="92425-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="92425-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92425-107">EXAMPLES</span></span>

### <span data-ttu-id="92425-108">Példa</span><span class="sxs-lookup"><span data-stu-id="92425-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="92425-109">Ez a példa egy privát hivatkozásszolgáltatás-azonosító tömböt ad vissza, amely az automatikus jóváhagyással egy privát végponthoz csatolható.</span><span class="sxs-lookup"><span data-stu-id="92425-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="92425-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92425-110">PARAMETERS</span></span>

### <span data-ttu-id="92425-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92425-111">-DefaultProfile</span></span>
<span data-ttu-id="92425-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92425-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92425-113">-Location</span><span class="sxs-lookup"><span data-stu-id="92425-113">-Location</span></span>
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

### <span data-ttu-id="92425-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92425-114">-ResourceGroupName</span></span>
<span data-ttu-id="92425-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92425-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="92425-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92425-116">CommonParameters</span></span>
<span data-ttu-id="92425-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92425-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92425-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92425-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92425-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92425-119">INPUTS</span></span>

### <span data-ttu-id="92425-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="92425-120">None</span></span>

## <span data-ttu-id="92425-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92425-121">OUTPUTS</span></span>

### <span data-ttu-id="92425-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92425-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="92425-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92425-123">NOTES</span></span>

## <span data-ttu-id="92425-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92425-124">RELATED LINKS</span></span>
