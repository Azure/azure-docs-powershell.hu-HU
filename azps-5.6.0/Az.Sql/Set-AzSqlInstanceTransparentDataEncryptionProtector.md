---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 4f3b0bccd8f352d6870899473440b690381bec10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937329"
---
# <span data-ttu-id="93c88-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="93c88-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="93c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c88-102">SYNOPSIS</span></span>
<span data-ttu-id="93c88-103">Egy SQL-kezelt példány átlátszó adattitkosítási (TDE) védelmét állítja be.</span><span class="sxs-lookup"><span data-stu-id="93c88-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="93c88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93c88-104">SYNTAX</span></span>

### <span data-ttu-id="93c88-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93c88-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c88-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c88-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c88-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c88-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93c88-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93c88-108">DESCRIPTION</span></span>
<span data-ttu-id="93c88-109">A Set-AzSqlInstanceTransparentDataEncryptionProtector parancsmag beállítja egy SQL által felügyelt példány TDE-védelmét.</span><span class="sxs-lookup"><span data-stu-id="93c88-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="93c88-110">A TDE-védelem típusának módosítása elforgatja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="93c88-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="93c88-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93c88-111">EXAMPLES</span></span>

### <span data-ttu-id="93c88-112">1. példa: Az Átlátszó adattitkosítás (TDE) protector típusának beállítása ServiceManaged típusra</span><span class="sxs-lookup"><span data-stu-id="93c88-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="93c88-113">Ez a parancs frissíti a felügyelt példány TDE-védelem típusát Szolgáltatás által felügyelt típusra.</span><span class="sxs-lookup"><span data-stu-id="93c88-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="93c88-114">2. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra</span><span class="sxs-lookup"><span data-stu-id="93c88-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="93c88-115">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="93c88-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="93c88-116">3. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra felügyelt példányobjektum használatával</span><span class="sxs-lookup"><span data-stu-id="93c88-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="93c88-117">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="93c88-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="93c88-118">4. példa: Az átlátszó adattitkosítási védelem típusának beállítása Azure-kulcstárra erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="93c88-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="93c88-119">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="93c88-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="93c88-120">5. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="93c88-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="93c88-121">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="93c88-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="93c88-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93c88-122">PARAMETERS</span></span>

### <span data-ttu-id="93c88-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c88-123">-DefaultProfile</span></span>
<span data-ttu-id="93c88-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93c88-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c88-125">-Force</span><span class="sxs-lookup"><span data-stu-id="93c88-125">-Force</span></span>
<span data-ttu-id="93c88-126">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="93c88-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="93c88-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="93c88-127">-Instance</span></span>
<span data-ttu-id="93c88-128">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="93c88-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="93c88-129">-InstanceName</span></span>
<span data-ttu-id="93c88-130">A példány neve</span><span class="sxs-lookup"><span data-stu-id="93c88-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="93c88-131">-InstanceResourceId</span></span>
<span data-ttu-id="93c88-132">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="93c88-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="93c88-133">-KeyId</span></span>
<span data-ttu-id="93c88-134">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="93c88-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c88-135">-ResourceGroupName</span></span>
<span data-ttu-id="93c88-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="93c88-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-137">-Type</span><span class="sxs-lookup"><span data-stu-id="93c88-137">-Type</span></span>
<span data-ttu-id="93c88-138">Az Azure Sql-adatbázis átlátszó adattitkosítási védelem típusa.</span><span class="sxs-lookup"><span data-stu-id="93c88-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c88-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93c88-139">-Confirm</span></span>
<span data-ttu-id="93c88-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93c88-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c88-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c88-141">-WhatIf</span></span>
<span data-ttu-id="93c88-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93c88-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c88-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93c88-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c88-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c88-144">CommonParameters</span></span>
<span data-ttu-id="93c88-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c88-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c88-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93c88-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c88-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93c88-147">INPUTS</span></span>

### <span data-ttu-id="93c88-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="93c88-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="93c88-149">System.String</span><span class="sxs-lookup"><span data-stu-id="93c88-149">System.String</span></span>

## <span data-ttu-id="93c88-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c88-150">OUTPUTS</span></span>

### <span data-ttu-id="93c88-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="93c88-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="93c88-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93c88-152">NOTES</span></span>

## <span data-ttu-id="93c88-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93c88-153">RELATED LINKS</span></span>
