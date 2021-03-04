---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: cede1001f475d820dfec7131a8c86815bd98adb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920738"
---
# <span data-ttu-id="af485-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="af485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af485-102">SYNOPSIS</span></span>
<span data-ttu-id="af485-103">Frissíti a tároló beállításjegyzékének webhookját.</span><span class="sxs-lookup"><span data-stu-id="af485-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="af485-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af485-104">SYNTAX</span></span>

### <span data-ttu-id="af485-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af485-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af485-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="af485-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af485-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af485-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af485-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af485-108">DESCRIPTION</span></span>
<span data-ttu-id="af485-109">A Update-AzContainerRegistryWebhook parancsmag frissíti a tároló beállításjegyzékének webhook parancsmagját.</span><span class="sxs-lookup"><span data-stu-id="af485-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="af485-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af485-110">EXAMPLES</span></span>

### <span data-ttu-id="af485-111">1. példa: Egy meglévő tároló beállításjegyzékének frissítése.</span><span class="sxs-lookup"><span data-stu-id="af485-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="af485-112">Frissítsen egy meglévő tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="af485-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="af485-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af485-113">PARAMETERS</span></span>

### <span data-ttu-id="af485-114">-Művelet</span><span class="sxs-lookup"><span data-stu-id="af485-114">-Action</span></span>
<span data-ttu-id="af485-115">Szóközvel elválasztott műveletlista, amely a webhook értesítéseket való bejegyzését váltja ki.</span><span class="sxs-lookup"><span data-stu-id="af485-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af485-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af485-116">-DefaultProfile</span></span>
<span data-ttu-id="af485-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af485-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af485-118">-Header</span><span class="sxs-lookup"><span data-stu-id="af485-118">-Header</span></span>
<span data-ttu-id="af485-119">Szóközök elválasztott egyéni fejlécek "key \[ =value \] ' formátumban, amely hozzáadódik a webhook értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="af485-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="af485-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af485-120">-Name</span></span>
<span data-ttu-id="af485-121">Webhook név.</span><span class="sxs-lookup"><span data-stu-id="af485-121">Webhook Name.</span></span>

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

### <span data-ttu-id="af485-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="af485-122">-RegistryName</span></span>
<span data-ttu-id="af485-123">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="af485-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="af485-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af485-124">-ResourceGroupName</span></span>
<span data-ttu-id="af485-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af485-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="af485-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af485-126">-ResourceId</span></span>
<span data-ttu-id="af485-127">A tároló beállításjegyzékének Webhook erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="af485-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="af485-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="af485-128">-Scope</span></span>
<span data-ttu-id="af485-129">Webhook hatóköre.</span><span class="sxs-lookup"><span data-stu-id="af485-129">Webhook scope.</span></span>

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

### <span data-ttu-id="af485-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="af485-130">-Status</span></span>
<span data-ttu-id="af485-131">Webhook állapot</span><span class="sxs-lookup"><span data-stu-id="af485-131">Webhook status</span></span>

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

### <span data-ttu-id="af485-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="af485-132">-Tag</span></span>
<span data-ttu-id="af485-133">A "key =value" (kulcs =érték) formátumban szóközt \[ \] választva elválasztott címkék.</span><span class="sxs-lookup"><span data-stu-id="af485-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="af485-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="af485-134">-Uri</span></span>
<span data-ttu-id="af485-135">A webhook szolgáltatás URI-ja értesítéseket közzéten.</span><span class="sxs-lookup"><span data-stu-id="af485-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af485-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="af485-136">-Webhook</span></span>
<span data-ttu-id="af485-137">Container Registry Webhook objektum.</span><span class="sxs-lookup"><span data-stu-id="af485-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="af485-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af485-138">-Confirm</span></span>
<span data-ttu-id="af485-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="af485-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af485-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af485-140">-WhatIf</span></span>
<span data-ttu-id="af485-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="af485-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af485-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af485-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af485-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af485-143">CommonParameters</span></span>
<span data-ttu-id="af485-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af485-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af485-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af485-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af485-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af485-146">INPUTS</span></span>

### <span data-ttu-id="af485-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="af485-148">System.String</span><span class="sxs-lookup"><span data-stu-id="af485-148">System.String</span></span>

## <span data-ttu-id="af485-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af485-149">OUTPUTS</span></span>

### <span data-ttu-id="af485-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="af485-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af485-151">NOTES</span></span>

## <span data-ttu-id="af485-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af485-152">RELATED LINKS</span></span>

[<span data-ttu-id="af485-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="af485-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="af485-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="af485-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af485-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)