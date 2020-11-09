---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301529"
---
# <span data-ttu-id="1cafd-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="1cafd-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="1cafd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cafd-102">SYNOPSIS</span></span>
<span data-ttu-id="1cafd-103">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1cafd-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="1cafd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cafd-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cafd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cafd-105">DESCRIPTION</span></span>
<span data-ttu-id="1cafd-106">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1cafd-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="1cafd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1cafd-107">EXAMPLES</span></span>

### <span data-ttu-id="1cafd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1cafd-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="1cafd-109">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS legújabb folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1cafd-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="1cafd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cafd-110">PARAMETERS</span></span>

### <span data-ttu-id="1cafd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cafd-111">-DefaultProfile</span></span>
<span data-ttu-id="1cafd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cafd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cafd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cafd-113">-ResourceGroupName</span></span>
<span data-ttu-id="1cafd-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cafd-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="1cafd-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1cafd-115">-VMScaleSetName</span></span>
<span data-ttu-id="1cafd-116">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="1cafd-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="1cafd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cafd-117">CommonParameters</span></span>
<span data-ttu-id="1cafd-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cafd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cafd-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1cafd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cafd-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cafd-120">INPUTS</span></span>

### <span data-ttu-id="1cafd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1cafd-121">System.String</span></span>

## <span data-ttu-id="1cafd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cafd-122">OUTPUTS</span></span>

### <span data-ttu-id="1cafd-123">Microsoft. Azure. commands. számítási. Automation. models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="1cafd-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="1cafd-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cafd-124">NOTES</span></span>

## <span data-ttu-id="1cafd-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cafd-125">RELATED LINKS</span></span>
