---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144051"
---
# <span data-ttu-id="cbaef-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbaef-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="cbaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbaef-102">SYNOPSIS</span></span>
<span data-ttu-id="cbaef-103">Kulcsbillentyű eltávolítása egy SQL-kezelt példányból</span><span class="sxs-lookup"><span data-stu-id="cbaef-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="cbaef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbaef-104">SYNTAX</span></span>

### <span data-ttu-id="cbaef-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbaef-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbaef-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbaef-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbaef-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbaef-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbaef-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbaef-108">DESCRIPTION</span></span>
<span data-ttu-id="cbaef-109">A Remove-AzSqlInstanceKeyVaultKey parancsmag eltávolítja a kulcstár kulcsát a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="cbaef-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="cbaef-110">Felhívjuk a figyelmét arra, hogy az SQL által felügyelt példánynak a kulcs tárolóhoz való engedélyei nem változnak.</span><span class="sxs-lookup"><span data-stu-id="cbaef-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="cbaef-111">Az engedélyeket a Set-AzKeyVaultAccessPolicy segítségével módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="cbaef-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="cbaef-112">Ne feledje, hogy ez a parancsmag nem módosítja a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="cbaef-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="cbaef-113">Ha el szeretne távolítani egy kulcsot a kulcstárból, használja az Remove-AzureKeyVaultKey kulcsot.</span><span class="sxs-lookup"><span data-stu-id="cbaef-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="cbaef-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbaef-114">EXAMPLES</span></span>

### <span data-ttu-id="cbaef-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbaef-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="cbaef-116">Ez a parancs eltávolítja a kulcstár kulcsát az Id ' ' azonosítóval https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="cbaef-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="cbaef-117">2. példa: Felügyelt példány objektum használata</span><span class="sxs-lookup"><span data-stu-id="cbaef-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="cbaef-118">Ez a parancs eltávolítja a kulcstár kulcsát az Id ' ' azonosítóval https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="cbaef-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="cbaef-119">3. példa: Felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="cbaef-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="cbaef-120">Ez a parancs eltávolítja a kulcstár kulcsát az Id ' ' azonosítóval https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="cbaef-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="cbaef-121">4. példa: Pipázás használata</span><span class="sxs-lookup"><span data-stu-id="cbaef-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="cbaef-122">Ez a parancs eltávolítja a kulcstár kulcsát az Id ' ' azonosítóval https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="cbaef-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="cbaef-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbaef-123">PARAMETERS</span></span>

### <span data-ttu-id="cbaef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbaef-124">-DefaultProfile</span></span>
<span data-ttu-id="cbaef-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbaef-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbaef-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="cbaef-126">-Instance</span></span>
<span data-ttu-id="cbaef-127">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="cbaef-127">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbaef-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cbaef-128">-InstanceName</span></span>
<span data-ttu-id="cbaef-129">A példány neve</span><span class="sxs-lookup"><span data-stu-id="cbaef-129">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbaef-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cbaef-130">-InstanceResourceId</span></span>
<span data-ttu-id="cbaef-131">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cbaef-131">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbaef-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cbaef-132">-KeyId</span></span>
<span data-ttu-id="cbaef-133">AzureKeyVault kulcsazonosító</span><span class="sxs-lookup"><span data-stu-id="cbaef-133">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbaef-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbaef-134">-ResourceGroupName</span></span>
<span data-ttu-id="cbaef-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cbaef-135">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbaef-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbaef-136">-Confirm</span></span>
<span data-ttu-id="cbaef-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cbaef-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbaef-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbaef-138">-WhatIf</span></span>
<span data-ttu-id="cbaef-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cbaef-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbaef-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbaef-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbaef-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbaef-141">CommonParameters</span></span>
<span data-ttu-id="cbaef-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbaef-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbaef-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbaef-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbaef-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbaef-144">INPUTS</span></span>

### <span data-ttu-id="cbaef-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cbaef-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="cbaef-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cbaef-146">System.String</span></span>

## <span data-ttu-id="cbaef-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbaef-147">OUTPUTS</span></span>

### <span data-ttu-id="cbaef-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="cbaef-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="cbaef-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbaef-149">NOTES</span></span>

## <span data-ttu-id="cbaef-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbaef-150">RELATED LINKS</span></span>
