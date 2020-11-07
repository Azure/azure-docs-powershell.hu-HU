---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef9d1ac2e5bca51ee1addf8fdffd87c5045d23eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680184"
---
# <span data-ttu-id="df2f7-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="df2f7-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="df2f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="df2f7-103">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="df2f7-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df2f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df2f7-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df2f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="df2f7-106">A virtuálisgép-készlet legújabb, folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="df2f7-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="df2f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="df2f7-107">EXAMPLES</span></span>

### <span data-ttu-id="df2f7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df2f7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="df2f7-109">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS legújabb folyamatos frissítésének állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="df2f7-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="df2f7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df2f7-110">PARAMETERS</span></span>

### <span data-ttu-id="df2f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2f7-111">-DefaultProfile</span></span>
<span data-ttu-id="df2f7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df2f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df2f7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df2f7-113">-ResourceGroupName</span></span>
<span data-ttu-id="df2f7-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df2f7-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="df2f7-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="df2f7-115">-VMScaleSetName</span></span>
<span data-ttu-id="df2f7-116">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="df2f7-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="df2f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2f7-117">CommonParameters</span></span>
<span data-ttu-id="df2f7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df2f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2f7-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2f7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2f7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df2f7-120">INPUTS</span></span>

### <span data-ttu-id="df2f7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="df2f7-121">System.String</span></span>

## <span data-ttu-id="df2f7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df2f7-122">OUTPUTS</span></span>

### <span data-ttu-id="df2f7-123">Microsoft. Azure. commands. számítási. Automation. models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="df2f7-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="df2f7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df2f7-124">NOTES</span></span>

## <span data-ttu-id="df2f7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df2f7-125">RELATED LINKS</span></span>
