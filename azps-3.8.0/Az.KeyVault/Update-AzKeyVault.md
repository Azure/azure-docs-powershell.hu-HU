---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846025"
---
# <span data-ttu-id="8e7ca-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8e7ca-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="8e7ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7ca-103">Frissítse az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="8e7ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e7ca-104">SYNTAX</span></span>

### <span data-ttu-id="8e7ca-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e7ca-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7ca-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e7ca-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7ca-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e7ca-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7ca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e7ca-108">DESCRIPTION</span></span>
<span data-ttu-id="8e7ca-109">Ez a parancsmag frissíti az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="8e7ca-110">Felhívjuk a figyelmét arra, hogy a tulajdonságok némelyike visszafordíthatatlan művelet, például ha be van kapcsolva a finom törlés, a továbbiakban nem tiltható le.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="8e7ca-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8e7ca-111">EXAMPLES</span></span>

### <span data-ttu-id="8e7ca-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e7ca-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="8e7ca-113">Lehetővé teszi a finom törlést az erőforrás csoportban elnevezett kulcs boltozatakor `$keyVaultName` `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="8e7ca-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="8e7ca-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e7ca-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="8e7ca-115">Lehetővé teszi a védelem beállítását a csővezeték-szintaxis használatával.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="8e7ca-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e7ca-116">PARAMETERS</span></span>

### <span data-ttu-id="8e7ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7ca-117">-DefaultProfile</span></span>
<span data-ttu-id="8e7ca-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="8e7ca-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="8e7ca-120">Engedélyezze a kiürítési védelem funkcióját a kulcsfájl számára.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="8e7ca-121">Ha engedélyezve van, nem lehet letiltani.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="8e7ca-122">Ehhez a művelethez a Soft-delete beállítás be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="8e7ca-123">-EnableSoftDelete</span></span>
<span data-ttu-id="8e7ca-124">A Soft-delete funkció engedélyezése a fő boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="8e7ca-125">Ha engedélyezve van, nem lehet letiltani.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-125">Once enabled it cannot be disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e7ca-126">-InputObject</span></span>
<span data-ttu-id="8e7ca-127">A Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e7ca-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7ca-130">-ResourceId</span></span>
<span data-ttu-id="8e7ca-131">A fő pince erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8e7ca-132">-VaultName</span></span>
<span data-ttu-id="8e7ca-133">A kulcs boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e7ca-134">-Confirm</span></span>
<span data-ttu-id="8e7ca-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7ca-136">-WhatIf</span></span>
<span data-ttu-id="8e7ca-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e7ca-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7ca-139">CommonParameters</span></span>
<span data-ttu-id="8e7ca-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e7ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7ca-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7ca-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e7ca-142">INPUTS</span></span>

### <span data-ttu-id="8e7ca-143">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8e7ca-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7ca-144">System.String</span></span>

## <span data-ttu-id="8e7ca-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e7ca-145">OUTPUTS</span></span>

### <span data-ttu-id="8e7ca-146">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8e7ca-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e7ca-147">NOTES</span></span>

## <span data-ttu-id="8e7ca-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e7ca-148">RELATED LINKS</span></span>
