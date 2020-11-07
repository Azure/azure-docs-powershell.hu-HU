---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 717e1ecd7b2242ee5643ca80883e472f5ea4a3c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667117"
---
# <span data-ttu-id="02244-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="02244-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="02244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02244-102">SYNOPSIS</span></span>
<span data-ttu-id="02244-103">Eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="02244-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="02244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02244-104">SYNTAX</span></span>

### <span data-ttu-id="02244-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02244-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02244-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02244-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02244-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02244-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02244-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02244-108">DESCRIPTION</span></span>
<span data-ttu-id="02244-109">A Remove-AzContainerRegistryReplication parancsmag eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="02244-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="02244-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02244-110">EXAMPLES</span></span>

### <span data-ttu-id="02244-111">1. példa: eltávolítja a tároló beállításjegyzékbeli replikálását.</span><span class="sxs-lookup"><span data-stu-id="02244-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="02244-112">Eltávolítja a tároló beállításjegyzékének replikálását.</span><span class="sxs-lookup"><span data-stu-id="02244-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="02244-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02244-113">PARAMETERS</span></span>

### <span data-ttu-id="02244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02244-114">-DefaultProfile</span></span>
<span data-ttu-id="02244-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02244-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02244-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02244-116">-Name</span></span>
<span data-ttu-id="02244-117">A tároló beállításjegyzék-replikációs neve.</span><span class="sxs-lookup"><span data-stu-id="02244-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="02244-118">A hely neve alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="02244-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02244-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02244-119">-PassThru</span></span>
<span data-ttu-id="02244-120">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="02244-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="02244-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="02244-121">-RegistryName</span></span>
<span data-ttu-id="02244-122">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="02244-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02244-123">-Replikáció</span><span class="sxs-lookup"><span data-stu-id="02244-123">-Replication</span></span>
<span data-ttu-id="02244-124">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="02244-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02244-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02244-125">-ResourceGroupName</span></span>
<span data-ttu-id="02244-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="02244-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02244-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02244-127">-ResourceId</span></span>
<span data-ttu-id="02244-128">A tároló beállításjegyzék-replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="02244-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02244-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02244-129">-Confirm</span></span>
<span data-ttu-id="02244-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02244-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02244-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02244-131">-WhatIf</span></span>
<span data-ttu-id="02244-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02244-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02244-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02244-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02244-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02244-134">CommonParameters</span></span>
<span data-ttu-id="02244-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02244-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02244-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="02244-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02244-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02244-137">INPUTS</span></span>

### <span data-ttu-id="02244-138">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="02244-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="02244-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02244-139">System.String</span></span>

## <span data-ttu-id="02244-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02244-140">OUTPUTS</span></span>

### <span data-ttu-id="02244-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02244-141">System.Boolean</span></span>

## <span data-ttu-id="02244-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02244-142">NOTES</span></span>

## <span data-ttu-id="02244-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02244-143">RELATED LINKS</span></span>

[<span data-ttu-id="02244-144">Új – AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="02244-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="02244-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="02244-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

