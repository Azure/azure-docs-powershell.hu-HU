---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493572"
---
# <span data-ttu-id="51f3b-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51f3b-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="51f3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="51f3b-103">Tároló-nyilvántartó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="51f3b-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51f3b-104">SYNTAX</span></span>

### <span data-ttu-id="51f3b-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51f3b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f3b-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51f3b-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f3b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="51f3b-108">A **Remove-AzureRmContainerRegistry** parancsmag eltávolítja a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="51f3b-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="51f3b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="51f3b-110">1. példa: a megadott tároló beállításjegyzékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51f3b-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="51f3b-111">Ez a parancs eltávolítja a megadott tároló-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="51f3b-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="51f3b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51f3b-112">PARAMETERS</span></span>

### <span data-ttu-id="51f3b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51f3b-113">-Name</span></span>
<span data-ttu-id="51f3b-114">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="51f3b-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f3b-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="51f3b-115">-Registry</span></span>
<span data-ttu-id="51f3b-116">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="51f3b-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51f3b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f3b-117">-ResourceGroupName</span></span>
<span data-ttu-id="51f3b-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="51f3b-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f3b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51f3b-119">-Confirm</span></span>
<span data-ttu-id="51f3b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51f3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f3b-121">-WhatIf</span></span>
<span data-ttu-id="51f3b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51f3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f3b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51f3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f3b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f3b-124">-DefaultProfile</span></span>
<span data-ttu-id="51f3b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51f3b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f3b-126">CommonParameters</span></span>
<span data-ttu-id="51f3b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51f3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f3b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f3b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51f3b-129">INPUTS</span></span>

### <span data-ttu-id="51f3b-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51f3b-130">PSContainerRegistry</span></span>
<span data-ttu-id="51f3b-131">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="51f3b-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="51f3b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51f3b-132">OUTPUTS</span></span>

### <span data-ttu-id="51f3b-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="51f3b-133">None</span></span>

## <span data-ttu-id="51f3b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51f3b-134">NOTES</span></span>

## <span data-ttu-id="51f3b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51f3b-135">RELATED LINKS</span></span>

[<span data-ttu-id="51f3b-136">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51f3b-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="51f3b-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51f3b-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="51f3b-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="51f3b-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

