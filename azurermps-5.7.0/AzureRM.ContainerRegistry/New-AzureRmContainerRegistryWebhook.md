---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497675"
---
# <span data-ttu-id="acf16-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="acf16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acf16-102">SYNOPSIS</span></span>
<span data-ttu-id="acf16-103">Létrehoz egy tároló-nyilvántartó webhorogot.</span><span class="sxs-lookup"><span data-stu-id="acf16-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acf16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acf16-104">SYNTAX</span></span>

### <span data-ttu-id="acf16-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acf16-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acf16-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf16-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf16-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf16-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf16-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="acf16-108">DESCRIPTION</span></span>
<span data-ttu-id="acf16-109">Az New-AzureRmContainerRegistryWebhook parancsmag létrehoz egy tárolót, melyet a webhook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="acf16-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="acf16-110">Példák</span><span class="sxs-lookup"><span data-stu-id="acf16-110">EXAMPLES</span></span>

### <span data-ttu-id="acf16-111">Példa 1: tároló-nyilvántartó webakasztó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="acf16-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="acf16-112">Hozzon létre egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="acf16-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="acf16-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acf16-113">PARAMETERS</span></span>

### <span data-ttu-id="acf16-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="acf16-114">-Action</span></span>
<span data-ttu-id="acf16-115">A webkampót elindító műveletek elvégzése az értesítések elküldésével</span><span class="sxs-lookup"><span data-stu-id="acf16-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="acf16-116">-Confirm</span></span>
<span data-ttu-id="acf16-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="acf16-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf16-118">-DefaultProfile</span></span>
<span data-ttu-id="acf16-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acf16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-120">-Header</span><span class="sxs-lookup"><span data-stu-id="acf16-120">-Header</span></span>
<span data-ttu-id="acf16-121">Egyéni fejlécek, amelyeket felvesz a webhook-értesítésekre.</span><span class="sxs-lookup"><span data-stu-id="acf16-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="acf16-122">-Location</span></span>
<span data-ttu-id="acf16-123">Webhook-hely</span><span class="sxs-lookup"><span data-stu-id="acf16-123">Webhook Location.</span></span>
<span data-ttu-id="acf16-124">A beállításjegyzék alapértelmezett helye.</span><span class="sxs-lookup"><span data-stu-id="acf16-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acf16-125">-Name</span></span>
<span data-ttu-id="acf16-126">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="acf16-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-127">-Registry</span><span class="sxs-lookup"><span data-stu-id="acf16-127">-Registry</span></span>
<span data-ttu-id="acf16-128">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="acf16-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="acf16-129">-RegistryName</span></span>
<span data-ttu-id="acf16-130">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="acf16-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf16-131">-ResourceGroupName</span></span>
<span data-ttu-id="acf16-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="acf16-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf16-133">-ResourceId</span></span>
<span data-ttu-id="acf16-134">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="acf16-134">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-135">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="acf16-135">-Scope</span></span>
<span data-ttu-id="acf16-136">Webhook-hatókör</span><span class="sxs-lookup"><span data-stu-id="acf16-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="acf16-137">-Status</span></span>
<span data-ttu-id="acf16-138">Webhook-állapot, alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="acf16-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="acf16-139">-Tag</span></span>
<span data-ttu-id="acf16-140">Webhook-címkék.</span><span class="sxs-lookup"><span data-stu-id="acf16-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-141">-URI</span><span class="sxs-lookup"><span data-stu-id="acf16-141">-Uri</span></span>
<span data-ttu-id="acf16-142">A webhook szolgáltatás URI-ja értesítéseket küldhet.</span><span class="sxs-lookup"><span data-stu-id="acf16-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf16-143">-WhatIf</span></span>
<span data-ttu-id="acf16-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="acf16-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf16-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="acf16-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf16-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf16-146">CommonParameters</span></span>
<span data-ttu-id="acf16-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acf16-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf16-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf16-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf16-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf16-149">INPUTS</span></span>

### <span data-ttu-id="acf16-150">System. String</span><span class="sxs-lookup"><span data-stu-id="acf16-150">System.String</span></span>

## <span data-ttu-id="acf16-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf16-151">OUTPUTS</span></span>

### <span data-ttu-id="acf16-152">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="acf16-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acf16-153">NOTES</span></span>

## <span data-ttu-id="acf16-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acf16-154">RELATED LINKS</span></span>

[<span data-ttu-id="acf16-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="acf16-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="acf16-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="acf16-158">Teszt-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="acf16-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
