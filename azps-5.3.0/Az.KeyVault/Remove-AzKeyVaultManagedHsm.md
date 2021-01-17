---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465957"
---
# <span data-ttu-id="96f91-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="96f91-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="96f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96f91-102">SYNOPSIS</span></span>
<span data-ttu-id="96f91-103">Felügyelt HSM törlése.</span><span class="sxs-lookup"><span data-stu-id="96f91-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="96f91-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96f91-104">SYNTAX</span></span>

### <span data-ttu-id="96f91-105">RemoveManagedHsmByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96f91-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f91-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="96f91-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f91-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="96f91-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f91-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96f91-108">DESCRIPTION</span></span>
<span data-ttu-id="96f91-109">Az **Remove-AzKeyVaultManagedHsm** parancsmag törli a megadott felügyelt HSM-et.</span><span class="sxs-lookup"><span data-stu-id="96f91-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="96f91-110">Ezenkívül törli az ebben a példányban található összes billentyűt is.</span><span class="sxs-lookup"><span data-stu-id="96f91-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="96f91-111">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ennél a parancsmagnál, a jobb teljesítmény érdekében érdemes így lennie.</span><span class="sxs-lookup"><span data-stu-id="96f91-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="96f91-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96f91-112">EXAMPLES</span></span>

### <span data-ttu-id="96f91-113">1. példa: Felügyelt HSM eltávolítása</span><span class="sxs-lookup"><span data-stu-id="96f91-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="96f91-114">Ez a parancs eltávolítja a myhsm nevű felügyelt hsm-et az aktuális előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="96f91-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="96f91-115">2. példa: Felügyelt hsm eltávolítása egy adott erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="96f91-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="96f91-116">Ez a parancs eltávolítja a myhsm nevű felügyelt hsm-et a myrg1 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="96f91-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="96f91-117">Ha nem adja meg az erőforráscsoport nevét, a parancsmag megkeresi az aktuális előfizetésben törölni kívánt felügyelt HSM-et.</span><span class="sxs-lookup"><span data-stu-id="96f91-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="96f91-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96f91-118">PARAMETERS</span></span>

### <span data-ttu-id="96f91-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96f91-119">-AsJob</span></span>
<span data-ttu-id="96f91-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="96f91-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96f91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f91-121">-DefaultProfile</span></span>
<span data-ttu-id="96f91-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96f91-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f91-123">-Force</span><span class="sxs-lookup"><span data-stu-id="96f91-123">-Force</span></span>
<span data-ttu-id="96f91-124">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96f91-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="96f91-125">Ez a parancsmag alapértelmezés szerint kérni fogja, hogy erősítse meg a felügyelt HSM törlését.</span><span class="sxs-lookup"><span data-stu-id="96f91-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="96f91-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96f91-126">-InputObject</span></span>
<span data-ttu-id="96f91-127">Törölt felügyelt HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="96f91-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f91-128">-Name</span><span class="sxs-lookup"><span data-stu-id="96f91-128">-Name</span></span>
<span data-ttu-id="96f91-129">Az eltávolítható felügyelt HSM neve.</span><span class="sxs-lookup"><span data-stu-id="96f91-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f91-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96f91-130">-PassThru</span></span>
<span data-ttu-id="96f91-131">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="96f91-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="96f91-132">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="96f91-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="96f91-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f91-133">-ResourceGroupName</span></span>
<span data-ttu-id="96f91-134">Az Azure által felügyelt HSM-hez eltávolítható erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96f91-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f91-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96f91-135">-ResourceId</span></span>
<span data-ttu-id="96f91-136">ManagedHsm Resource Id.</span><span class="sxs-lookup"><span data-stu-id="96f91-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f91-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96f91-137">-Confirm</span></span>
<span data-ttu-id="96f91-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96f91-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f91-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f91-139">-WhatIf</span></span>
<span data-ttu-id="96f91-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96f91-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f91-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96f91-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f91-142">CommonParameters</span></span>
<span data-ttu-id="96f91-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f91-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96f91-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f91-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96f91-145">INPUTS</span></span>

### <span data-ttu-id="96f91-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="96f91-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="96f91-147">System.String</span><span class="sxs-lookup"><span data-stu-id="96f91-147">System.String</span></span>

## <span data-ttu-id="96f91-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96f91-148">OUTPUTS</span></span>

### <span data-ttu-id="96f91-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96f91-149">System.Boolean</span></span>

## <span data-ttu-id="96f91-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96f91-150">NOTES</span></span>

## <span data-ttu-id="96f91-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96f91-151">RELATED LINKS</span></span>

[<span data-ttu-id="96f91-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="96f91-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="96f91-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="96f91-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="96f91-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="96f91-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)