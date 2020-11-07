---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 4c9281bc7eea4f8bf3b60d458f662ada19d97807
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848537"
---
# <span data-ttu-id="7cdfc-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7cdfc-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="7cdfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cdfc-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdfc-103">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cdfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cdfc-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cdfc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cdfc-105">DESCRIPTION</span></span>
<span data-ttu-id="7cdfc-106">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="7cdfc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cdfc-107">EXAMPLES</span></span>

### <span data-ttu-id="7cdfc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cdfc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7cdfc-109">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS legújabb folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7cdfc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cdfc-110">PARAMETERS</span></span>

### <span data-ttu-id="7cdfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdfc-111">-DefaultProfile</span></span>
<span data-ttu-id="7cdfc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdfc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cdfc-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cdfc-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdfc-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7cdfc-115">-VMScaleSetName</span></span>
<span data-ttu-id="7cdfc-116">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-116">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdfc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdfc-117">CommonParameters</span></span>
<span data-ttu-id="7cdfc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cdfc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdfc-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cdfc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdfc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdfc-120">INPUTS</span></span>

### <span data-ttu-id="7cdfc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7cdfc-121">System.String</span></span>

## <span data-ttu-id="7cdfc-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdfc-122">OUTPUTS</span></span>

### <span data-ttu-id="7cdfc-123">Microsoft. Azure. commands. számítási. Automation. models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="7cdfc-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="7cdfc-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cdfc-124">NOTES</span></span>

## <span data-ttu-id="7cdfc-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cdfc-125">RELATED LINKS</span></span>

