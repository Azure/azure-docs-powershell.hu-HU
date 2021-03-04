---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934490"
---
# <span data-ttu-id="297dd-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="297dd-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="297dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="297dd-102">SYNOPSIS</span></span>
<span data-ttu-id="297dd-103">Az összes számítási erőforrás-skus felsorolása</span><span class="sxs-lookup"><span data-stu-id="297dd-103">List all compute resource Skus</span></span>

## <span data-ttu-id="297dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="297dd-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="297dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="297dd-105">DESCRIPTION</span></span>
<span data-ttu-id="297dd-106">Az összes számítási erőforrás-skus felsorolása</span><span class="sxs-lookup"><span data-stu-id="297dd-106">List all compute resource Skus</span></span>

## <span data-ttu-id="297dd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="297dd-107">EXAMPLES</span></span>

### <span data-ttu-id="297dd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="297dd-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="297dd-109">Az összes számítási erőforrás-skus felsorolása az Amerikai Egyesült Térség nyugati részén</span><span class="sxs-lookup"><span data-stu-id="297dd-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="297dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="297dd-110">PARAMETERS</span></span>

### <span data-ttu-id="297dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297dd-111">-DefaultProfile</span></span>
<span data-ttu-id="297dd-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="297dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="297dd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="297dd-113">-Location</span></span>
<span data-ttu-id="297dd-114">Megadja a listához rendelkezésre álló lista összes elemének helyét.</span><span class="sxs-lookup"><span data-stu-id="297dd-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297dd-115">CommonParameters</span></span>
<span data-ttu-id="297dd-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297dd-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="297dd-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297dd-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="297dd-118">INPUTS</span></span>

### <span data-ttu-id="297dd-119">System.String</span><span class="sxs-lookup"><span data-stu-id="297dd-119">System.String</span></span>

## <span data-ttu-id="297dd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="297dd-120">OUTPUTS</span></span>

### <span data-ttu-id="297dd-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="297dd-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="297dd-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="297dd-122">NOTES</span></span>

## <span data-ttu-id="297dd-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="297dd-123">RELATED LINKS</span></span>
