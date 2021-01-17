---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477546"
---
# <span data-ttu-id="2e9e8-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="2e9e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9e8-103">Webhook pingelési eseményt indít el.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="2e9e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e9e8-104">SYNTAX</span></span>

### <span data-ttu-id="2e9e8-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e9e8-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e9e8-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e9e8-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e9e8-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e9e8-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e9e8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e9e8-108">DESCRIPTION</span></span>
<span data-ttu-id="2e9e8-109">A Test-AzContainerRegistryWebhook parancsmag webhook pingelési eseményt indít el.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="2e9e8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e9e8-110">EXAMPLES</span></span>

### <span data-ttu-id="2e9e8-111">1. példa: Webhook ping esemény kiváltása.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="2e9e8-112">Webhook pingelési eseményt indít el.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="2e9e8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e9e8-113">PARAMETERS</span></span>

### <span data-ttu-id="2e9e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9e8-114">-DefaultProfile</span></span>
<span data-ttu-id="2e9e8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e9e8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2e9e8-116">-Name</span></span>
<span data-ttu-id="2e9e8-117">Webhook név.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-117">Webhook Name.</span></span>

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

### <span data-ttu-id="2e9e8-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2e9e8-118">-RegistryName</span></span>
<span data-ttu-id="2e9e8-119">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="2e9e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e9e8-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e9e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e9e8-122">-ResourceId</span></span>
<span data-ttu-id="2e9e8-123">A tároló beállításjegyzékének Webhook erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e9e8-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="2e9e8-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-124">-Webhook</span></span>
<span data-ttu-id="2e9e8-125">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="2e9e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9e8-126">CommonParameters</span></span>
<span data-ttu-id="2e9e8-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e9e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9e8-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e9e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9e8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e9e8-129">INPUTS</span></span>

### <span data-ttu-id="2e9e8-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="2e9e8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2e9e8-131">System.String</span></span>

## <span data-ttu-id="2e9e8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e9e8-132">OUTPUTS</span></span>

### <span data-ttu-id="2e9e8-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="2e9e8-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="2e9e8-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e9e8-134">NOTES</span></span>

## <span data-ttu-id="2e9e8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e9e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="2e9e8-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2e9e8-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2e9e8-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2e9e8-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2e9e8-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)