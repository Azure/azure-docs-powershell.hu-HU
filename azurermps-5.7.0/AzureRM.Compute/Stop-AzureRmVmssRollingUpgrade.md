---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 292da4caf90fb43895ec5cda12dcfc6418e6bde9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503819"
---
# <span data-ttu-id="20dd3-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="20dd3-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="20dd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="20dd3-103">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="20dd3-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20dd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20dd3-104">SYNTAX</span></span>

### <span data-ttu-id="20dd3-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20dd3-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dd3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="20dd3-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20dd3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="20dd3-107">DESCRIPTION</span></span>
<span data-ttu-id="20dd3-108">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="20dd3-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="20dd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="20dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="20dd3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20dd3-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="20dd3-111">Ez a parancs a "VMSS001" erőforráscsoport "Group001" erőforráscsoporthoz való folyamatos folyamatos frissítését lemondja.</span><span class="sxs-lookup"><span data-stu-id="20dd3-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="20dd3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20dd3-112">PARAMETERS</span></span>

### <span data-ttu-id="20dd3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20dd3-113">-AsJob</span></span>
<span data-ttu-id="20dd3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="20dd3-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dd3-115">-DefaultProfile</span></span>
<span data-ttu-id="20dd3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20dd3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20dd3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20dd3-117">-Force</span></span>
<span data-ttu-id="20dd3-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="20dd3-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20dd3-119">-ResourceGroupName</span></span>
<span data-ttu-id="20dd3-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="20dd3-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="20dd3-121">-VMScaleSetName</span></span>
<span data-ttu-id="20dd3-122">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="20dd3-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20dd3-123">-Confirm</span></span>
<span data-ttu-id="20dd3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20dd3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20dd3-125">-WhatIf</span></span>
<span data-ttu-id="20dd3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20dd3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20dd3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20dd3-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dd3-128">CommonParameters</span></span>
<span data-ttu-id="20dd3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20dd3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dd3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20dd3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dd3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20dd3-131">INPUTS</span></span>

### <span data-ttu-id="20dd3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="20dd3-132">System.String</span></span>

## <span data-ttu-id="20dd3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20dd3-133">OUTPUTS</span></span>

### <span data-ttu-id="20dd3-134">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="20dd3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="20dd3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20dd3-135">NOTES</span></span>

## <span data-ttu-id="20dd3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20dd3-136">RELATED LINKS</span></span>
