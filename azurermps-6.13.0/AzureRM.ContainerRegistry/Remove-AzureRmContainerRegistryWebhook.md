---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679865"
---
# <span data-ttu-id="a66cf-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="a66cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a66cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a66cf-103">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="a66cf-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a66cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a66cf-104">SYNTAX</span></span>

### <span data-ttu-id="a66cf-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a66cf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a66cf-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a66cf-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a66cf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a66cf-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66cf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a66cf-108">DESCRIPTION</span></span>
<span data-ttu-id="a66cf-109">A Remove-AzureRmContainerRegistryWebhook parancsmag eltávolítja a tároló-nyilvántartó webhookot.</span><span class="sxs-lookup"><span data-stu-id="a66cf-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="a66cf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a66cf-110">EXAMPLES</span></span>

### <span data-ttu-id="a66cf-111">1. példa: a Container-nyilvántartó webhook eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a66cf-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="a66cf-112">Eltávolítja a tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="a66cf-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="a66cf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a66cf-113">PARAMETERS</span></span>

### <span data-ttu-id="a66cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66cf-114">-DefaultProfile</span></span>
<span data-ttu-id="a66cf-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a66cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a66cf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a66cf-116">-Name</span></span>
<span data-ttu-id="a66cf-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="a66cf-117">Webhook Name.</span></span>

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

### <span data-ttu-id="a66cf-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a66cf-118">-PassThru</span></span>
<span data-ttu-id="a66cf-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad eredményül, ha az Eltávolítás sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="a66cf-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="a66cf-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a66cf-120">-RegistryName</span></span>
<span data-ttu-id="a66cf-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="a66cf-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="a66cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="a66cf-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a66cf-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="a66cf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a66cf-124">-ResourceId</span></span>
<span data-ttu-id="a66cf-125">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a66cf-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a66cf-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-126">-Webhook</span></span>
<span data-ttu-id="a66cf-127">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="a66cf-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="a66cf-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a66cf-128">-Confirm</span></span>
<span data-ttu-id="a66cf-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a66cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66cf-130">-WhatIf</span></span>
<span data-ttu-id="a66cf-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a66cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a66cf-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a66cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66cf-133">CommonParameters</span></span>
<span data-ttu-id="a66cf-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a66cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66cf-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66cf-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a66cf-136">INPUTS</span></span>

### <span data-ttu-id="a66cf-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="a66cf-138">Paraméterek: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a66cf-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="a66cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a66cf-139">System.String</span></span>

## <span data-ttu-id="a66cf-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a66cf-140">OUTPUTS</span></span>

### <span data-ttu-id="a66cf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a66cf-141">System.Boolean</span></span>

## <span data-ttu-id="a66cf-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a66cf-142">NOTES</span></span>

## <span data-ttu-id="a66cf-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a66cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="a66cf-144">Új – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a66cf-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a66cf-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a66cf-147">Teszt-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a66cf-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
