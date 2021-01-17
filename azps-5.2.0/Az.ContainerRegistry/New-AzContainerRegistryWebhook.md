---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356273"
---
# <span data-ttu-id="ea571-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="ea571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea571-102">SYNOPSIS</span></span>
<span data-ttu-id="ea571-103">Létrehoz egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="ea571-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="ea571-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea571-104">SYNTAX</span></span>

### <span data-ttu-id="ea571-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea571-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea571-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea571-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea571-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea571-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea571-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea571-108">DESCRIPTION</span></span>
<span data-ttu-id="ea571-109">A New-AzContainerRegistryWebhook parancsmag létrehoz egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="ea571-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="ea571-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea571-110">EXAMPLES</span></span>

### <span data-ttu-id="ea571-111">1. példa: Hozzon létre egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="ea571-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="ea571-112">Hozzon létre egy tárolóadatbázis-webhookot.</span><span class="sxs-lookup"><span data-stu-id="ea571-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="ea571-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea571-113">PARAMETERS</span></span>

### <span data-ttu-id="ea571-114">-Művelet</span><span class="sxs-lookup"><span data-stu-id="ea571-114">-Action</span></span>
<span data-ttu-id="ea571-115">Szóközvel elválasztott műveletlista, amely a webhook értesítéseket való bejegyzését váltja ki.</span><span class="sxs-lookup"><span data-stu-id="ea571-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="ea571-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea571-116">-DefaultProfile</span></span>
<span data-ttu-id="ea571-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea571-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea571-118">-Header</span><span class="sxs-lookup"><span data-stu-id="ea571-118">-Header</span></span>
<span data-ttu-id="ea571-119">A webhook értesítésekhez hozzáadható egyéni fejlécek.</span><span class="sxs-lookup"><span data-stu-id="ea571-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="ea571-120">-Location</span><span class="sxs-lookup"><span data-stu-id="ea571-120">-Location</span></span>
<span data-ttu-id="ea571-121">Webhook-hely.</span><span class="sxs-lookup"><span data-stu-id="ea571-121">Webhook Location.</span></span>
<span data-ttu-id="ea571-122">A beállításjegyzék alapértelmezett helye.</span><span class="sxs-lookup"><span data-stu-id="ea571-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="ea571-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ea571-123">-Name</span></span>
<span data-ttu-id="ea571-124">Webhook név.</span><span class="sxs-lookup"><span data-stu-id="ea571-124">Webhook Name.</span></span>

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

### <span data-ttu-id="ea571-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="ea571-125">-Registry</span></span>
<span data-ttu-id="ea571-126">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="ea571-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="ea571-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ea571-127">-RegistryName</span></span>
<span data-ttu-id="ea571-128">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="ea571-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="ea571-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea571-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea571-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea571-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea571-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea571-131">-ResourceId</span></span>
<span data-ttu-id="ea571-132">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ea571-132">The container registry resource id</span></span>

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

### <span data-ttu-id="ea571-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="ea571-133">-Scope</span></span>
<span data-ttu-id="ea571-134">Webhook hatóköre.</span><span class="sxs-lookup"><span data-stu-id="ea571-134">Webhook scope.</span></span>

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

### <span data-ttu-id="ea571-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="ea571-135">-Status</span></span>
<span data-ttu-id="ea571-136">Webhook status, default value is enabled</span><span class="sxs-lookup"><span data-stu-id="ea571-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="ea571-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea571-137">-Tag</span></span>
<span data-ttu-id="ea571-138">Webhook-címkék.</span><span class="sxs-lookup"><span data-stu-id="ea571-138">Webhook tags.</span></span>

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

### <span data-ttu-id="ea571-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="ea571-139">-Uri</span></span>
<span data-ttu-id="ea571-140">A webhook szolgáltatás URI-ja értesítéseket közzéten.</span><span class="sxs-lookup"><span data-stu-id="ea571-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="ea571-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea571-141">-Confirm</span></span>
<span data-ttu-id="ea571-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea571-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea571-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea571-143">-WhatIf</span></span>
<span data-ttu-id="ea571-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea571-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea571-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea571-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea571-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea571-146">CommonParameters</span></span>
<span data-ttu-id="ea571-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea571-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea571-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea571-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea571-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea571-149">INPUTS</span></span>

### <span data-ttu-id="ea571-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ea571-150">System.String</span></span>

## <span data-ttu-id="ea571-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea571-151">OUTPUTS</span></span>

### <span data-ttu-id="ea571-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="ea571-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea571-153">NOTES</span></span>

## <span data-ttu-id="ea571-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea571-154">RELATED LINKS</span></span>

[<span data-ttu-id="ea571-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea571-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea571-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea571-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea571-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)