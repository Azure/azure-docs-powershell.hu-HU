---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 03073d24ac492741385aa4b879b2a00981b5921e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667115"
---
# <span data-ttu-id="fb7b8-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fb7b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7b8-103">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fb7b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb7b8-104">SYNTAX</span></span>

### <span data-ttu-id="fb7b8-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb7b8-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7b8-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7b8-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7b8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7b8-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="fb7b8-109">A Remove-AzContainerRegistryWebhook parancsmag eltávolítja a tároló-nyilvántartó webhookot.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="fb7b8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb7b8-110">EXAMPLES</span></span>

### <span data-ttu-id="fb7b8-111">1. példa: a Container-nyilvántartó webhook eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="fb7b8-112">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fb7b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb7b8-113">PARAMETERS</span></span>

### <span data-ttu-id="fb7b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7b8-114">-DefaultProfile</span></span>
<span data-ttu-id="fb7b8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7b8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb7b8-116">-Name</span></span>
<span data-ttu-id="fb7b8-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7b8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb7b8-118">-PassThru</span></span>
<span data-ttu-id="fb7b8-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fb7b8-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fb7b8-120">-RegistryName</span></span>
<span data-ttu-id="fb7b8-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb7b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb7b8-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb7b8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7b8-124">-ResourceId</span></span>
<span data-ttu-id="fb7b8-125">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="fb7b8-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fb7b8-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-126">-Webhook</span></span>
<span data-ttu-id="fb7b8-127">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7b8-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb7b8-128">-Confirm</span></span>
<span data-ttu-id="fb7b8-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7b8-130">-WhatIf</span></span>
<span data-ttu-id="fb7b8-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7b8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7b8-133">CommonParameters</span></span>
<span data-ttu-id="fb7b8-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb7b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7b8-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb7b8-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7b8-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb7b8-136">INPUTS</span></span>

### <span data-ttu-id="fb7b8-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="fb7b8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fb7b8-138">System.String</span></span>

## <span data-ttu-id="fb7b8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb7b8-139">OUTPUTS</span></span>

### <span data-ttu-id="fb7b8-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb7b8-140">System.Boolean</span></span>

## <span data-ttu-id="fb7b8-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb7b8-141">NOTES</span></span>

## <span data-ttu-id="fb7b8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb7b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="fb7b8-143">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fb7b8-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fb7b8-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fb7b8-146">Teszt-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb7b8-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)