---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672740"
---
# <span data-ttu-id="f7e55-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f7e55-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="f7e55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7e55-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e55-103">Eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="f7e55-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7e55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7e55-104">SYNTAX</span></span>

### <span data-ttu-id="f7e55-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7e55-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7e55-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7e55-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e55-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7e55-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7e55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7e55-108">DESCRIPTION</span></span>
<span data-ttu-id="f7e55-109">A Remove-AzureRmContainerRegistryReplication parancsmag eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="f7e55-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="f7e55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f7e55-110">EXAMPLES</span></span>

### <span data-ttu-id="f7e55-111">1. példa: eltávolítja a tároló beállításjegyzékbeli replikálását.</span><span class="sxs-lookup"><span data-stu-id="f7e55-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="f7e55-112">Eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="f7e55-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="f7e55-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7e55-113">PARAMETERS</span></span>

### <span data-ttu-id="f7e55-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7e55-114">-Confirm</span></span>
<span data-ttu-id="f7e55-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7e55-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e55-116">-DefaultProfile</span></span>
<span data-ttu-id="f7e55-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7e55-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7e55-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7e55-118">-Name</span></span>
<span data-ttu-id="f7e55-119">A tároló beállításjegyzék-replikációs neve.</span><span class="sxs-lookup"><span data-stu-id="f7e55-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="f7e55-120">A hely neve alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="f7e55-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f7e55-121">-RegistryName</span></span>
<span data-ttu-id="f7e55-122">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="f7e55-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="f7e55-123">-Replicatoin</span></span>
<span data-ttu-id="f7e55-124">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="f7e55-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="f7e55-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f7e55-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e55-127">-ResourceId</span></span>
<span data-ttu-id="f7e55-128">A tároló beállításjegyzék-replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7e55-128">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e55-129">-WhatIf</span></span>
<span data-ttu-id="f7e55-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7e55-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e55-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7e55-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e55-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7e55-132">-PassThru</span></span>
<span data-ttu-id="f7e55-133">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f7e55-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e55-134">CommonParameters</span></span>
<span data-ttu-id="f7e55-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7e55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e55-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7e55-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e55-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7e55-137">INPUTS</span></span>

### <span data-ttu-id="f7e55-138">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f7e55-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="f7e55-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f7e55-139">System.String</span></span>

## <span data-ttu-id="f7e55-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7e55-140">OUTPUTS</span></span>

### <span data-ttu-id="f7e55-141">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="f7e55-141">System.Object</span></span>

## <span data-ttu-id="f7e55-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7e55-142">NOTES</span></span>

## <span data-ttu-id="f7e55-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7e55-143">RELATED LINKS</span></span>

[<span data-ttu-id="f7e55-144">Új – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f7e55-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="f7e55-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f7e55-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

