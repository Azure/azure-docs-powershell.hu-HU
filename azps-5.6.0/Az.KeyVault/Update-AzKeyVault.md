---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 44d22938d2d9fd8d7830acf676ac0b953c6bdc4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931106"
---
# <span data-ttu-id="bade2-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bade2-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="bade2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bade2-102">SYNOPSIS</span></span>
<span data-ttu-id="bade2-103">Frissítse egy Azure-kulcstár állapotát.</span><span class="sxs-lookup"><span data-stu-id="bade2-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="bade2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bade2-104">SYNTAX</span></span>

### <span data-ttu-id="bade2-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bade2-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bade2-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bade2-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bade2-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bade2-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bade2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bade2-108">DESCRIPTION</span></span>
<span data-ttu-id="bade2-109">Ez a parancsmag frissíti egy Azure-kulcstár állapotát.</span><span class="sxs-lookup"><span data-stu-id="bade2-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="bade2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bade2-110">EXAMPLES</span></span>

### <span data-ttu-id="bade2-111">1. példa: Végleges végleges végleges védelem engedélyezése</span><span class="sxs-lookup"><span data-stu-id="bade2-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="bade2-112">A végleges végleges végleges védelmének lehetővé teszi a pipázás szintaxisát.</span><span class="sxs-lookup"><span data-stu-id="bade2-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="bade2-113">2. példa: Az RBAC-hitelesítés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="bade2-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="bade2-114">Engedélyezi az RBAC-hitelesítést a pipázás szintaxisával.</span><span class="sxs-lookup"><span data-stu-id="bade2-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="bade2-115">3. példa: Címkék beállítása</span><span class="sxs-lookup"><span data-stu-id="bade2-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="bade2-116">Beállítja a $keyVaultName kulcstár $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="bade2-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="bade2-117">4. példa: Címkék tisztítása</span><span class="sxs-lookup"><span data-stu-id="bade2-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="bade2-118">Törli egy másik nevű kulcstár $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="bade2-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="bade2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bade2-119">PARAMETERS</span></span>

### <span data-ttu-id="bade2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bade2-120">-DefaultProfile</span></span>
<span data-ttu-id="bade2-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bade2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bade2-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="bade2-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="bade2-123">Engedélyezze a végleges végleges védelem funkcióját ehhez a kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="bade2-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="bade2-124">Az engedélyezése után az alkalmazás nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="bade2-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="bade2-125">A szoftveres törlés bekapcsolás szükséges hozzá.</span><span class="sxs-lookup"><span data-stu-id="bade2-125">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="bade2-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="bade2-127">Engedélyezze vagy tiltsa le ezt a kulcstárat az adatműveletek szerepköralapú hozzáférés-vezérléssel (RBAC) való engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="bade2-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bade2-128">-InputObject</span></span>
<span data-ttu-id="bade2-129">Kulcstár-objektum.</span><span class="sxs-lookup"><span data-stu-id="bade2-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bade2-130">-ResourceGroupName</span></span>
<span data-ttu-id="bade2-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bade2-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bade2-132">-ResourceId</span></span>
<span data-ttu-id="bade2-133">A kulcstár erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bade2-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="bade2-134">-Tag</span></span>
<span data-ttu-id="bade2-135">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="bade2-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bade2-136">-VaultName</span></span>
<span data-ttu-id="bade2-137">A kulcstár neve.</span><span class="sxs-lookup"><span data-stu-id="bade2-137">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bade2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bade2-138">-Confirm</span></span>
<span data-ttu-id="bade2-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bade2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bade2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bade2-140">-WhatIf</span></span>
<span data-ttu-id="bade2-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bade2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bade2-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bade2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bade2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bade2-143">CommonParameters</span></span>
<span data-ttu-id="bade2-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bade2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bade2-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bade2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bade2-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bade2-146">INPUTS</span></span>

### <span data-ttu-id="bade2-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bade2-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bade2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bade2-148">System.String</span></span>

## <span data-ttu-id="bade2-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bade2-149">OUTPUTS</span></span>

### <span data-ttu-id="bade2-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bade2-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="bade2-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bade2-151">NOTES</span></span>

## <span data-ttu-id="bade2-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bade2-152">RELATED LINKS</span></span>
