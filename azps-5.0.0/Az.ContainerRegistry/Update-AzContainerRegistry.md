---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299615"
---
# <span data-ttu-id="27dbd-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27dbd-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="27dbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="27dbd-103">Frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="27dbd-103">Updates a container registry.</span></span>

## <span data-ttu-id="27dbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27dbd-104">SYNTAX</span></span>

### <span data-ttu-id="27dbd-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27dbd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbd-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbd-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbd-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbd-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbd-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27dbd-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="27dbd-111">DESCRIPTION</span></span>
<span data-ttu-id="27dbd-112">A Update-AzContainerRegistry parancsmag frissíti a tároló rendszerleíró adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="27dbd-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="27dbd-113">Példák</span><span class="sxs-lookup"><span data-stu-id="27dbd-113">EXAMPLES</span></span>

### <span data-ttu-id="27dbd-114">1. példa: a rendszergazdai felhasználó engedélyezése a megadott tároló beállításjegyzékhez</span><span class="sxs-lookup"><span data-stu-id="27dbd-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="27dbd-115">Ez a parancs a megadott tároló beállításjegyzékének rendszergazdai felhasználóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="27dbd-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="27dbd-116">2. példa: a megadott tároló-nyilvántartó által használt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="27dbd-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="27dbd-117">Ez a parancs beállítja a megadott tároló beállításjegyzékét, hogy egy meglévő tárolási fiókot \` mystorageaccount \` az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="27dbd-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="27dbd-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27dbd-118">PARAMETERS</span></span>

### <span data-ttu-id="27dbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dbd-119">-DefaultProfile</span></span>
<span data-ttu-id="27dbd-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="27dbd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27dbd-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="27dbd-121">-DisableAdminUser</span></span>
<span data-ttu-id="27dbd-122">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="27dbd-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="27dbd-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="27dbd-123">-EnableAdminUser</span></span>
<span data-ttu-id="27dbd-124">Engedélyezze a rendszergazdai felhasználóknak a tároló beállításjegyzékének használatát.</span><span class="sxs-lookup"><span data-stu-id="27dbd-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="27dbd-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27dbd-125">-Name</span></span>
<span data-ttu-id="27dbd-126">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="27dbd-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="27dbd-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27dbd-127">-NetworkRuleSet</span></span>
<span data-ttu-id="27dbd-128">A tároló beállításjegyzékéhez beállított hálózati szabály.</span><span class="sxs-lookup"><span data-stu-id="27dbd-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27dbd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27dbd-129">-ResourceGroupName</span></span>
<span data-ttu-id="27dbd-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="27dbd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="27dbd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27dbd-131">-ResourceId</span></span>
<span data-ttu-id="27dbd-132">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="27dbd-132">The container registry resource id</span></span>

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

### <span data-ttu-id="27dbd-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="27dbd-133">-Sku</span></span>
<span data-ttu-id="27dbd-134">Tároló rendszerleíró SKU (SKU)</span><span class="sxs-lookup"><span data-stu-id="27dbd-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="27dbd-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27dbd-135">-StorageAccountName</span></span>
<span data-ttu-id="27dbd-136">Egy meglévő tárterület-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="27dbd-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="27dbd-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="27dbd-137">-Tag</span></span>
<span data-ttu-id="27dbd-138">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="27dbd-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="27dbd-139">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="27dbd-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="27dbd-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27dbd-140">-Confirm</span></span>
<span data-ttu-id="27dbd-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27dbd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27dbd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dbd-142">-WhatIf</span></span>
<span data-ttu-id="27dbd-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27dbd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27dbd-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27dbd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27dbd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dbd-145">CommonParameters</span></span>
<span data-ttu-id="27dbd-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27dbd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dbd-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27dbd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dbd-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27dbd-148">INPUTS</span></span>

### <span data-ttu-id="27dbd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="27dbd-149">System.String</span></span>

## <span data-ttu-id="27dbd-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27dbd-150">OUTPUTS</span></span>

### <span data-ttu-id="27dbd-151">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27dbd-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="27dbd-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27dbd-152">NOTES</span></span>

## <span data-ttu-id="27dbd-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27dbd-153">RELATED LINKS</span></span>

[<span data-ttu-id="27dbd-154">Új – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27dbd-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="27dbd-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27dbd-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="27dbd-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27dbd-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

