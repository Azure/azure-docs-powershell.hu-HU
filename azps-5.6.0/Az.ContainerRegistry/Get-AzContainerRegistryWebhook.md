---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931353"
---
# <span data-ttu-id="15a7a-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="15a7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="15a7a-103">Tárolóadatbázis-webhookot kap.</span><span class="sxs-lookup"><span data-stu-id="15a7a-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="15a7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15a7a-104">SYNTAX</span></span>

### <span data-ttu-id="15a7a-105">ListWebhookByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15a7a-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a7a-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a7a-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a7a-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a7a-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a7a-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a7a-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a7a-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a7a-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a7a-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15a7a-110">DESCRIPTION</span></span>
<span data-ttu-id="15a7a-111">A Get-AzContainerRegistryWebhook parancsmag egy megadott webhook típusú tároló beállításjegyzéket vagy egy tároló beállításjegyzékének összes webhookját megkapja.</span><span class="sxs-lookup"><span data-stu-id="15a7a-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="15a7a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15a7a-112">EXAMPLES</span></span>

### <span data-ttu-id="15a7a-113">1. példa: Megadott webhook lekérte egy tároló beállításjegyzékét</span><span class="sxs-lookup"><span data-stu-id="15a7a-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="15a7a-114">Tároló beállításjegyzékének megadott webhook-ját lekérte</span><span class="sxs-lookup"><span data-stu-id="15a7a-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="15a7a-115">2. példa: Egy tároló beállításjegyzékének összes webhookja</span><span class="sxs-lookup"><span data-stu-id="15a7a-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="15a7a-116">A tárolóadatbázis összes webhooksának be szereznie</span><span class="sxs-lookup"><span data-stu-id="15a7a-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="15a7a-117">3. példa: A konfigurációs adatokat tartalmazó tárolóadatbázis megadott webhook-jának lekérte</span><span class="sxs-lookup"><span data-stu-id="15a7a-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="15a7a-118">A konfigurációs adatokat tartalmazó tárolóadatbázis megadott webhook-jának be szereznie</span><span class="sxs-lookup"><span data-stu-id="15a7a-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="15a7a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15a7a-119">PARAMETERS</span></span>

### <span data-ttu-id="15a7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a7a-120">-DefaultProfile</span></span>
<span data-ttu-id="15a7a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a7a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a7a-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="15a7a-122">-IncludeConfiguration</span></span>
<span data-ttu-id="15a7a-123">A webhook konfigurációs információinak lekérte.</span><span class="sxs-lookup"><span data-stu-id="15a7a-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="15a7a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="15a7a-124">-Name</span></span>
<span data-ttu-id="15a7a-125">Webhook név.</span><span class="sxs-lookup"><span data-stu-id="15a7a-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a7a-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="15a7a-126">-Registry</span></span>
<span data-ttu-id="15a7a-127">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="15a7a-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a7a-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="15a7a-128">-RegistryName</span></span>
<span data-ttu-id="15a7a-129">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="15a7a-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a7a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a7a-130">-ResourceGroupName</span></span>
<span data-ttu-id="15a7a-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15a7a-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a7a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a7a-132">-ResourceId</span></span>
<span data-ttu-id="15a7a-133">A tároló beállításjegyzékének Webhook erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="15a7a-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="15a7a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a7a-134">CommonParameters</span></span>
<span data-ttu-id="15a7a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a7a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a7a-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15a7a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a7a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15a7a-137">INPUTS</span></span>

### <span data-ttu-id="15a7a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15a7a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="15a7a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="15a7a-139">System.String</span></span>

## <span data-ttu-id="15a7a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a7a-140">OUTPUTS</span></span>

### <span data-ttu-id="15a7a-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="15a7a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15a7a-142">NOTES</span></span>

## <span data-ttu-id="15a7a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a7a-143">RELATED LINKS</span></span>

[<span data-ttu-id="15a7a-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="15a7a-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="15a7a-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="15a7a-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="15a7a-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)