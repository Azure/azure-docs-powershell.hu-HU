---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: f87399901e00e19686d879799dbb799c7d79172c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505139"
---
# <span data-ttu-id="fc28c-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc28c-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="fc28c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc28c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc28c-103">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="fc28c-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc28c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc28c-104">SYNTAX</span></span>

### <span data-ttu-id="fc28c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc28c-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc28c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fc28c-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc28c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc28c-107">DESCRIPTION</span></span>
<span data-ttu-id="fc28c-108">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="fc28c-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="fc28c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fc28c-109">EXAMPLES</span></span>

### <span data-ttu-id="fc28c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc28c-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fc28c-111">Ez a parancs a "VMSS001" erőforráscsoport "Group001" erőforráscsoporthoz való folyamatos folyamatos frissítését lemondja.</span><span class="sxs-lookup"><span data-stu-id="fc28c-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="fc28c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc28c-112">PARAMETERS</span></span>

### <span data-ttu-id="fc28c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc28c-113">-DefaultProfile</span></span>
<span data-ttu-id="fc28c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc28c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc28c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc28c-115">-Force</span></span>
<span data-ttu-id="fc28c-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fc28c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc28c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc28c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc28c-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc28c-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc28c-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fc28c-119">-VMScaleSetName</span></span>
<span data-ttu-id="fc28c-120">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="fc28c-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc28c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc28c-121">-Confirm</span></span>
<span data-ttu-id="fc28c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc28c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc28c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc28c-123">-WhatIf</span></span>
<span data-ttu-id="fc28c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc28c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc28c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc28c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc28c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc28c-126">CommonParameters</span></span>
<span data-ttu-id="fc28c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc28c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc28c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc28c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc28c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc28c-129">INPUTS</span></span>

### <span data-ttu-id="fc28c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc28c-130">System.String</span></span>

## <span data-ttu-id="fc28c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc28c-131">OUTPUTS</span></span>

### <span data-ttu-id="fc28c-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fc28c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fc28c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc28c-133">NOTES</span></span>

## <span data-ttu-id="fc28c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc28c-134">RELATED LINKS</span></span>

