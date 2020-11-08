---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183388"
---
# <span data-ttu-id="f01b6-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="f01b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f01b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f01b6-103">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="f01b6-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="f01b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f01b6-104">SYNTAX</span></span>

### <span data-ttu-id="f01b6-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f01b6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f01b6-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f01b6-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f01b6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f01b6-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f01b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f01b6-108">DESCRIPTION</span></span>
<span data-ttu-id="f01b6-109">A Remove-AzContainerRegistryWebhook parancsmag eltávolítja a tároló-nyilvántartó webhookot.</span><span class="sxs-lookup"><span data-stu-id="f01b6-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="f01b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f01b6-110">EXAMPLES</span></span>

### <span data-ttu-id="f01b6-111">1. példa: a Container-nyilvántartó webhook eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f01b6-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="f01b6-112">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="f01b6-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="f01b6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f01b6-113">PARAMETERS</span></span>

### <span data-ttu-id="f01b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01b6-114">-DefaultProfile</span></span>
<span data-ttu-id="f01b6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f01b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f01b6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f01b6-116">-Name</span></span>
<span data-ttu-id="f01b6-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="f01b6-117">Webhook Name.</span></span>

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

### <span data-ttu-id="f01b6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f01b6-118">-PassThru</span></span>
<span data-ttu-id="f01b6-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f01b6-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="f01b6-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f01b6-120">-RegistryName</span></span>
<span data-ttu-id="f01b6-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="f01b6-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="f01b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f01b6-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f01b6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f01b6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f01b6-124">-ResourceId</span></span>
<span data-ttu-id="f01b6-125">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="f01b6-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="f01b6-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-126">-Webhook</span></span>
<span data-ttu-id="f01b6-127">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="f01b6-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="f01b6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f01b6-128">-Confirm</span></span>
<span data-ttu-id="f01b6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f01b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f01b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f01b6-130">-WhatIf</span></span>
<span data-ttu-id="f01b6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f01b6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f01b6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f01b6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f01b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01b6-133">CommonParameters</span></span>
<span data-ttu-id="f01b6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f01b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01b6-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f01b6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01b6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f01b6-136">INPUTS</span></span>

### <span data-ttu-id="f01b6-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="f01b6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f01b6-138">System.String</span></span>

## <span data-ttu-id="f01b6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f01b6-139">OUTPUTS</span></span>

### <span data-ttu-id="f01b6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f01b6-140">System.Boolean</span></span>

## <span data-ttu-id="f01b6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f01b6-141">NOTES</span></span>

## <span data-ttu-id="f01b6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f01b6-142">RELATED LINKS</span></span>

[<span data-ttu-id="f01b6-143">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f01b6-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f01b6-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f01b6-146">Teszt-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f01b6-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)