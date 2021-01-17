---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375576"
---
# <span data-ttu-id="01d3e-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="01d3e-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="01d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="01d3e-103">Hozzáad egy kulcskulcsot a megadott felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="01d3e-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="01d3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01d3e-104">SYNTAX</span></span>

### <span data-ttu-id="01d3e-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01d3e-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d3e-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d3e-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d3e-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d3e-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d3e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01d3e-108">DESCRIPTION</span></span>
<span data-ttu-id="01d3e-109">A Add-AzSqlInstanceKeyVaultKey parancsmag hozzáad egy kulcskulcsot a megadott felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="01d3e-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="01d3e-110">A felügyelt példánynak "get, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a tárolóhoz, az alábbi parancsfájlt használva adjon engedélyt a felügyelt példánynak.</span><span class="sxs-lookup"><span data-stu-id="01d3e-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="01d3e-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="01d3e-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="01d3e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01d3e-112">EXAMPLES</span></span>

### <span data-ttu-id="01d3e-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="01d3e-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="01d3e-114">Ez a parancs a "ContosoResourceGroup" erőforráscsoport "ContosoManagedInstanceName" nevű SQL-kezelt példányához hozzáadja a kulcstár kulcskulcsát "Azonosító https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " értékekkel.</span><span class="sxs-lookup"><span data-stu-id="01d3e-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="01d3e-115">2. példa: Felügyelt példány objektum használata</span><span class="sxs-lookup"><span data-stu-id="01d3e-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="01d3e-116">Ez a parancs a "ContosoResourceGroup" erőforráscsoport "ContosoManagedInstanceName" nevű SQL-kezelt példányához hozzáadja a kulcstár kulcskulcsát "Azonosító https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " értékekkel.</span><span class="sxs-lookup"><span data-stu-id="01d3e-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="01d3e-117">3. példa: Felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="01d3e-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="01d3e-118">Ez a parancs a "ContosoResourceGroup" erőforráscsoport "ContosoManagedInstanceName" nevű SQL-kezelt példányához hozzáadja a kulcstár kulcskulcsát "Azonosító https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " értékekkel.</span><span class="sxs-lookup"><span data-stu-id="01d3e-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="01d3e-119">4. példa: Pipázás használata</span><span class="sxs-lookup"><span data-stu-id="01d3e-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="01d3e-120">Ez a parancs a "ContosoResourceGroup" erőforráscsoport "ContosoManagedInstanceName" nevű SQL-kezelt példányához hozzáadja a kulcstár kulcskulcsát "Azonosító https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " értékekkel.</span><span class="sxs-lookup"><span data-stu-id="01d3e-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="01d3e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d3e-121">PARAMETERS</span></span>

### <span data-ttu-id="01d3e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d3e-122">-DefaultProfile</span></span>
<span data-ttu-id="01d3e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01d3e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d3e-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="01d3e-124">-Instance</span></span>
<span data-ttu-id="01d3e-125">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="01d3e-125">The instance input object</span></span>

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

### <span data-ttu-id="01d3e-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="01d3e-126">-InstanceName</span></span>
<span data-ttu-id="01d3e-127">A példány neve</span><span class="sxs-lookup"><span data-stu-id="01d3e-127">The instance name</span></span>

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

### <span data-ttu-id="01d3e-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="01d3e-128">-InstanceResourceId</span></span>
<span data-ttu-id="01d3e-129">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="01d3e-129">The instance resource id</span></span>

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

### <span data-ttu-id="01d3e-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="01d3e-130">-KeyId</span></span>
<span data-ttu-id="01d3e-131">AzureKeyVault kulcsazonosító</span><span class="sxs-lookup"><span data-stu-id="01d3e-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="01d3e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d3e-132">-ResourceGroupName</span></span>
<span data-ttu-id="01d3e-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="01d3e-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="01d3e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01d3e-134">-Confirm</span></span>
<span data-ttu-id="01d3e-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01d3e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d3e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d3e-136">-WhatIf</span></span>
<span data-ttu-id="01d3e-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01d3e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d3e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01d3e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d3e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d3e-139">CommonParameters</span></span>
<span data-ttu-id="01d3e-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d3e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d3e-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01d3e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d3e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01d3e-142">INPUTS</span></span>

### <span data-ttu-id="01d3e-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="01d3e-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="01d3e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="01d3e-144">System.String</span></span>

## <span data-ttu-id="01d3e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d3e-145">OUTPUTS</span></span>

### <span data-ttu-id="01d3e-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="01d3e-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="01d3e-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01d3e-147">NOTES</span></span>

## <span data-ttu-id="01d3e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01d3e-148">RELATED LINKS</span></span>
