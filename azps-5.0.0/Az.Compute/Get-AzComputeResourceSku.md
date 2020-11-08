---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185626"
---
# <span data-ttu-id="0211d-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="0211d-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="0211d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0211d-102">SYNOPSIS</span></span>
<span data-ttu-id="0211d-103">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="0211d-103">List all compute resource Skus</span></span>

## <span data-ttu-id="0211d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0211d-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0211d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0211d-105">DESCRIPTION</span></span>
<span data-ttu-id="0211d-106">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="0211d-106">List all compute resource Skus</span></span>

## <span data-ttu-id="0211d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0211d-107">EXAMPLES</span></span>

### <span data-ttu-id="0211d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0211d-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="0211d-109">Az összes számítási erőforrás listázása a Nyugat-amerikai régióban</span><span class="sxs-lookup"><span data-stu-id="0211d-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="0211d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0211d-110">PARAMETERS</span></span>

### <span data-ttu-id="0211d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0211d-111">-DefaultProfile</span></span>
<span data-ttu-id="0211d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0211d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0211d-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="0211d-113">-Location</span></span>
<span data-ttu-id="0211d-114">A rendelkezésre álló SKU-lista helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0211d-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="0211d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0211d-115">CommonParameters</span></span>
<span data-ttu-id="0211d-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0211d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0211d-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0211d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0211d-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0211d-118">INPUTS</span></span>

### <span data-ttu-id="0211d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0211d-119">System.String</span></span>

## <span data-ttu-id="0211d-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0211d-120">OUTPUTS</span></span>

### <span data-ttu-id="0211d-121">Microsoft. Azure. commands. számítási. Automation. models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="0211d-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="0211d-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0211d-122">NOTES</span></span>

## <span data-ttu-id="0211d-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0211d-123">RELATED LINKS</span></span>
