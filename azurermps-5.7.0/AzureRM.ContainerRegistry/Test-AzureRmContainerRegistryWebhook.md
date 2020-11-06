---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497655"
---
# <span data-ttu-id="1616f-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="1616f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1616f-102">SYNOPSIS</span></span>
<span data-ttu-id="1616f-103">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="1616f-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1616f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1616f-104">SYNTAX</span></span>

### <span data-ttu-id="1616f-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1616f-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1616f-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1616f-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1616f-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1616f-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1616f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1616f-108">DESCRIPTION</span></span>
<span data-ttu-id="1616f-109">A Test-AzureRmContainerRegistryWebhook parancsmag a webhook ping eseményét indítja el.</span><span class="sxs-lookup"><span data-stu-id="1616f-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="1616f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1616f-110">EXAMPLES</span></span>

### <span data-ttu-id="1616f-111">Példa 1: webhook-ping-esemény indítja el.</span><span class="sxs-lookup"><span data-stu-id="1616f-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="1616f-112">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="1616f-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="1616f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1616f-113">PARAMETERS</span></span>

### <span data-ttu-id="1616f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1616f-114">-DefaultProfile</span></span>
<span data-ttu-id="1616f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1616f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1616f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1616f-116">-Name</span></span>
<span data-ttu-id="1616f-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="1616f-117">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1616f-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1616f-118">-RegistryName</span></span>
<span data-ttu-id="1616f-119">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="1616f-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="1616f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1616f-120">-ResourceGroupName</span></span>
<span data-ttu-id="1616f-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1616f-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="1616f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1616f-122">-ResourceId</span></span>
<span data-ttu-id="1616f-123">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="1616f-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="1616f-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="1616f-124">-Webhook</span></span>
<span data-ttu-id="1616f-125">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="1616f-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1616f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1616f-126">CommonParameters</span></span>
<span data-ttu-id="1616f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1616f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1616f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1616f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1616f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1616f-129">INPUTS</span></span>

### <span data-ttu-id="1616f-130">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="1616f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1616f-131">System.String</span></span>

## <span data-ttu-id="1616f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1616f-132">OUTPUTS</span></span>

### <span data-ttu-id="1616f-133">Microsoft. Azure. Management. ContainerRegistry. models. EventInfo</span><span class="sxs-lookup"><span data-stu-id="1616f-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="1616f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1616f-134">NOTES</span></span>

## <span data-ttu-id="1616f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1616f-135">RELATED LINKS</span></span>

[<span data-ttu-id="1616f-136">Új – AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="1616f-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="1616f-138">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="1616f-139">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1616f-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
