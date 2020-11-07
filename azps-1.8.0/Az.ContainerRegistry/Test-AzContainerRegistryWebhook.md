---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1fb56caef2af79ac8f2bafa9d402acd91de7b305
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671173"
---
# <span data-ttu-id="4e66a-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="4e66a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e66a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e66a-103">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="4e66a-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="4e66a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e66a-104">SYNTAX</span></span>

### <span data-ttu-id="4e66a-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e66a-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e66a-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e66a-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e66a-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e66a-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e66a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e66a-108">DESCRIPTION</span></span>
<span data-ttu-id="4e66a-109">A Test-AzContainerRegistryWebhook parancsmag a webhook ping eseményét indítja el.</span><span class="sxs-lookup"><span data-stu-id="4e66a-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="4e66a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e66a-110">EXAMPLES</span></span>

### <span data-ttu-id="4e66a-111">Példa 1: webhook-ping-esemény indítja el.</span><span class="sxs-lookup"><span data-stu-id="4e66a-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="4e66a-112">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="4e66a-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="4e66a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e66a-113">PARAMETERS</span></span>

### <span data-ttu-id="4e66a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e66a-114">-DefaultProfile</span></span>
<span data-ttu-id="4e66a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e66a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e66a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e66a-116">-Name</span></span>
<span data-ttu-id="4e66a-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="4e66a-117">Webhook Name.</span></span>

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

### <span data-ttu-id="4e66a-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4e66a-118">-RegistryName</span></span>
<span data-ttu-id="4e66a-119">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="4e66a-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="4e66a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e66a-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e66a-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4e66a-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e66a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e66a-122">-ResourceId</span></span>
<span data-ttu-id="4e66a-123">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4e66a-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4e66a-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-124">-Webhook</span></span>
<span data-ttu-id="4e66a-125">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="4e66a-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="4e66a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e66a-126">CommonParameters</span></span>
<span data-ttu-id="4e66a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e66a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e66a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e66a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e66a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e66a-129">INPUTS</span></span>

### <span data-ttu-id="4e66a-130">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="4e66a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e66a-131">System.String</span></span>

## <span data-ttu-id="4e66a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e66a-132">OUTPUTS</span></span>

### <span data-ttu-id="4e66a-133">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="4e66a-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="4e66a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e66a-134">NOTES</span></span>

## <span data-ttu-id="4e66a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e66a-135">RELATED LINKS</span></span>

[<span data-ttu-id="4e66a-136">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4e66a-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4e66a-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4e66a-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4e66a-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)