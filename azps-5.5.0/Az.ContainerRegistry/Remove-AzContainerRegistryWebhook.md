---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164122"
---
# <span data-ttu-id="878a0-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="878a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="878a0-102">SYNOPSIS</span></span>
<span data-ttu-id="878a0-103">Eltávolít egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="878a0-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="878a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="878a0-104">SYNTAX</span></span>

### <span data-ttu-id="878a0-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="878a0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="878a0-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="878a0-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="878a0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="878a0-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="878a0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="878a0-108">DESCRIPTION</span></span>
<span data-ttu-id="878a0-109">A Remove-AzContainerRegistryWebhook parancsmag eltávolítja a tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="878a0-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="878a0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="878a0-110">EXAMPLES</span></span>

### <span data-ttu-id="878a0-111">1. példa: Egy tárolóadatbázis-webhook eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="878a0-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="878a0-112">Eltávolít egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="878a0-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="878a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="878a0-113">PARAMETERS</span></span>

### <span data-ttu-id="878a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878a0-114">-DefaultProfile</span></span>
<span data-ttu-id="878a0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="878a0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="878a0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="878a0-116">-Name</span></span>
<span data-ttu-id="878a0-117">Webhook név.</span><span class="sxs-lookup"><span data-stu-id="878a0-117">Webhook Name.</span></span>

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

### <span data-ttu-id="878a0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="878a0-118">-PassThru</span></span>
<span data-ttu-id="878a0-119">Azt jelzi, hogy ez a parancsmag igaz értéket ad vissza, ha az eltávolítás sikerült.</span><span class="sxs-lookup"><span data-stu-id="878a0-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="878a0-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="878a0-120">-RegistryName</span></span>
<span data-ttu-id="878a0-121">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="878a0-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="878a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="878a0-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="878a0-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="878a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="878a0-124">-ResourceId</span></span>
<span data-ttu-id="878a0-125">A tároló beállításjegyzékének Webhook erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="878a0-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="878a0-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="878a0-126">-Webhook</span></span>
<span data-ttu-id="878a0-127">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="878a0-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="878a0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="878a0-128">-Confirm</span></span>
<span data-ttu-id="878a0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="878a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="878a0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="878a0-130">-WhatIf</span></span>
<span data-ttu-id="878a0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="878a0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="878a0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="878a0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="878a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878a0-133">CommonParameters</span></span>
<span data-ttu-id="878a0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878a0-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="878a0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878a0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="878a0-136">INPUTS</span></span>

### <span data-ttu-id="878a0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="878a0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="878a0-138">System.String</span></span>

## <span data-ttu-id="878a0-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="878a0-139">OUTPUTS</span></span>

### <span data-ttu-id="878a0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="878a0-140">System.Boolean</span></span>

## <span data-ttu-id="878a0-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="878a0-141">NOTES</span></span>

## <span data-ttu-id="878a0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="878a0-142">RELATED LINKS</span></span>

[<span data-ttu-id="878a0-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="878a0-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="878a0-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="878a0-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="878a0-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)