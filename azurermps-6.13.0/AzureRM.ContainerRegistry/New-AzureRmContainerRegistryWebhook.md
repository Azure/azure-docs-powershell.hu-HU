---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 6cee5cc10fc9cbb1af014e2ad500b38111fc3564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491968"
---
# <span data-ttu-id="de548-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="de548-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de548-102">SYNOPSIS</span></span>
<span data-ttu-id="de548-103">Létrehoz egy tároló-nyilvántartó webhorogot.</span><span class="sxs-lookup"><span data-stu-id="de548-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de548-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de548-104">SYNTAX</span></span>

### <span data-ttu-id="de548-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de548-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de548-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de548-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de548-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de548-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de548-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="de548-108">DESCRIPTION</span></span>
<span data-ttu-id="de548-109">Az New-AzureRmContainerRegistryWebhook parancsmag létrehoz egy tárolót, melyet a webhook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de548-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="de548-110">Példák</span><span class="sxs-lookup"><span data-stu-id="de548-110">EXAMPLES</span></span>

### <span data-ttu-id="de548-111">Példa 1: tároló-nyilvántartó webakasztó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="de548-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="de548-112">Hozzon létre egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="de548-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="de548-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de548-113">PARAMETERS</span></span>

### <span data-ttu-id="de548-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="de548-114">-Action</span></span>
<span data-ttu-id="de548-115">A webkampót elindító műveletek elvégzése az értesítések elküldésével</span><span class="sxs-lookup"><span data-stu-id="de548-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="de548-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de548-116">-DefaultProfile</span></span>
<span data-ttu-id="de548-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de548-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de548-118">-Header</span><span class="sxs-lookup"><span data-stu-id="de548-118">-Header</span></span>
<span data-ttu-id="de548-119">Egyéni fejlécek, amelyeket felvesz a webhook-értesítésekre.</span><span class="sxs-lookup"><span data-stu-id="de548-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="de548-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="de548-120">-Location</span></span>
<span data-ttu-id="de548-121">Webhook-hely</span><span class="sxs-lookup"><span data-stu-id="de548-121">Webhook Location.</span></span>
<span data-ttu-id="de548-122">A beállításjegyzék alapértelmezett helye.</span><span class="sxs-lookup"><span data-stu-id="de548-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="de548-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de548-123">-Name</span></span>
<span data-ttu-id="de548-124">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="de548-124">Webhook Name.</span></span>

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

### <span data-ttu-id="de548-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="de548-125">-Registry</span></span>
<span data-ttu-id="de548-126">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="de548-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="de548-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="de548-127">-RegistryName</span></span>
<span data-ttu-id="de548-128">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="de548-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="de548-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de548-129">-ResourceGroupName</span></span>
<span data-ttu-id="de548-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="de548-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="de548-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de548-131">-ResourceId</span></span>
<span data-ttu-id="de548-132">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="de548-132">The container registry resource id</span></span>

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

### <span data-ttu-id="de548-133">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="de548-133">-Scope</span></span>
<span data-ttu-id="de548-134">Webhook-hatókör</span><span class="sxs-lookup"><span data-stu-id="de548-134">Webhook scope.</span></span>

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

### <span data-ttu-id="de548-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="de548-135">-Status</span></span>
<span data-ttu-id="de548-136">Webhook-állapot, alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="de548-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="de548-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="de548-137">-Tag</span></span>
<span data-ttu-id="de548-138">Webhook-címkék.</span><span class="sxs-lookup"><span data-stu-id="de548-138">Webhook tags.</span></span>

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

### <span data-ttu-id="de548-139">-URI</span><span class="sxs-lookup"><span data-stu-id="de548-139">-Uri</span></span>
<span data-ttu-id="de548-140">A webhook szolgáltatás URI-ja értesítéseket küldhet.</span><span class="sxs-lookup"><span data-stu-id="de548-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="de548-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de548-141">-Confirm</span></span>
<span data-ttu-id="de548-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de548-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de548-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de548-143">-WhatIf</span></span>
<span data-ttu-id="de548-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de548-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de548-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de548-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de548-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de548-146">CommonParameters</span></span>
<span data-ttu-id="de548-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de548-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de548-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de548-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de548-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de548-149">INPUTS</span></span>

### <span data-ttu-id="de548-150">System. String</span><span class="sxs-lookup"><span data-stu-id="de548-150">System.String</span></span>

## <span data-ttu-id="de548-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de548-151">OUTPUTS</span></span>

### <span data-ttu-id="de548-152">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="de548-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de548-153">NOTES</span></span>

## <span data-ttu-id="de548-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de548-154">RELATED LINKS</span></span>

[<span data-ttu-id="de548-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de548-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de548-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="de548-158">Teszt-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="de548-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
