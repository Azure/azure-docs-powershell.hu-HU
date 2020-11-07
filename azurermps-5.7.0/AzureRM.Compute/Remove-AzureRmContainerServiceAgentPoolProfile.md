---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672165"
---
# <span data-ttu-id="39714-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="39714-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="39714-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39714-102">SYNOPSIS</span></span>
<span data-ttu-id="39714-103">Egy ügynök-gyűjtő profil eltávolítása a tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="39714-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39714-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39714-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39714-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39714-105">DESCRIPTION</span></span>
<span data-ttu-id="39714-106">A **Remove-AzureRmContainerServiceAgentPoolProfile** parancsmag egy Agent Pool-profilt távolít el egy tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="39714-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="39714-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39714-107">EXAMPLES</span></span>

### <span data-ttu-id="39714-108">1. példa: profil eltávolítása tároló szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="39714-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="39714-109">Az első parancs a CSResourceGroup17 nevű tároló szolgáltatást a Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39714-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="39714-110">A parancs a $Container változóban tárolja a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="39714-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="39714-111">A második parancs eltávolítja a AgentPool01 nevű profilt a $Container tároló szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="39714-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="39714-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39714-112">PARAMETERS</span></span>

### <span data-ttu-id="39714-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="39714-113">-ContainerService</span></span>
<span data-ttu-id="39714-114">Annak a tároló-szolgáltató objektumnak a meghatározása, amelyből a parancsmag eltávolítja az ügynök-készlet profilját.</span><span class="sxs-lookup"><span data-stu-id="39714-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39714-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39714-115">-Name</span></span>
<span data-ttu-id="39714-116">A parancsmag által eltávolított Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39714-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="39714-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39714-117">-Confirm</span></span>
<span data-ttu-id="39714-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39714-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39714-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39714-119">-WhatIf</span></span>
<span data-ttu-id="39714-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39714-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39714-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39714-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39714-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39714-122">CommonParameters</span></span>
<span data-ttu-id="39714-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39714-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39714-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39714-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39714-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39714-125">INPUTS</span></span>

### <span data-ttu-id="39714-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="39714-126">None</span></span>
<span data-ttu-id="39714-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="39714-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39714-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39714-128">OUTPUTS</span></span>

## <span data-ttu-id="39714-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39714-129">NOTES</span></span>

## <span data-ttu-id="39714-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39714-130">RELATED LINKS</span></span>

[<span data-ttu-id="39714-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="39714-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="39714-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="39714-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


