---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499175"
---
# <span data-ttu-id="0ebad-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ebad-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="0ebad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ebad-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebad-103">Tároló-nyilvántartót kap.</span><span class="sxs-lookup"><span data-stu-id="0ebad-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ebad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ebad-104">SYNTAX</span></span>

### <span data-ttu-id="0ebad-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ebad-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ebad-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ebad-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ebad-107">DESCRIPTION</span></span>
<span data-ttu-id="0ebad-108">A **Get-AzureRmContainerRegistry** parancsmag egy adott tároló-beállításjegyzéket vagy egy erőforráscsoport összes tároló-nyilvántartását, illetve az előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ebad-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="0ebad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ebad-109">EXAMPLES</span></span>

### <span data-ttu-id="0ebad-110">1. példa: a megadott tároló beállításjegyzékének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ebad-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="0ebad-111">Ez a parancs a megadott tároló beállításjegyzékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ebad-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="0ebad-112">2. példa: egy erőforráscsoport összes tároló-nyilvántartásának lekérése</span><span class="sxs-lookup"><span data-stu-id="0ebad-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="0ebad-113">Ez a parancs egy erőforráscsoport minden tároló-nyilvántartását beolvassa.</span><span class="sxs-lookup"><span data-stu-id="0ebad-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="0ebad-114">3. példa: az előfizetésben szereplő összes tároló-nyilvántartó-bejegyzés beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ebad-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="0ebad-115">Ez a parancs beilleszti az előfizetéshez tartozó összes tároló-nyilvántartót.</span><span class="sxs-lookup"><span data-stu-id="0ebad-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="0ebad-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ebad-116">PARAMETERS</span></span>

### <span data-ttu-id="0ebad-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ebad-117">-Name</span></span>
<span data-ttu-id="0ebad-118">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="0ebad-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebad-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ebad-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0ebad-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebad-121">-DefaultProfile</span></span>
<span data-ttu-id="0ebad-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ebad-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ebad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebad-123">CommonParameters</span></span>
<span data-ttu-id="0ebad-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ebad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebad-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebad-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ebad-126">INPUTS</span></span>

## <span data-ttu-id="0ebad-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ebad-127">OUTPUTS</span></span>

### <span data-ttu-id="0ebad-128">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ebad-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="0ebad-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ebad-129">NOTES</span></span>

## <span data-ttu-id="0ebad-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ebad-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ebad-131">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ebad-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="0ebad-132">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ebad-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="0ebad-133">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ebad-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

