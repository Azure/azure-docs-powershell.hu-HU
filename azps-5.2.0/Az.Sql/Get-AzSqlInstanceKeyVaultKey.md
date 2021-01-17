---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323451"
---
# <span data-ttu-id="efdeb-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="efdeb-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="efdeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="efdeb-103">Egy SQL-példány kulcstárkulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efdeb-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="efdeb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efdeb-104">SYNTAX</span></span>

### <span data-ttu-id="efdeb-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efdeb-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdeb-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdeb-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efdeb-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efdeb-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efdeb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efdeb-108">DESCRIPTION</span></span>
<span data-ttu-id="efdeb-109">A Get-AzSqlInstanceKeyVaultKey parancsmag információt kap az SQL által felügyelt példány kulcstár-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="efdeb-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="efdeb-110">A felügyelt példány összes kulcsát megtekintheti, vagy egy adott kulcsot a KeyId billentyű meg biztosításával.</span><span class="sxs-lookup"><span data-stu-id="efdeb-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="efdeb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efdeb-111">EXAMPLES</span></span>

### <span data-ttu-id="efdeb-112">1. példa: Az összes kulcstárbillentyű lekérte</span><span class="sxs-lookup"><span data-stu-id="efdeb-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="efdeb-113">Ez a parancs lekérte az SQL által felügyelt példány összes kulcskulcsát.</span><span class="sxs-lookup"><span data-stu-id="efdeb-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="efdeb-114">2. példa: Adott kulcstárkulcs lekérte</span><span class="sxs-lookup"><span data-stu-id="efdeb-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="efdeb-115">Ez a parancs a kulcstár kulcsát az Id ' '-val https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efdeb-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="efdeb-116">3. példa: Példányobjektum használata</span><span class="sxs-lookup"><span data-stu-id="efdeb-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="efdeb-117">Ez a parancs a kulcstár kulcsát az Id ' '-val https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efdeb-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="efdeb-118">4. példa: Példány típusú erőforrás-azonosító használata</span><span class="sxs-lookup"><span data-stu-id="efdeb-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="efdeb-119">Ez a parancs a kulcstár kulcsát az Id ' '-val https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efdeb-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="efdeb-120">5. példa: Pipázás használata</span><span class="sxs-lookup"><span data-stu-id="efdeb-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="efdeb-121">Ez a parancs a kulcstár kulcsát az Id ' '-val https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 kapja meg.</span><span class="sxs-lookup"><span data-stu-id="efdeb-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="efdeb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efdeb-122">PARAMETERS</span></span>

### <span data-ttu-id="efdeb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdeb-123">-DefaultProfile</span></span>
<span data-ttu-id="efdeb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efdeb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efdeb-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="efdeb-125">-Instance</span></span>
<span data-ttu-id="efdeb-126">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="efdeb-126">The instance input object</span></span>

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

### <span data-ttu-id="efdeb-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="efdeb-127">-InstanceName</span></span>
<span data-ttu-id="efdeb-128">A példány neve</span><span class="sxs-lookup"><span data-stu-id="efdeb-128">The instance name</span></span>

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

### <span data-ttu-id="efdeb-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="efdeb-129">-InstanceResourceId</span></span>
<span data-ttu-id="efdeb-130">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="efdeb-130">The instance resource id</span></span>

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

### <span data-ttu-id="efdeb-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="efdeb-131">-KeyId</span></span>
<span data-ttu-id="efdeb-132">AzureKeyVault kulcsazonosító</span><span class="sxs-lookup"><span data-stu-id="efdeb-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdeb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efdeb-133">-ResourceGroupName</span></span>
<span data-ttu-id="efdeb-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="efdeb-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="efdeb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efdeb-135">-Confirm</span></span>
<span data-ttu-id="efdeb-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efdeb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efdeb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efdeb-137">-WhatIf</span></span>
<span data-ttu-id="efdeb-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efdeb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efdeb-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efdeb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efdeb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdeb-140">CommonParameters</span></span>
<span data-ttu-id="efdeb-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efdeb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdeb-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efdeb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdeb-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efdeb-143">INPUTS</span></span>

### <span data-ttu-id="efdeb-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="efdeb-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="efdeb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="efdeb-145">System.String</span></span>

## <span data-ttu-id="efdeb-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efdeb-146">OUTPUTS</span></span>

### <span data-ttu-id="efdeb-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="efdeb-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="efdeb-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efdeb-148">NOTES</span></span>

## <span data-ttu-id="efdeb-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efdeb-149">RELATED LINKS</span></span>
