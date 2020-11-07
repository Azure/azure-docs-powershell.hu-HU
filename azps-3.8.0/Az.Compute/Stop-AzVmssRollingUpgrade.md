---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846142"
---
# <span data-ttu-id="ef20e-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ef20e-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="ef20e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef20e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef20e-103">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="ef20e-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="ef20e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef20e-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef20e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef20e-105">DESCRIPTION</span></span>
<span data-ttu-id="ef20e-106">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="ef20e-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="ef20e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef20e-107">EXAMPLES</span></span>

### <span data-ttu-id="ef20e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef20e-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ef20e-109">Ez a parancs a "VMSS001" erőforráscsoport "Group001" erőforráscsoporthoz való folyamatos folyamatos frissítését lemondja.</span><span class="sxs-lookup"><span data-stu-id="ef20e-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="ef20e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef20e-110">PARAMETERS</span></span>

### <span data-ttu-id="ef20e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef20e-111">-AsJob</span></span>
<span data-ttu-id="ef20e-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ef20e-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef20e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef20e-113">-DefaultProfile</span></span>
<span data-ttu-id="ef20e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef20e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef20e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef20e-115">-Force</span></span>
<span data-ttu-id="ef20e-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ef20e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef20e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef20e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef20e-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef20e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef20e-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ef20e-119">-VMScaleSetName</span></span>
<span data-ttu-id="ef20e-120">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="ef20e-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="ef20e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef20e-121">-Confirm</span></span>
<span data-ttu-id="ef20e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef20e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef20e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef20e-123">-WhatIf</span></span>
<span data-ttu-id="ef20e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef20e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef20e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef20e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef20e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef20e-126">CommonParameters</span></span>
<span data-ttu-id="ef20e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef20e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef20e-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef20e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef20e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef20e-129">INPUTS</span></span>

### <span data-ttu-id="ef20e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ef20e-130">System.String</span></span>

## <span data-ttu-id="ef20e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef20e-131">OUTPUTS</span></span>

### <span data-ttu-id="ef20e-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ef20e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ef20e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef20e-133">NOTES</span></span>

## <span data-ttu-id="ef20e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef20e-134">RELATED LINKS</span></span>
