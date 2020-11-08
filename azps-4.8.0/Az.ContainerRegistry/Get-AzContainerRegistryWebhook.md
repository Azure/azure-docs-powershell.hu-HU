---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182884"
---
# <span data-ttu-id="4a172-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="4a172-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a172-102">SYNOPSIS</span></span>
<span data-ttu-id="4a172-103">Beilleszt egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="4a172-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="4a172-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a172-104">SYNTAX</span></span>

### <span data-ttu-id="4a172-105">ListWebhookByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a172-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a172-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a172-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a172-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a172-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a172-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a172-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a172-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a172-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a172-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a172-110">DESCRIPTION</span></span>
<span data-ttu-id="4a172-111">A Get-AzContainerRegistryWebhook parancsmag a tároló beállításjegyzékének egy megadott webhorogát vagy a tároló beállításjegyzékének összes webkampóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4a172-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="4a172-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4a172-112">EXAMPLES</span></span>

### <span data-ttu-id="4a172-113">Példa 1: a tároló beállításjegyzékének beszerzése meghatározott webhorogra</span><span class="sxs-lookup"><span data-stu-id="4a172-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="4a172-114">A tároló beállításjegyzékének beszerzése meghatározott webkampóval</span><span class="sxs-lookup"><span data-stu-id="4a172-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="4a172-115">2. példa: a Container-nyilvántartó összes webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4a172-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="4a172-116">A Container-nyilvántartó összes webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4a172-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="4a172-117">3. példa: a tároló beállításjegyzékének beszerzése meghatározott webhorogra konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="4a172-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="4a172-118">A tároló beállításjegyzékének beszerzése meghatározott webkampóval konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="4a172-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="4a172-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a172-119">PARAMETERS</span></span>

### <span data-ttu-id="4a172-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a172-120">-DefaultProfile</span></span>
<span data-ttu-id="4a172-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a172-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a172-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a172-122">-IncludeConfiguration</span></span>
<span data-ttu-id="4a172-123">Megtudhatja, hogy miként érheti el a webhook konfigurációs adatait.</span><span class="sxs-lookup"><span data-stu-id="4a172-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="4a172-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a172-124">-Name</span></span>
<span data-ttu-id="4a172-125">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="4a172-125">Webhook Name.</span></span>

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

### <span data-ttu-id="4a172-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="4a172-126">-Registry</span></span>
<span data-ttu-id="4a172-127">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="4a172-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="4a172-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4a172-128">-RegistryName</span></span>
<span data-ttu-id="4a172-129">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="4a172-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="4a172-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a172-130">-ResourceGroupName</span></span>
<span data-ttu-id="4a172-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4a172-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a172-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a172-132">-ResourceId</span></span>
<span data-ttu-id="4a172-133">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4a172-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4a172-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a172-134">CommonParameters</span></span>
<span data-ttu-id="4a172-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a172-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a172-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a172-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a172-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a172-137">INPUTS</span></span>

### <span data-ttu-id="4a172-138">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4a172-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="4a172-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4a172-139">System.String</span></span>

## <span data-ttu-id="4a172-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a172-140">OUTPUTS</span></span>

### <span data-ttu-id="4a172-141">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="4a172-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a172-142">NOTES</span></span>

## <span data-ttu-id="4a172-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a172-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a172-144">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4a172-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4a172-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4a172-147">Teszt-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4a172-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)