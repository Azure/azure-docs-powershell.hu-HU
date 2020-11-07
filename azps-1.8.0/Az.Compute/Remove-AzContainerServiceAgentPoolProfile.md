---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: dc1884d643bd2f3c58ae6cb68fe272a786bcde73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836736"
---
# <span data-ttu-id="45782-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="45782-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="45782-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45782-102">SYNOPSIS</span></span>
<span data-ttu-id="45782-103">Egy ügynök-gyűjtő profil eltávolítása a tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="45782-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="45782-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45782-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45782-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45782-105">DESCRIPTION</span></span>
<span data-ttu-id="45782-106">A **Remove-AzContainerServiceAgentPoolProfile** parancsmag egy Agent Pool-profilt távolít el egy tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="45782-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="45782-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45782-107">EXAMPLES</span></span>

### <span data-ttu-id="45782-108">1. példa: profil eltávolítása tároló szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="45782-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="45782-109">Az első parancs a CSResourceGroup17 nevű tároló szolgáltatást a Get-AzContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45782-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="45782-110">A parancs a $Container változóban tárolja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="45782-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="45782-111">A második parancs eltávolítja a AgentPool01 nevű profilt a $Container tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="45782-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="45782-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45782-112">PARAMETERS</span></span>

### <span data-ttu-id="45782-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="45782-113">-ContainerService</span></span>
<span data-ttu-id="45782-114">Annak a tároló-szolgáltató objektumnak a meghatározása, amelyből a parancsmag eltávolítja az ügynök-készlet profilját.</span><span class="sxs-lookup"><span data-stu-id="45782-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45782-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45782-115">-DefaultProfile</span></span>
<span data-ttu-id="45782-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45782-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45782-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45782-117">-Name</span></span>
<span data-ttu-id="45782-118">A parancsmag által eltávolított Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45782-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45782-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45782-119">-Confirm</span></span>
<span data-ttu-id="45782-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45782-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45782-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45782-121">-WhatIf</span></span>
<span data-ttu-id="45782-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45782-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45782-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45782-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45782-124">CommonParameters</span></span>
<span data-ttu-id="45782-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45782-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45782-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45782-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45782-127">INPUTS</span></span>

### <span data-ttu-id="45782-128">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="45782-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="45782-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45782-129">System.String</span></span>

## <span data-ttu-id="45782-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45782-130">OUTPUTS</span></span>

### <span data-ttu-id="45782-131">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="45782-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="45782-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45782-132">NOTES</span></span>

## <span data-ttu-id="45782-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45782-133">RELATED LINKS</span></span>

[<span data-ttu-id="45782-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="45782-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="45782-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="45782-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


