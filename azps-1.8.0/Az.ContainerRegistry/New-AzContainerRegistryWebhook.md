---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 061b712f0c9e2d77d4dab70a0e39051d5f92d7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836577"
---
# <span data-ttu-id="63edf-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="63edf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63edf-102">SYNOPSIS</span></span>
<span data-ttu-id="63edf-103">Létrehoz egy tároló-nyilvántartó webhorogot.</span><span class="sxs-lookup"><span data-stu-id="63edf-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="63edf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63edf-104">SYNTAX</span></span>

### <span data-ttu-id="63edf-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63edf-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63edf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63edf-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63edf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63edf-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63edf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="63edf-108">DESCRIPTION</span></span>
<span data-ttu-id="63edf-109">Az New-AzContainerRegistryWebhook parancsmag létrehoz egy tárolót, melyet a webhook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63edf-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="63edf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="63edf-110">EXAMPLES</span></span>

### <span data-ttu-id="63edf-111">Példa 1: tároló-nyilvántartó webakasztó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="63edf-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="63edf-112">Hozzon létre egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="63edf-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="63edf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63edf-113">PARAMETERS</span></span>

### <span data-ttu-id="63edf-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="63edf-114">-Action</span></span>
<span data-ttu-id="63edf-115">A webkampót elindító műveletek elvégzése az értesítések elküldésével</span><span class="sxs-lookup"><span data-stu-id="63edf-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63edf-116">-DefaultProfile</span></span>
<span data-ttu-id="63edf-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63edf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63edf-118">-Header</span><span class="sxs-lookup"><span data-stu-id="63edf-118">-Header</span></span>
<span data-ttu-id="63edf-119">Egyéni fejlécek, amelyeket felvesz a webhook-értesítésekre.</span><span class="sxs-lookup"><span data-stu-id="63edf-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="63edf-120">-Location</span></span>
<span data-ttu-id="63edf-121">Webhook-hely</span><span class="sxs-lookup"><span data-stu-id="63edf-121">Webhook Location.</span></span>
<span data-ttu-id="63edf-122">A beállításjegyzék alapértelmezett helye.</span><span class="sxs-lookup"><span data-stu-id="63edf-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63edf-123">-Name</span></span>
<span data-ttu-id="63edf-124">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="63edf-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="63edf-125">-Registry</span></span>
<span data-ttu-id="63edf-126">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="63edf-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="63edf-127">-RegistryName</span></span>
<span data-ttu-id="63edf-128">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="63edf-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="63edf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63edf-129">-ResourceGroupName</span></span>
<span data-ttu-id="63edf-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="63edf-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="63edf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63edf-131">-ResourceId</span></span>
<span data-ttu-id="63edf-132">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="63edf-132">The container registry resource id</span></span>

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

### <span data-ttu-id="63edf-133">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="63edf-133">-Scope</span></span>
<span data-ttu-id="63edf-134">Webhook-hatókör</span><span class="sxs-lookup"><span data-stu-id="63edf-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="63edf-135">-Status</span></span>
<span data-ttu-id="63edf-136">Webhook-állapot, alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="63edf-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="63edf-137">-Tag</span></span>
<span data-ttu-id="63edf-138">Webhook-címkék.</span><span class="sxs-lookup"><span data-stu-id="63edf-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-139">-URI</span><span class="sxs-lookup"><span data-stu-id="63edf-139">-Uri</span></span>
<span data-ttu-id="63edf-140">A webhook szolgáltatás URI-ja értesítéseket küldhet.</span><span class="sxs-lookup"><span data-stu-id="63edf-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63edf-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63edf-141">-Confirm</span></span>
<span data-ttu-id="63edf-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63edf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63edf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63edf-143">-WhatIf</span></span>
<span data-ttu-id="63edf-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63edf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63edf-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63edf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63edf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63edf-146">CommonParameters</span></span>
<span data-ttu-id="63edf-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63edf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63edf-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63edf-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63edf-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63edf-149">INPUTS</span></span>

### <span data-ttu-id="63edf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="63edf-150">System.String</span></span>

## <span data-ttu-id="63edf-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63edf-151">OUTPUTS</span></span>

### <span data-ttu-id="63edf-152">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="63edf-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63edf-153">NOTES</span></span>

## <span data-ttu-id="63edf-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63edf-154">RELATED LINKS</span></span>

[<span data-ttu-id="63edf-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="63edf-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="63edf-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="63edf-158">Teszt-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="63edf-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)