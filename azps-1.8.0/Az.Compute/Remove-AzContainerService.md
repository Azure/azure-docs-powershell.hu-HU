---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: e41817c76cbc35564f5eec408de8acecac0466c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671292"
---
# <span data-ttu-id="40b57-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40b57-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="40b57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40b57-102">SYNOPSIS</span></span>
<span data-ttu-id="40b57-103">Tároló szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="40b57-103">Removes a container service.</span></span>

## <span data-ttu-id="40b57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40b57-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40b57-105">DESCRIPTION</span></span>
<span data-ttu-id="40b57-106">A **Remove-AzContainerService** parancsmag eltávolítja a tároló szolgáltatást az Azure-fiókjából.</span><span class="sxs-lookup"><span data-stu-id="40b57-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="40b57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40b57-107">EXAMPLES</span></span>

### <span data-ttu-id="40b57-108">1. példa: tároló szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="40b57-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="40b57-109">Ez a parancs eltávolítja a CSResourceGroup17 nevű tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="40b57-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="40b57-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40b57-110">PARAMETERS</span></span>

### <span data-ttu-id="40b57-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40b57-111">-AsJob</span></span>
<span data-ttu-id="40b57-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="40b57-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="40b57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b57-113">-DefaultProfile</span></span>
<span data-ttu-id="40b57-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40b57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b57-115">-Force</span><span class="sxs-lookup"><span data-stu-id="40b57-115">-Force</span></span>
<span data-ttu-id="40b57-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="40b57-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40b57-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40b57-117">-Name</span></span>
<span data-ttu-id="40b57-118">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="40b57-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b57-119">-ResourceGroupName</span></span>
<span data-ttu-id="40b57-120">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="40b57-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40b57-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40b57-121">-Confirm</span></span>
<span data-ttu-id="40b57-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40b57-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b57-123">-WhatIf</span></span>
<span data-ttu-id="40b57-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40b57-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40b57-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40b57-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b57-126">CommonParameters</span></span>
<span data-ttu-id="40b57-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40b57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b57-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b57-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b57-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40b57-129">INPUTS</span></span>

### <span data-ttu-id="40b57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40b57-130">System.String</span></span>

## <span data-ttu-id="40b57-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40b57-131">OUTPUTS</span></span>

### <span data-ttu-id="40b57-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="40b57-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="40b57-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40b57-133">NOTES</span></span>

## <span data-ttu-id="40b57-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40b57-134">RELATED LINKS</span></span>

[<span data-ttu-id="40b57-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40b57-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="40b57-136">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40b57-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="40b57-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="40b57-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


