---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025524"
---
# <span data-ttu-id="8a0b9-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8a0b9-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="8a0b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0b9-103">Tároló szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-103">Removes a container service.</span></span>

## <span data-ttu-id="8a0b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a0b9-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a0b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0b9-106">A **Remove-AzContainerService** parancsmag eltávolítja a tároló szolgáltatást az Azure-fiókjából.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="8a0b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8a0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="8a0b9-108">1. példa: tároló szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8a0b9-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="8a0b9-109">Ez a parancs eltávolítja a CSResourceGroup17 nevű tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="8a0b9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a0b9-110">PARAMETERS</span></span>

### <span data-ttu-id="8a0b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a0b9-111">-AsJob</span></span>
<span data-ttu-id="8a0b9-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8a0b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0b9-113">-DefaultProfile</span></span>
<span data-ttu-id="8a0b9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a0b9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a0b9-115">-Force</span></span>
<span data-ttu-id="8a0b9-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a0b9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a0b9-117">-Name</span></span>
<span data-ttu-id="8a0b9-118">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a0b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a0b9-120">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a0b9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a0b9-121">-Confirm</span></span>
<span data-ttu-id="8a0b9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a0b9-123">-WhatIf</span></span>
<span data-ttu-id="8a0b9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a0b9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0b9-126">CommonParameters</span></span>
<span data-ttu-id="8a0b9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a0b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0b9-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a0b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0b9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a0b9-129">INPUTS</span></span>

### <span data-ttu-id="8a0b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8a0b9-130">System.String</span></span>

## <span data-ttu-id="8a0b9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a0b9-131">OUTPUTS</span></span>

### <span data-ttu-id="8a0b9-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8a0b9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8a0b9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a0b9-133">NOTES</span></span>

## <span data-ttu-id="8a0b9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a0b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="8a0b9-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8a0b9-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="8a0b9-136">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8a0b9-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="8a0b9-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8a0b9-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


