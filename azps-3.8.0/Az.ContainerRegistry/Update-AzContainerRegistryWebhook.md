---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845653"
---
# <span data-ttu-id="8d8e1-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="8d8e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8e1-103">Frissít egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="8d8e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d8e1-104">SYNTAX</span></span>

### <span data-ttu-id="8d8e1-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d8e1-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d8e1-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d8e1-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d8e1-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d8e1-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d8e1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d8e1-108">DESCRIPTION</span></span>
<span data-ttu-id="8d8e1-109">Az Update-AzContainerRegistryWebhook parancsmag a tároló beállításjegyzékének webkampóját frissíti.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="8d8e1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8d8e1-110">EXAMPLES</span></span>

### <span data-ttu-id="8d8e1-111">1. példa: a meglévő tároló beállításjegyzék-webakasztójának frissítése.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="8d8e1-112">Frissítsen egy meglévő tároló rendszerleíró webhelyről.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="8d8e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d8e1-113">PARAMETERS</span></span>

### <span data-ttu-id="8d8e1-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="8d8e1-114">-Action</span></span>
<span data-ttu-id="8d8e1-115">A webkampót elindító műveletek elvégzése az értesítések elküldésével</span><span class="sxs-lookup"><span data-stu-id="8d8e1-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="8d8e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8e1-116">-DefaultProfile</span></span>
<span data-ttu-id="8d8e1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d8e1-118">-Header</span><span class="sxs-lookup"><span data-stu-id="8d8e1-118">-Header</span></span>
<span data-ttu-id="8d8e1-119">Szóközzel elválasztott egyéni fejlécek a ' Key \[ = Value \] ' formátumban, amelyet a webhook-értesítésekhez fog hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="8d8e1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d8e1-120">-Name</span></span>
<span data-ttu-id="8d8e1-121">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-121">Webhook Name.</span></span>

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

### <span data-ttu-id="8d8e1-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8d8e1-122">-RegistryName</span></span>
<span data-ttu-id="8d8e1-123">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="8d8e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d8e1-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8d8e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8e1-126">-ResourceId</span></span>
<span data-ttu-id="8d8e1-127">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="8d8e1-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="8d8e1-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8d8e1-128">-Scope</span></span>
<span data-ttu-id="8d8e1-129">Webhook-hatókör</span><span class="sxs-lookup"><span data-stu-id="8d8e1-129">Webhook scope.</span></span>

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

### <span data-ttu-id="8d8e1-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="8d8e1-130">-Status</span></span>
<span data-ttu-id="8d8e1-131">Webhook-állapot</span><span class="sxs-lookup"><span data-stu-id="8d8e1-131">Webhook status</span></span>

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

### <span data-ttu-id="8d8e1-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="8d8e1-132">-Tag</span></span>
<span data-ttu-id="8d8e1-133">Szóközzel tagolt címkék a "kulcs \[ = érték \] " formátumban.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="8d8e1-134">-URI</span><span class="sxs-lookup"><span data-stu-id="8d8e1-134">-Uri</span></span>
<span data-ttu-id="8d8e1-135">A webhook szolgáltatás URI-ja értesítéseket küldhet.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="8d8e1-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-136">-Webhook</span></span>
<span data-ttu-id="8d8e1-137">Tároló rendszerleíró webhook-objektum.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="8d8e1-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d8e1-138">-Confirm</span></span>
<span data-ttu-id="8d8e1-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d8e1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d8e1-140">-WhatIf</span></span>
<span data-ttu-id="8d8e1-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d8e1-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d8e1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8e1-143">CommonParameters</span></span>
<span data-ttu-id="8d8e1-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d8e1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8e1-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8e1-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d8e1-146">INPUTS</span></span>

### <span data-ttu-id="8d8e1-147">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="8d8e1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8e1-148">System.String</span></span>

## <span data-ttu-id="8d8e1-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d8e1-149">OUTPUTS</span></span>

### <span data-ttu-id="8d8e1-150">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="8d8e1-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d8e1-151">NOTES</span></span>

## <span data-ttu-id="8d8e1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d8e1-152">RELATED LINKS</span></span>

[<span data-ttu-id="8d8e1-153">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8d8e1-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8d8e1-155">Teszt-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8d8e1-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8d8e1-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)