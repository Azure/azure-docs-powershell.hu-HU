---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503015"
---
# <span data-ttu-id="ce99c-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="ce99c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce99c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce99c-103">Beilleszt egy tároló-nyilvántartó webkampót.</span><span class="sxs-lookup"><span data-stu-id="ce99c-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce99c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce99c-104">SYNTAX</span></span>

### <span data-ttu-id="ce99c-105">ListWebhookByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce99c-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce99c-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce99c-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce99c-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce99c-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce99c-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce99c-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce99c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce99c-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce99c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce99c-110">DESCRIPTION</span></span>
<span data-ttu-id="ce99c-111">A Get-AzureRmContainerRegistryWebhook parancsmag a tároló beállításjegyzékének egy megadott webhorogát vagy a tároló beállításjegyzékének összes webkampóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ce99c-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="ce99c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ce99c-112">EXAMPLES</span></span>

### <span data-ttu-id="ce99c-113">Példa 1: a tároló beállításjegyzékének beszerzése meghatározott webhorogra</span><span class="sxs-lookup"><span data-stu-id="ce99c-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="ce99c-114">A tároló beállításjegyzékének beszerzése meghatározott webkampóval</span><span class="sxs-lookup"><span data-stu-id="ce99c-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="ce99c-115">2. példa: a Container-nyilvántartó összes webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ce99c-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="ce99c-116">A Container-nyilvántartó összes webakasztójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ce99c-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="ce99c-117">3. példa: a tároló beállításjegyzékének beszerzése meghatározott webhorogra konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="ce99c-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="ce99c-118">A tároló beállításjegyzékének beszerzése meghatározott webkampóval konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="ce99c-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="ce99c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce99c-119">PARAMETERS</span></span>

### <span data-ttu-id="ce99c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce99c-120">-DefaultProfile</span></span>
<span data-ttu-id="ce99c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce99c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce99c-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce99c-122">-IncludeConfiguration</span></span>
<span data-ttu-id="ce99c-123">Megtudhatja, hogy miként érheti el a webhook konfigurációs adatait.</span><span class="sxs-lookup"><span data-stu-id="ce99c-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="ce99c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce99c-124">-Name</span></span>
<span data-ttu-id="ce99c-125">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="ce99c-125">Webhook Name.</span></span>

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

### <span data-ttu-id="ce99c-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="ce99c-126">-Registry</span></span>
<span data-ttu-id="ce99c-127">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="ce99c-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="ce99c-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ce99c-128">-RegistryName</span></span>
<span data-ttu-id="ce99c-129">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="ce99c-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="ce99c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce99c-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce99c-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ce99c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="ce99c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce99c-132">-ResourceId</span></span>
<span data-ttu-id="ce99c-133">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="ce99c-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="ce99c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce99c-134">CommonParameters</span></span>
<span data-ttu-id="ce99c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce99c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce99c-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce99c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce99c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce99c-137">INPUTS</span></span>

### <span data-ttu-id="ce99c-138">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce99c-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="ce99c-139">Paraméterek: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ce99c-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="ce99c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce99c-140">System.String</span></span>

## <span data-ttu-id="ce99c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce99c-141">OUTPUTS</span></span>

### <span data-ttu-id="ce99c-142">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="ce99c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce99c-143">NOTES</span></span>

## <span data-ttu-id="ce99c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce99c-144">RELATED LINKS</span></span>

[<span data-ttu-id="ce99c-145">Új – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ce99c-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ce99c-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="ce99c-148">Teszt-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ce99c-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
