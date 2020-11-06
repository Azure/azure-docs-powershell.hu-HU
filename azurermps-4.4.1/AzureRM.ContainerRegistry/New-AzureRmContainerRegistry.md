---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493830"
---
# <span data-ttu-id="1818f-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1818f-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="1818f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1818f-102">SYNOPSIS</span></span>
<span data-ttu-id="1818f-103">Tároló-nyilvántartót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1818f-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1818f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1818f-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1818f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1818f-105">DESCRIPTION</span></span>
<span data-ttu-id="1818f-106">A **New-AzureRmContainerRegistry** parancsmag létrehoz egy tároló beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="1818f-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="1818f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1818f-107">EXAMPLES</span></span>

### <span data-ttu-id="1818f-108">1. példa: új tárterület-fiók létrehozása a tároló beállításjegyzékben.</span><span class="sxs-lookup"><span data-stu-id="1818f-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

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

<span data-ttu-id="1818f-109">Ez a parancs létrehoz egy tároló beállításjegyzéket az erőforráscsoport új tárterület-fiókjával `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="1818f-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="1818f-110">2. példa: a tároló beállításjegyzékének létrehozása engedélyezve van a rendszergazdai felhasználóval.</span><span class="sxs-lookup"><span data-stu-id="1818f-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

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
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="1818f-111">Ez a parancs létrehoz egy tároló beállításjegyzéket, amelyben engedélyezve van a rendszergazdai felhasználó.</span><span class="sxs-lookup"><span data-stu-id="1818f-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="1818f-112">3. példa: a tároló beállításjegyzékének létrehozása meglévő tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="1818f-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="1818f-113">Ez a parancs létrehoz egy tároló beállításjegyzéket egy meglévő tárterület `mystorageaccount` -fiókkal ugyanazon az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1818f-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="1818f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1818f-114">PARAMETERS</span></span>

### <span data-ttu-id="1818f-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1818f-115">-EnableAdminUser</span></span>
<span data-ttu-id="1818f-116">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="1818f-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1818f-117">-Location</span></span>
<span data-ttu-id="1818f-118">A tároló beállításjegyzékének helye.</span><span class="sxs-lookup"><span data-stu-id="1818f-118">Container Registry Location.</span></span>
<span data-ttu-id="1818f-119">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="1818f-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1818f-120">-Name</span></span>
<span data-ttu-id="1818f-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="1818f-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1818f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1818f-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1818f-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="1818f-124">-Sku</span></span>
<span data-ttu-id="1818f-125">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="1818f-125">Container Registry SKU.</span></span>
<span data-ttu-id="1818f-126">Engedélyezett értékek: egyszerű.</span><span class="sxs-lookup"><span data-stu-id="1818f-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1818f-127">-StorageAccountName</span></span>
<span data-ttu-id="1818f-128">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="1818f-128">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1818f-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="1818f-129">-Tag</span></span>
<span data-ttu-id="1818f-130">Tároló rendszerleíróadatbázis-címkék. kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1818f-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1818f-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="1818f-131">For example:</span></span>

<span data-ttu-id="1818f-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1818f-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1818f-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1818f-133">-Confirm</span></span>
<span data-ttu-id="1818f-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1818f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1818f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1818f-135">-WhatIf</span></span>
<span data-ttu-id="1818f-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1818f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1818f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1818f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1818f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1818f-138">-DefaultProfile</span></span>
<span data-ttu-id="1818f-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1818f-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1818f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1818f-140">CommonParameters</span></span>
<span data-ttu-id="1818f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1818f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1818f-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1818f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1818f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1818f-143">INPUTS</span></span>

## <span data-ttu-id="1818f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1818f-144">OUTPUTS</span></span>

### <span data-ttu-id="1818f-145">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1818f-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1818f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1818f-146">NOTES</span></span>

## <span data-ttu-id="1818f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1818f-147">RELATED LINKS</span></span>

[<span data-ttu-id="1818f-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1818f-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="1818f-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1818f-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="1818f-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1818f-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
