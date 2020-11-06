---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493188"
---
# <span data-ttu-id="d3194-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d3194-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="d3194-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3194-102">SYNOPSIS</span></span>
<span data-ttu-id="d3194-103">Tároló szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d3194-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3194-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3194-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3194-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3194-105">DESCRIPTION</span></span>
<span data-ttu-id="d3194-106">A **Remove-AzureRmContainerService** parancsmag eltávolítja a tároló szolgáltatást az Azure-fiókjából.</span><span class="sxs-lookup"><span data-stu-id="d3194-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="d3194-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3194-107">EXAMPLES</span></span>

### <span data-ttu-id="d3194-108">1. példa: tároló szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d3194-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="d3194-109">Ez a parancs eltávolítja a CSResourceGroup17 nevű tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d3194-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="d3194-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3194-110">PARAMETERS</span></span>

### <span data-ttu-id="d3194-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d3194-111">-Force</span></span>
<span data-ttu-id="d3194-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d3194-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3194-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3194-113">-Name</span></span>
<span data-ttu-id="d3194-114">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d3194-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3194-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3194-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3194-116">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="d3194-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3194-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3194-117">-Confirm</span></span>
<span data-ttu-id="d3194-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3194-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3194-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3194-119">-WhatIf</span></span>
<span data-ttu-id="d3194-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3194-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3194-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3194-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3194-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3194-122">CommonParameters</span></span>
<span data-ttu-id="d3194-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3194-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3194-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3194-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3194-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3194-125">INPUTS</span></span>

### <span data-ttu-id="d3194-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3194-126">None</span></span>
<span data-ttu-id="d3194-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d3194-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3194-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3194-128">OUTPUTS</span></span>

## <span data-ttu-id="d3194-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3194-129">NOTES</span></span>

## <span data-ttu-id="d3194-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3194-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3194-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d3194-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="d3194-132">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d3194-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="d3194-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d3194-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


