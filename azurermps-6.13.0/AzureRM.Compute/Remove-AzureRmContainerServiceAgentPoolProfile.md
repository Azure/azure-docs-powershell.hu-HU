---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b960f89ddacb365ee7c1b909b6f0a12bf7c038e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494115"
---
# <span data-ttu-id="32193-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="32193-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="32193-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32193-102">SYNOPSIS</span></span>
<span data-ttu-id="32193-103">Egy ügynök-gyűjtő profil eltávolítása a tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="32193-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32193-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32193-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32193-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32193-105">DESCRIPTION</span></span>
<span data-ttu-id="32193-106">A **Remove-AzureRmContainerServiceAgentPoolProfile** parancsmag egy Agent Pool-profilt távolít el egy tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="32193-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="32193-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32193-107">EXAMPLES</span></span>

### <span data-ttu-id="32193-108">1. példa: profil eltávolítása tároló szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="32193-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="32193-109">Az első parancs a CSResourceGroup17 nevű tároló szolgáltatást a Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32193-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="32193-110">A parancs a $Container változóban tárolja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="32193-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="32193-111">A második parancs eltávolítja a AgentPool01 nevű profilt a $Container tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="32193-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="32193-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32193-112">PARAMETERS</span></span>

### <span data-ttu-id="32193-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="32193-113">-ContainerService</span></span>
<span data-ttu-id="32193-114">Annak a tároló-szolgáltató objektumnak a meghatározása, amelyből a parancsmag eltávolítja az ügynök-készlet profilját.</span><span class="sxs-lookup"><span data-stu-id="32193-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="32193-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32193-115">-DefaultProfile</span></span>
<span data-ttu-id="32193-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32193-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32193-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32193-117">-Name</span></span>
<span data-ttu-id="32193-118">A parancsmag által eltávolított Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32193-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="32193-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32193-119">-Confirm</span></span>
<span data-ttu-id="32193-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32193-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32193-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32193-121">-WhatIf</span></span>
<span data-ttu-id="32193-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32193-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32193-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32193-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32193-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32193-124">CommonParameters</span></span>
<span data-ttu-id="32193-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32193-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32193-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32193-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32193-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32193-127">INPUTS</span></span>

### <span data-ttu-id="32193-128">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="32193-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="32193-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32193-129">System.String</span></span>

## <span data-ttu-id="32193-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32193-130">OUTPUTS</span></span>

### <span data-ttu-id="32193-131">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="32193-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="32193-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32193-132">NOTES</span></span>

## <span data-ttu-id="32193-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32193-133">RELATED LINKS</span></span>

[<span data-ttu-id="32193-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="32193-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="32193-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="32193-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


