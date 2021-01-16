---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338657"
---
# <span data-ttu-id="c8900-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c8900-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="c8900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8900-102">SYNOPSIS</span></span>
<span data-ttu-id="c8900-103">Egy kulcstár törlése.</span><span class="sxs-lookup"><span data-stu-id="c8900-103">Deletes a key vault.</span></span>

## <span data-ttu-id="c8900-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8900-104">SYNTAX</span></span>

### <span data-ttu-id="c8900-105">ByAvailableVault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8900-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8900-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c8900-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8900-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="c8900-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8900-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c8900-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8900-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="c8900-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8900-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c8900-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8900-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8900-111">DESCRIPTION</span></span>
<span data-ttu-id="c8900-112">Az **Remove-AzKeyVault** parancsmag törli a megadott kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="c8900-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="c8900-113">Ezenkívül az ebben az esetben található összes kulcsot és titkos kulcsot is törli.</span><span class="sxs-lookup"><span data-stu-id="c8900-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="c8900-114">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ennél a parancsmagnál, a jobb teljesítmény érdekében érdemes így lennie.</span><span class="sxs-lookup"><span data-stu-id="c8900-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="c8900-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8900-115">EXAMPLES</span></span>

### <span data-ttu-id="c8900-116">1. példa: Kulcstár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c8900-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="c8900-117">Ez a parancs eltávolítja a Contoso03Vault nevű kulcstárat az aktuális előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="c8900-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="c8900-118">2. példa: Kulcstár eltávolítása egy adott erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="c8900-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="c8900-119">Ez a parancs eltávolítja a Contoso03Vault nevű kulcstárat a megnevezett erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="c8900-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="c8900-120">Ha nem adja meg az erőforráscsoport nevét, a parancsmag rákeres az aktuális előfizetésében törölni kívánt elnevezett kulcstárra.</span><span class="sxs-lookup"><span data-stu-id="c8900-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="c8900-121">3. példa: Felügyelt hsm eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c8900-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="c8900-122">Ez a parancs eltávolítja a testManagedHsm nevű felügyelt hsm-et az aktuális előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="c8900-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="c8900-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8900-123">PARAMETERS</span></span>

### <span data-ttu-id="c8900-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8900-124">-AsJob</span></span>
<span data-ttu-id="c8900-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c8900-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8900-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8900-126">-DefaultProfile</span></span>
<span data-ttu-id="c8900-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8900-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8900-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c8900-128">-Force</span></span>
<span data-ttu-id="c8900-129">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8900-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="c8900-130">Ez a parancsmag alapértelmezés szerint kérni fogja, hogy erősítse meg a kulcstár törlését.</span><span class="sxs-lookup"><span data-stu-id="c8900-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="c8900-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8900-131">-InputObject</span></span>
<span data-ttu-id="c8900-132">Key Vault object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="c8900-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c8900-133">-InRemovedState</span></span>
<span data-ttu-id="c8900-134">Távolítsa el véglegesen a korábban törölt tárolót.</span><span class="sxs-lookup"><span data-stu-id="c8900-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-135">-Location</span><span class="sxs-lookup"><span data-stu-id="c8900-135">-Location</span></span>
<span data-ttu-id="c8900-136">A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="c8900-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8900-137">-PassThru</span></span>
<span data-ttu-id="c8900-138">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="c8900-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c8900-139">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="c8900-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c8900-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8900-140">-ResourceGroupName</span></span>
<span data-ttu-id="c8900-141">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8900-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8900-142">-ResourceId</span></span>
<span data-ttu-id="c8900-143">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c8900-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c8900-144">-VaultName</span></span>
<span data-ttu-id="c8900-145">Az eltávolítható kulcstár neve.</span><span class="sxs-lookup"><span data-stu-id="c8900-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8900-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8900-146">-Confirm</span></span>
<span data-ttu-id="c8900-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c8900-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8900-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8900-148">-WhatIf</span></span>
<span data-ttu-id="c8900-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c8900-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8900-150">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c8900-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8900-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8900-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8900-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8900-152">CommonParameters</span></span>
<span data-ttu-id="c8900-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8900-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8900-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8900-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8900-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8900-155">INPUTS</span></span>

### <span data-ttu-id="c8900-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c8900-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c8900-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c8900-157">System.String</span></span>

## <span data-ttu-id="c8900-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8900-158">OUTPUTS</span></span>

### <span data-ttu-id="c8900-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8900-159">System.Boolean</span></span>

## <span data-ttu-id="c8900-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8900-160">NOTES</span></span>

## <span data-ttu-id="c8900-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8900-161">RELATED LINKS</span></span>

[<span data-ttu-id="c8900-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c8900-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="c8900-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c8900-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
