---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185276"
---
# <span data-ttu-id="2f3a6-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="2f3a6-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="2f3a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3a6-103">Frissítse az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="2f3a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f3a6-104">SYNTAX</span></span>

### <span data-ttu-id="2f3a6-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f3a6-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f3a6-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f3a6-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f3a6-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f3a6-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f3a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f3a6-108">DESCRIPTION</span></span>
<span data-ttu-id="2f3a6-109">Ez a parancsmag frissíti az Azure Key Vault állapotát.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="2f3a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f3a6-110">EXAMPLES</span></span>

### <span data-ttu-id="2f3a6-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="2f3a6-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="2f3a6-112">Lehetővé teszi a védelem beállítását a csővezeték-szintaxis használatával.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="2f3a6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f3a6-113">PARAMETERS</span></span>

### <span data-ttu-id="2f3a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3a6-114">-DefaultProfile</span></span>
<span data-ttu-id="2f3a6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f3a6-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="2f3a6-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="2f3a6-117">Engedélyezze a kiürítési védelem funkcióját a kulcsfájl számára.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="2f3a6-118">Ha engedélyezve van, nem lehet letiltani.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="2f3a6-119">Ehhez a művelethez a Soft-delete beállítás be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="2f3a6-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f3a6-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="2f3a6-121">Engedélyezze vagy tiltsa le ezt a kulcspárt az adatműveletek engedélyezéséhez szerepköralapú hozzáférés-vezérlés (RBAC) segítségével.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="2f3a6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f3a6-122">-InputObject</span></span>
<span data-ttu-id="2f3a6-123">A Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-123">Key vault object.</span></span>

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

### <span data-ttu-id="2f3a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f3a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f3a6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="2f3a6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3a6-126">-ResourceId</span></span>
<span data-ttu-id="2f3a6-127">A fő pince erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="2f3a6-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2f3a6-128">-VaultName</span></span>
<span data-ttu-id="2f3a6-129">A kulcs boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-129">Name of the key vault.</span></span>

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

### <span data-ttu-id="2f3a6-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f3a6-130">-Confirm</span></span>
<span data-ttu-id="2f3a6-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f3a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f3a6-132">-WhatIf</span></span>
<span data-ttu-id="2f3a6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f3a6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f3a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3a6-135">CommonParameters</span></span>
<span data-ttu-id="2f3a6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f3a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3a6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3a6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f3a6-138">INPUTS</span></span>

### <span data-ttu-id="2f3a6-139">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="2f3a6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f3a6-140">System.String</span></span>

## <span data-ttu-id="2f3a6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f3a6-141">OUTPUTS</span></span>

### <span data-ttu-id="2f3a6-142">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="2f3a6-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2f3a6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f3a6-143">NOTES</span></span>

## <span data-ttu-id="2f3a6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f3a6-144">RELATED LINKS</span></span>
