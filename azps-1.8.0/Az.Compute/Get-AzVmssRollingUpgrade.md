---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836770"
---
# <span data-ttu-id="bc30f-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="bc30f-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="bc30f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc30f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc30f-103">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="bc30f-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="bc30f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc30f-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc30f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc30f-105">DESCRIPTION</span></span>
<span data-ttu-id="bc30f-106">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="bc30f-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="bc30f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc30f-107">EXAMPLES</span></span>

### <span data-ttu-id="bc30f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc30f-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="bc30f-109">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS legújabb folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="bc30f-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="bc30f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc30f-110">PARAMETERS</span></span>

### <span data-ttu-id="bc30f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc30f-111">-DefaultProfile</span></span>
<span data-ttu-id="bc30f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc30f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc30f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc30f-113">-ResourceGroupName</span></span>
<span data-ttu-id="bc30f-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc30f-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc30f-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bc30f-115">-VMScaleSetName</span></span>
<span data-ttu-id="bc30f-116">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="bc30f-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="bc30f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc30f-117">CommonParameters</span></span>
<span data-ttu-id="bc30f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc30f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc30f-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc30f-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc30f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc30f-120">INPUTS</span></span>

### <span data-ttu-id="bc30f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bc30f-121">System.String</span></span>

## <span data-ttu-id="bc30f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc30f-122">OUTPUTS</span></span>

### <span data-ttu-id="bc30f-123">Microsoft. Azure. commands. számítási. Automation. models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="bc30f-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="bc30f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc30f-124">NOTES</span></span>

## <span data-ttu-id="bc30f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc30f-125">RELATED LINKS</span></span>
