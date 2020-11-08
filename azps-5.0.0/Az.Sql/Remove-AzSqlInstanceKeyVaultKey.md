---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185820"
---
# <span data-ttu-id="a1d27-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1d27-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="a1d27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1d27-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d27-103">Kulcs-Vault-kulcs eltávolítása SQL-alapú felügyelt példányból</span><span class="sxs-lookup"><span data-stu-id="a1d27-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="a1d27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1d27-104">SYNTAX</span></span>

### <span data-ttu-id="a1d27-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d27-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d27-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d27-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d27-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d27-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d27-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1d27-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d27-109">A Remove-AzSqlInstanceKeyVaultKey parancsmag eltávolítja a megadott felügyelt példányból a kulcsfájl kulcsát.</span><span class="sxs-lookup"><span data-stu-id="a1d27-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="a1d27-110">Ne feledje, hogy az SQL által felügyelt példánynak a kulcs boltozatához tartozó engedélyei nem változnak.</span><span class="sxs-lookup"><span data-stu-id="a1d27-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="a1d27-111">Az engedélyek módosításához használja a set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="a1d27-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="a1d27-112">Ne feledje, hogy ez a parancsmag nem változtatja meg a Key Vault-t.</span><span class="sxs-lookup"><span data-stu-id="a1d27-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="a1d27-113">Ha el szeretne távolítani egy billentyűt a Key Vault-ról, használja a Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="a1d27-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="a1d27-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a1d27-114">EXAMPLES</span></span>

### <span data-ttu-id="a1d27-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1d27-115">Example 1</span></span>
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

<span data-ttu-id="a1d27-116">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="a1d27-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="a1d27-117">2. példa: a Managed instance objektum használata</span><span class="sxs-lookup"><span data-stu-id="a1d27-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="a1d27-118">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="a1d27-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="a1d27-119">3. példa: a felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="a1d27-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="a1d27-120">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="a1d27-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="a1d27-121">Példa 4: csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="a1d27-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="a1d27-122">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott felügyelt példányból.</span><span class="sxs-lookup"><span data-stu-id="a1d27-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="a1d27-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1d27-123">PARAMETERS</span></span>

### <span data-ttu-id="a1d27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d27-124">-DefaultProfile</span></span>
<span data-ttu-id="a1d27-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d27-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d27-126">-Példány</span><span class="sxs-lookup"><span data-stu-id="a1d27-126">-Instance</span></span>
<span data-ttu-id="a1d27-127">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="a1d27-127">The instance input object</span></span>

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

### <span data-ttu-id="a1d27-128">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="a1d27-128">-InstanceName</span></span>
<span data-ttu-id="a1d27-129">A példány neve</span><span class="sxs-lookup"><span data-stu-id="a1d27-129">The instance name</span></span>

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

### <span data-ttu-id="a1d27-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d27-130">-InstanceResourceId</span></span>
<span data-ttu-id="a1d27-131">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a1d27-131">The instance resource id</span></span>

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

### <span data-ttu-id="a1d27-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a1d27-132">-KeyId</span></span>
<span data-ttu-id="a1d27-133">AzureKeyVault-kulcs azonosítója</span><span class="sxs-lookup"><span data-stu-id="a1d27-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="a1d27-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d27-134">-ResourceGroupName</span></span>
<span data-ttu-id="a1d27-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a1d27-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="a1d27-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1d27-136">-Confirm</span></span>
<span data-ttu-id="a1d27-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1d27-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d27-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d27-138">-WhatIf</span></span>
<span data-ttu-id="a1d27-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1d27-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d27-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1d27-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d27-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d27-141">CommonParameters</span></span>
<span data-ttu-id="a1d27-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1d27-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d27-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1d27-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d27-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d27-144">INPUTS</span></span>

### <span data-ttu-id="a1d27-145">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a1d27-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="a1d27-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d27-146">System.String</span></span>

## <span data-ttu-id="a1d27-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d27-147">OUTPUTS</span></span>

### <span data-ttu-id="a1d27-148">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="a1d27-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="a1d27-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1d27-149">NOTES</span></span>

## <span data-ttu-id="a1d27-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d27-150">RELATED LINKS</span></span>
