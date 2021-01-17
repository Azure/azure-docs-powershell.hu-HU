---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480624"
---
# <span data-ttu-id="84a4a-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84a4a-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="84a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="84a4a-103">Frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="84a4a-103">Updates a container registry.</span></span>

## <span data-ttu-id="84a4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84a4a-104">SYNTAX</span></span>

### <span data-ttu-id="84a4a-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84a4a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4a-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4a-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4a-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4a-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4a-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a4a-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84a4a-111">DESCRIPTION</span></span>
<span data-ttu-id="84a4a-112">A Update-AzContainerRegistry parancsmag frissíti a tároló beállításjegyzékét.</span><span class="sxs-lookup"><span data-stu-id="84a4a-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="84a4a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84a4a-113">EXAMPLES</span></span>

### <span data-ttu-id="84a4a-114">1. példa: Rendszergazdai felhasználó engedélyezése egy megadott tárolóadatbázishoz</span><span class="sxs-lookup"><span data-stu-id="84a4a-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="84a4a-115">Ez a parancs lehetővé teszi a rendszergazdai felhasználónak a megadott tárolóadatbázis-beállításjegyzéket.</span><span class="sxs-lookup"><span data-stu-id="84a4a-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="84a4a-116">2. példa: A megadott tárolóadatbázis által használt tárfiók beállítása</span><span class="sxs-lookup"><span data-stu-id="84a4a-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="84a4a-117">Ez a parancs úgy állítja be a megadott tároló beállításjegyzékét, hogy egy meglévő tárfiók \` mystorageaccount-ját használja \` ugyanabban az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="84a4a-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="84a4a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a4a-118">PARAMETERS</span></span>

### <span data-ttu-id="84a4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a4a-119">-DefaultProfile</span></span>
<span data-ttu-id="84a4a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="84a4a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84a4a-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="84a4a-121">-DisableAdminUser</span></span>
<span data-ttu-id="84a4a-122">Engedélyezze a rendszergazdai felhasználót a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="84a4a-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="84a4a-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="84a4a-123">-EnableAdminUser</span></span>
<span data-ttu-id="84a4a-124">Engedélyezze a rendszergazdai felhasználót a tároló beállításjegyzékéhez.</span><span class="sxs-lookup"><span data-stu-id="84a4a-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="84a4a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="84a4a-125">-Name</span></span>
<span data-ttu-id="84a4a-126">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="84a4a-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="84a4a-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="84a4a-127">-NetworkRuleSet</span></span>
<span data-ttu-id="84a4a-128">A tároló beállításjegyzékéhez beállított hálózati szabály.</span><span class="sxs-lookup"><span data-stu-id="84a4a-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="84a4a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a4a-129">-ResourceGroupName</span></span>
<span data-ttu-id="84a4a-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84a4a-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="84a4a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84a4a-131">-ResourceId</span></span>
<span data-ttu-id="84a4a-132">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="84a4a-132">The container registry resource id</span></span>

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

### <span data-ttu-id="84a4a-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="84a4a-133">-Sku</span></span>
<span data-ttu-id="84a4a-134">Container Registry termékváltozat.</span><span class="sxs-lookup"><span data-stu-id="84a4a-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="84a4a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84a4a-135">-StorageAccountName</span></span>
<span data-ttu-id="84a4a-136">Egy meglévő tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="84a4a-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="84a4a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="84a4a-137">-Tag</span></span>
<span data-ttu-id="84a4a-138">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="84a4a-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="84a4a-139">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="84a4a-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84a4a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84a4a-140">-Confirm</span></span>
<span data-ttu-id="84a4a-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84a4a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a4a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a4a-142">-WhatIf</span></span>
<span data-ttu-id="84a4a-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84a4a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a4a-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84a4a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a4a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a4a-145">CommonParameters</span></span>
<span data-ttu-id="84a4a-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a4a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a4a-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a4a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a4a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84a4a-148">INPUTS</span></span>

### <span data-ttu-id="84a4a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="84a4a-149">System.String</span></span>

## <span data-ttu-id="84a4a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84a4a-150">OUTPUTS</span></span>

### <span data-ttu-id="84a4a-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84a4a-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="84a4a-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84a4a-152">NOTES</span></span>

## <span data-ttu-id="84a4a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84a4a-153">RELATED LINKS</span></span>

[<span data-ttu-id="84a4a-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84a4a-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="84a4a-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84a4a-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="84a4a-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="84a4a-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

