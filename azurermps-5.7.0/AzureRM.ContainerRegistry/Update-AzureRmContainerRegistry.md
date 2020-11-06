---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497691"
---
# <span data-ttu-id="d07e1-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d07e1-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="d07e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d07e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d07e1-103">Frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="d07e1-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d07e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d07e1-104">SYNTAX</span></span>

### <span data-ttu-id="d07e1-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d07e1-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07e1-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d07e1-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07e1-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d07e1-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07e1-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d07e1-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07e1-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d07e1-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d07e1-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d07e1-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07e1-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d07e1-111">DESCRIPTION</span></span>
<span data-ttu-id="d07e1-112">A Update-AzureRmContainerRegistry parancsmag frissíti a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="d07e1-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="d07e1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d07e1-113">EXAMPLES</span></span>

### <span data-ttu-id="d07e1-114">1. példa: a rendszergazdai felhasználó engedélyezése a megadott tároló beállításjegyzékhez</span><span class="sxs-lookup"><span data-stu-id="d07e1-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="d07e1-115">Ez a parancs a megadott tároló beállításjegyzékének rendszergazdai felhasználóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="d07e1-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="d07e1-116">2. példa: a megadott tároló-nyilvántartó által használt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="d07e1-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="d07e1-117">Ez a parancs beállítja a megadott tároló beállításjegyzékét, hogy egy meglévő tárolási fiókot \` mystorageaccount \` az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d07e1-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="d07e1-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d07e1-118">PARAMETERS</span></span>

### <span data-ttu-id="d07e1-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d07e1-119">-DisableAdminUser</span></span>
<span data-ttu-id="d07e1-120">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="d07e1-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d07e1-121">-EnableAdminUser</span></span>
<span data-ttu-id="d07e1-122">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="d07e1-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d07e1-123">-Name</span></span>
<span data-ttu-id="d07e1-124">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="d07e1-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="d07e1-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d07e1-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d07e1-127">-StorageAccountName</span></span>
<span data-ttu-id="d07e1-128">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d07e1-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="d07e1-129">-Tag</span></span>
<span data-ttu-id="d07e1-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d07e1-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d07e1-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="d07e1-131">For example:</span></span>

<span data-ttu-id="d07e1-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d07e1-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d07e1-133">-Confirm</span></span>
<span data-ttu-id="d07e1-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d07e1-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07e1-135">-WhatIf</span></span>
<span data-ttu-id="d07e1-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d07e1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07e1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d07e1-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07e1-138">-DefaultProfile</span></span>
<span data-ttu-id="d07e1-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d07e1-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d07e1-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07e1-140">-ResourceId</span></span>
<span data-ttu-id="d07e1-141">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d07e1-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="d07e1-142">-Sku</span></span>
<span data-ttu-id="d07e1-143">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="d07e1-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07e1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07e1-144">CommonParameters</span></span>
<span data-ttu-id="d07e1-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d07e1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07e1-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07e1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07e1-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07e1-147">INPUTS</span></span>

### <span data-ttu-id="d07e1-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="d07e1-148">None</span></span>
<span data-ttu-id="d07e1-149">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d07e1-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d07e1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07e1-150">OUTPUTS</span></span>

### <span data-ttu-id="d07e1-151">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d07e1-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d07e1-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d07e1-152">NOTES</span></span>

## <span data-ttu-id="d07e1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d07e1-153">RELATED LINKS</span></span>

[<span data-ttu-id="d07e1-154">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d07e1-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="d07e1-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d07e1-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="d07e1-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d07e1-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

