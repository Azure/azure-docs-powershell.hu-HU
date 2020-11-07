---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: b7f10fd96d8f746db1ff37b1461cdd8394bdf75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679864"
---
# <span data-ttu-id="74489-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="74489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74489-102">SYNOPSIS</span></span>
<span data-ttu-id="74489-103">Frissít egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="74489-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74489-104">SYNTAX</span></span>

### <span data-ttu-id="74489-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74489-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74489-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="74489-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74489-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74489-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74489-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="74489-108">DESCRIPTION</span></span>
<span data-ttu-id="74489-109">Az Update-AzureRmContainerRegistryWebhook parancsmag a tároló beállításjegyzékének webkampóját frissíti.</span><span class="sxs-lookup"><span data-stu-id="74489-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="74489-110">Példák</span><span class="sxs-lookup"><span data-stu-id="74489-110">EXAMPLES</span></span>

### <span data-ttu-id="74489-111">1. példa: a meglévő tároló beállításjegyzék-webakasztójának frissítése.</span><span class="sxs-lookup"><span data-stu-id="74489-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="74489-112">Frissítsen egy meglévő tároló rendszerleíró webhelyről.</span><span class="sxs-lookup"><span data-stu-id="74489-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="74489-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74489-113">PARAMETERS</span></span>

### <span data-ttu-id="74489-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="74489-114">-Action</span></span>
<span data-ttu-id="74489-115">A webkampót elindító műveletek elvégzése az értesítések elküldésével</span><span class="sxs-lookup"><span data-stu-id="74489-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="74489-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74489-116">-DefaultProfile</span></span>
<span data-ttu-id="74489-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74489-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74489-118">-Header</span><span class="sxs-lookup"><span data-stu-id="74489-118">-Header</span></span>
<span data-ttu-id="74489-119">Szóközzel elválasztott egyéni fejlécek a ' Key \[ = Value \] ' formátumban, amelyet a webhook-értesítésekhez fog hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="74489-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="74489-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74489-120">-Name</span></span>
<span data-ttu-id="74489-121">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="74489-121">Webhook Name.</span></span>

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

### <span data-ttu-id="74489-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="74489-122">-RegistryName</span></span>
<span data-ttu-id="74489-123">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="74489-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="74489-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74489-124">-ResourceGroupName</span></span>
<span data-ttu-id="74489-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="74489-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="74489-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74489-126">-ResourceId</span></span>
<span data-ttu-id="74489-127">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="74489-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="74489-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="74489-128">-Scope</span></span>
<span data-ttu-id="74489-129">Webhook-hatókör</span><span class="sxs-lookup"><span data-stu-id="74489-129">Webhook scope.</span></span>

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

### <span data-ttu-id="74489-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="74489-130">-Status</span></span>
<span data-ttu-id="74489-131">Webhook-állapot</span><span class="sxs-lookup"><span data-stu-id="74489-131">Webhook status</span></span>

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

### <span data-ttu-id="74489-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="74489-132">-Tag</span></span>
<span data-ttu-id="74489-133">Szóközzel tagolt címkék a "kulcs \[ = érték \] " formátumban.</span><span class="sxs-lookup"><span data-stu-id="74489-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="74489-134">-URI</span><span class="sxs-lookup"><span data-stu-id="74489-134">-Uri</span></span>
<span data-ttu-id="74489-135">A webhook szolgáltatás URI-ja értesítéseket küldhet.</span><span class="sxs-lookup"><span data-stu-id="74489-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="74489-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="74489-136">-Webhook</span></span>
<span data-ttu-id="74489-137">Tároló rendszerleíró webhook-objektum.</span><span class="sxs-lookup"><span data-stu-id="74489-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="74489-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74489-138">-Confirm</span></span>
<span data-ttu-id="74489-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74489-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74489-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74489-140">-WhatIf</span></span>
<span data-ttu-id="74489-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74489-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74489-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74489-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74489-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74489-143">CommonParameters</span></span>
<span data-ttu-id="74489-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74489-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74489-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74489-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74489-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74489-146">INPUTS</span></span>

### <span data-ttu-id="74489-147">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="74489-148">Paraméterek: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74489-148">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="74489-149">System. String</span><span class="sxs-lookup"><span data-stu-id="74489-149">System.String</span></span>

## <span data-ttu-id="74489-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74489-150">OUTPUTS</span></span>

### <span data-ttu-id="74489-151">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="74489-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74489-152">NOTES</span></span>

## <span data-ttu-id="74489-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74489-153">RELATED LINKS</span></span>

[<span data-ttu-id="74489-154">Új – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-154">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="74489-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="74489-156">Teszt-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-156">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="74489-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="74489-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
