---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299624"
---
# <span data-ttu-id="1ab55-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="1ab55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ab55-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab55-103">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="1ab55-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="1ab55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ab55-104">SYNTAX</span></span>

### <span data-ttu-id="1ab55-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ab55-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab55-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab55-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ab55-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab55-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ab55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ab55-108">DESCRIPTION</span></span>
<span data-ttu-id="1ab55-109">A Test-AzContainerRegistryWebhook parancsmag a webhook ping eseményét indítja el.</span><span class="sxs-lookup"><span data-stu-id="1ab55-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="1ab55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ab55-110">EXAMPLES</span></span>

### <span data-ttu-id="1ab55-111">Példa 1: webhook-ping-esemény indítja el.</span><span class="sxs-lookup"><span data-stu-id="1ab55-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="1ab55-112">Elindítja a webhook ping eseményt.</span><span class="sxs-lookup"><span data-stu-id="1ab55-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="1ab55-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ab55-113">PARAMETERS</span></span>

### <span data-ttu-id="1ab55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab55-114">-DefaultProfile</span></span>
<span data-ttu-id="1ab55-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ab55-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ab55-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ab55-116">-Name</span></span>
<span data-ttu-id="1ab55-117">Webhook-név.</span><span class="sxs-lookup"><span data-stu-id="1ab55-117">Webhook Name.</span></span>

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

### <span data-ttu-id="1ab55-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1ab55-118">-RegistryName</span></span>
<span data-ttu-id="1ab55-119">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="1ab55-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="1ab55-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab55-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ab55-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1ab55-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ab55-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab55-122">-ResourceId</span></span>
<span data-ttu-id="1ab55-123">A Container Registry webhook-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ab55-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="1ab55-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-124">-Webhook</span></span>
<span data-ttu-id="1ab55-125">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="1ab55-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="1ab55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab55-126">CommonParameters</span></span>
<span data-ttu-id="1ab55-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ab55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab55-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ab55-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab55-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ab55-129">INPUTS</span></span>

### <span data-ttu-id="1ab55-130">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="1ab55-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1ab55-131">System.String</span></span>

## <span data-ttu-id="1ab55-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ab55-132">OUTPUTS</span></span>

### <span data-ttu-id="1ab55-133">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="1ab55-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="1ab55-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ab55-134">NOTES</span></span>

## <span data-ttu-id="1ab55-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ab55-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ab55-136">Új – AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1ab55-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1ab55-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1ab55-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1ab55-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)