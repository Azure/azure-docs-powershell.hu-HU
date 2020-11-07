---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 10321e780532cd522e7cc1d4532baa360350c324
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672111"
---
# <span data-ttu-id="79a44-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="79a44-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="79a44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79a44-102">SYNOPSIS</span></span>
<span data-ttu-id="79a44-103">Frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="79a44-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79a44-104">SYNTAX</span></span>

### <span data-ttu-id="79a44-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79a44-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a44-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a44-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a44-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a44-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a44-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a44-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a44-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a44-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a44-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a44-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a44-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="79a44-111">DESCRIPTION</span></span>
<span data-ttu-id="79a44-112">A Update-AzureRmContainerRegistry parancsmag frissíti a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="79a44-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="79a44-113">Példák</span><span class="sxs-lookup"><span data-stu-id="79a44-113">EXAMPLES</span></span>

### <span data-ttu-id="79a44-114">1. példa: a rendszergazdai felhasználó engedélyezése a megadott tároló beállításjegyzékhez</span><span class="sxs-lookup"><span data-stu-id="79a44-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="79a44-115">Ez a parancs a megadott tároló beállításjegyzékének rendszergazdai felhasználóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="79a44-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="79a44-116">2. példa: a megadott tároló-nyilvántartó által használt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="79a44-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="79a44-117">Ez a parancs beállítja a megadott tároló beállításjegyzékét, hogy egy meglévő tárolási fiókot \` mystorageaccount \` az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="79a44-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="79a44-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79a44-118">PARAMETERS</span></span>

### <span data-ttu-id="79a44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a44-119">-DefaultProfile</span></span>
<span data-ttu-id="79a44-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79a44-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79a44-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="79a44-121">-DisableAdminUser</span></span>
<span data-ttu-id="79a44-122">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="79a44-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="79a44-123">-EnableAdminUser</span></span>
<span data-ttu-id="79a44-124">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="79a44-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79a44-125">-Name</span></span>
<span data-ttu-id="79a44-126">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="79a44-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a44-127">-ResourceGroupName</span></span>
<span data-ttu-id="79a44-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="79a44-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79a44-129">-ResourceId</span></span>
<span data-ttu-id="79a44-130">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="79a44-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="79a44-131">-Sku</span></span>
<span data-ttu-id="79a44-132">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="79a44-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79a44-133">-StorageAccountName</span></span>
<span data-ttu-id="79a44-134">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="79a44-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="79a44-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="79a44-135">-Tag</span></span>
<span data-ttu-id="79a44-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="79a44-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="79a44-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="79a44-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79a44-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79a44-138">-Confirm</span></span>
<span data-ttu-id="79a44-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79a44-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a44-140">-WhatIf</span></span>
<span data-ttu-id="79a44-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79a44-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a44-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79a44-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a44-143">CommonParameters</span></span>
<span data-ttu-id="79a44-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79a44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a44-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a44-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a44-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79a44-146">INPUTS</span></span>

### <span data-ttu-id="79a44-147">System. String</span><span class="sxs-lookup"><span data-stu-id="79a44-147">System.String</span></span>

## <span data-ttu-id="79a44-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79a44-148">OUTPUTS</span></span>

### <span data-ttu-id="79a44-149">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="79a44-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="79a44-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79a44-150">NOTES</span></span>

## <span data-ttu-id="79a44-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79a44-151">RELATED LINKS</span></span>

[<span data-ttu-id="79a44-152">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="79a44-152">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="79a44-153">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="79a44-153">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="79a44-154">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="79a44-154">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

