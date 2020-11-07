---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850089"
---
# <span data-ttu-id="56d20-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="56d20-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="56d20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56d20-102">SYNOPSIS</span></span>
<span data-ttu-id="56d20-103">Egy ügynök-gyűjtő profil eltávolítása a tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="56d20-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56d20-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56d20-105">DESCRIPTION</span></span>
<span data-ttu-id="56d20-106">A **Remove-AzureRmContainerServiceAgentPoolProfile** parancsmag egy Agent Pool-profilt távolít el egy tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="56d20-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="56d20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56d20-107">EXAMPLES</span></span>

### <span data-ttu-id="56d20-108">1. példa: profil eltávolítása tároló szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="56d20-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="56d20-109">Az első parancs a CSResourceGroup17 nevű tároló szolgáltatást a Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="56d20-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="56d20-110">A parancs a $Container változóban tárolja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="56d20-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="56d20-111">A második parancs eltávolítja a AgentPool01 nevű profilt a $Container tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="56d20-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="56d20-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56d20-112">PARAMETERS</span></span>

### <span data-ttu-id="56d20-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="56d20-113">-ContainerService</span></span>
<span data-ttu-id="56d20-114">Annak a tároló-szolgáltató objektumnak a meghatározása, amelyből a parancsmag eltávolítja az ügynök-készlet profilját.</span><span class="sxs-lookup"><span data-stu-id="56d20-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56d20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d20-115">-DefaultProfile</span></span>
<span data-ttu-id="56d20-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56d20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d20-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56d20-117">-Name</span></span>
<span data-ttu-id="56d20-118">A parancsmag által eltávolított Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56d20-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56d20-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56d20-119">-Confirm</span></span>
<span data-ttu-id="56d20-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56d20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d20-121">-WhatIf</span></span>
<span data-ttu-id="56d20-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56d20-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56d20-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56d20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d20-124">CommonParameters</span></span>
<span data-ttu-id="56d20-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56d20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d20-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d20-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56d20-127">INPUTS</span></span>

### <span data-ttu-id="56d20-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="56d20-128">ContainerService</span></span>
<span data-ttu-id="56d20-129">A ' ContainerService ' paraméter az "ContainerService" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="56d20-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="56d20-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56d20-130">OUTPUTS</span></span>

### <span data-ttu-id="56d20-131">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="56d20-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="56d20-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56d20-132">NOTES</span></span>

## <span data-ttu-id="56d20-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56d20-133">RELATED LINKS</span></span>

[<span data-ttu-id="56d20-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="56d20-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="56d20-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="56d20-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


