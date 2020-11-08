---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181701"
---
# <span data-ttu-id="056c3-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="056c3-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="056c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="056c3-102">SYNOPSIS</span></span>
<span data-ttu-id="056c3-103">Frissítse az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="056c3-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="056c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="056c3-104">SYNTAX</span></span>

### <span data-ttu-id="056c3-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="056c3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="056c3-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="056c3-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="056c3-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="056c3-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="056c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="056c3-108">DESCRIPTION</span></span>
<span data-ttu-id="056c3-109">Ez a parancsmag frissíti az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="056c3-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="056c3-110">Felhívjuk a figyelmét arra, hogy a tulajdonságok némelyike visszafordíthatatlan művelet, például ha be van kapcsolva a finom törlés, a továbbiakban nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="056c3-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="056c3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="056c3-111">EXAMPLES</span></span>

### <span data-ttu-id="056c3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="056c3-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="056c3-113">Lehetővé teszi a finom törlést az erőforrás csoportban elnevezett kulcs boltozatakor `$keyVaultName` `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="056c3-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="056c3-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="056c3-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="056c3-115">Lehetővé teszi a védelem beállítását a csővezeték-szintaxis használatával.</span><span class="sxs-lookup"><span data-stu-id="056c3-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="056c3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="056c3-116">PARAMETERS</span></span>

### <span data-ttu-id="056c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056c3-117">-DefaultProfile</span></span>
<span data-ttu-id="056c3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="056c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="056c3-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="056c3-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="056c3-120">Engedélyezze a kiürítési védelem funkcióját a kulcsfájl számára.</span><span class="sxs-lookup"><span data-stu-id="056c3-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="056c3-121">Ha engedélyezve van, nem lehet letiltani.</span><span class="sxs-lookup"><span data-stu-id="056c3-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="056c3-122">Ehhez a művelethez a Soft-delete beállítás be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="056c3-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="056c3-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="056c3-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="056c3-124">Engedélyezze vagy tiltsa le ezt a kulcspárt az adatműveletek engedélyezéséhez szerepköralapú hozzáférés-vezérlés (RBAC) segítségével.</span><span class="sxs-lookup"><span data-stu-id="056c3-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="056c3-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="056c3-125">-EnableSoftDelete</span></span>
<span data-ttu-id="056c3-126">A Soft-delete funkció engedélyezése a fő boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="056c3-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="056c3-127">Ha engedélyezve van, nem lehet letiltani.</span><span class="sxs-lookup"><span data-stu-id="056c3-127">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="056c3-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="056c3-128">-InputObject</span></span>
<span data-ttu-id="056c3-129">A Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="056c3-129">Key vault object.</span></span>

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

### <span data-ttu-id="056c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="056c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="056c3-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="056c3-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="056c3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="056c3-132">-ResourceId</span></span>
<span data-ttu-id="056c3-133">A fő pince erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="056c3-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="056c3-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="056c3-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="056c3-135">Itt adhatja meg, hogy a törölt erőforrások mennyi ideig maradnak, és mennyi ideig maradjon, amíg el nem távolítható egy boltozat vagy objektum a törölt állapotban.</span><span class="sxs-lookup"><span data-stu-id="056c3-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="056c3-136">Az alapértelmezett érték 90 nap.</span><span class="sxs-lookup"><span data-stu-id="056c3-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056c3-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="056c3-137">-VaultName</span></span>
<span data-ttu-id="056c3-138">A kulcs boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="056c3-138">Name of the key vault.</span></span>

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

### <span data-ttu-id="056c3-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="056c3-139">-Confirm</span></span>
<span data-ttu-id="056c3-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="056c3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="056c3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="056c3-141">-WhatIf</span></span>
<span data-ttu-id="056c3-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="056c3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="056c3-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="056c3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="056c3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056c3-144">CommonParameters</span></span>
<span data-ttu-id="056c3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="056c3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056c3-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="056c3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056c3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="056c3-147">INPUTS</span></span>

### <span data-ttu-id="056c3-148">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="056c3-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="056c3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="056c3-149">System.String</span></span>

## <span data-ttu-id="056c3-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="056c3-150">OUTPUTS</span></span>

### <span data-ttu-id="056c3-151">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="056c3-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="056c3-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="056c3-152">NOTES</span></span>

## <span data-ttu-id="056c3-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="056c3-153">RELATED LINKS</span></span>
