---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503244"
---
# <span data-ttu-id="19023-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19023-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="19023-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19023-102">SYNOPSIS</span></span>
<span data-ttu-id="19023-103">Frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="19023-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19023-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19023-104">SYNTAX</span></span>

### <span data-ttu-id="19023-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19023-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19023-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="19023-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19023-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="19023-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19023-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="19023-108">DESCRIPTION</span></span>
<span data-ttu-id="19023-109">Az **Update-AzureRmContainerRegistry** parancsmag frissíti a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="19023-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="19023-110">Példák</span><span class="sxs-lookup"><span data-stu-id="19023-110">EXAMPLES</span></span>

### <span data-ttu-id="19023-111">1. példa: a rendszergazdai felhasználó engedélyezése a megadott tároló beállításjegyzékhez</span><span class="sxs-lookup"><span data-stu-id="19023-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="19023-112">Ez a parancs a megadott tároló beállításjegyzékének rendszergazdai felhasználóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="19023-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="19023-113">2. példa: a megadott tároló-nyilvántartó által használt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="19023-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="19023-114">Ez a parancs beállítja a megadott tároló beállításjegyzékét, hogy egy meglévő tárterület-fiókot használjon `mystorageaccount` ugyanazon az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="19023-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="19023-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19023-115">PARAMETERS</span></span>

### <span data-ttu-id="19023-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="19023-116">-DisableAdminUser</span></span>
<span data-ttu-id="19023-117">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="19023-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19023-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="19023-118">-EnableAdminUser</span></span>
<span data-ttu-id="19023-119">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="19023-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19023-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19023-120">-Name</span></span>
<span data-ttu-id="19023-121">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="19023-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="19023-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19023-122">-ResourceGroupName</span></span>
<span data-ttu-id="19023-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="19023-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="19023-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19023-124">-StorageAccountName</span></span>
<span data-ttu-id="19023-125">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="19023-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="19023-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="19023-126">-Tag</span></span>
<span data-ttu-id="19023-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="19023-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="19023-128">Példa:</span><span class="sxs-lookup"><span data-stu-id="19023-128">For example:</span></span>

<span data-ttu-id="19023-129">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="19023-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="19023-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19023-130">-Confirm</span></span>
<span data-ttu-id="19023-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19023-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19023-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19023-132">-WhatIf</span></span>
<span data-ttu-id="19023-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19023-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19023-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19023-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19023-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19023-135">-DefaultProfile</span></span>
<span data-ttu-id="19023-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19023-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19023-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19023-137">CommonParameters</span></span>
<span data-ttu-id="19023-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19023-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19023-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19023-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19023-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19023-140">INPUTS</span></span>

## <span data-ttu-id="19023-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19023-141">OUTPUTS</span></span>

### <span data-ttu-id="19023-142">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19023-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="19023-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19023-143">NOTES</span></span>

## <span data-ttu-id="19023-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19023-144">RELATED LINKS</span></span>

[<span data-ttu-id="19023-145">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19023-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="19023-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19023-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="19023-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19023-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
