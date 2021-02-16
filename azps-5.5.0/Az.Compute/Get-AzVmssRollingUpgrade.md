---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144946"
---
# <span data-ttu-id="7a7c2-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a7c2-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="7a7c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7c2-103">A legújabb virtuálisgép-méretarányú frissítés állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="7a7c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a7c2-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7c2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7c2-106">A legújabb virtuálisgép-méretarányú frissítés állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="7a7c2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7c2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a7c2-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7a7c2-109">Ez a parancs a VMSS001 nevű VMSS legújabb, gördülő frissítésének állapotát mutatja, amely a Group001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7a7c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a7c2-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7c2-111">-DefaultProfile</span></span>
<span data-ttu-id="7a7c2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7c2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7c2-113">-ResourceGroupName</span></span>
<span data-ttu-id="7a7c2-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c2-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7a7c2-115">-VMScaleSetName</span></span>
<span data-ttu-id="7a7c2-116">A VM-méretkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7c2-117">CommonParameters</span></span>
<span data-ttu-id="7a7c2-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7c2-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a7c2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7c2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a7c2-120">INPUTS</span></span>

### <span data-ttu-id="7a7c2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7a7c2-121">System.String</span></span>

## <span data-ttu-id="7a7c2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7c2-122">OUTPUTS</span></span>

### <span data-ttu-id="7a7c2-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="7a7c2-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="7a7c2-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a7c2-124">NOTES</span></span>

## <span data-ttu-id="7a7c2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a7c2-125">RELATED LINKS</span></span>
