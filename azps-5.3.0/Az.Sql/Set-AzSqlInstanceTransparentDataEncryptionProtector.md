---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468057"
---
# <span data-ttu-id="26183-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="26183-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="26183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26183-102">SYNOPSIS</span></span>
<span data-ttu-id="26183-103">Egy SQL-kezelt példány átlátszó adattitkosítási (TDE) védelmét állítja be.</span><span class="sxs-lookup"><span data-stu-id="26183-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="26183-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26183-104">SYNTAX</span></span>

### <span data-ttu-id="26183-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26183-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26183-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26183-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26183-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26183-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26183-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26183-108">DESCRIPTION</span></span>
<span data-ttu-id="26183-109">A Set-AzSqlInstanceTransparentDataEncryptionProtector parancsmag beállítja egy SQL által felügyelt példány TDE-védelmét.</span><span class="sxs-lookup"><span data-stu-id="26183-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="26183-110">A TDE-védelem típusának módosítása elforgatja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="26183-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="26183-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26183-111">EXAMPLES</span></span>

### <span data-ttu-id="26183-112">1. példa: Az Átlátszó adattitkosítás (TDE) protector típusának beállítása ServiceManaged típusra</span><span class="sxs-lookup"><span data-stu-id="26183-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="26183-113">Ez a parancs frissíti a felügyelt példány TDE-védelem típusát Szolgáltatás által felügyelt típusra.</span><span class="sxs-lookup"><span data-stu-id="26183-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="26183-114">2. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra</span><span class="sxs-lookup"><span data-stu-id="26183-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="26183-115">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="26183-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="26183-116">3. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra felügyelt példányobjektum használatával</span><span class="sxs-lookup"><span data-stu-id="26183-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="26183-117">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="26183-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="26183-118">4. példa: Az átlátszó adattitkosítási védelem típusának beállítása Azure-kulcstárra erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="26183-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="26183-119">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="26183-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="26183-120">5. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="26183-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="26183-121">Ez a parancs frissíti a megadott felügyelt példányt úgy, hogy a Felügyelt példány kulcs tárolókulcsát használja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE-védelemként az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="26183-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="26183-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26183-122">PARAMETERS</span></span>

### <span data-ttu-id="26183-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26183-123">-DefaultProfile</span></span>
<span data-ttu-id="26183-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26183-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26183-125">-Force</span><span class="sxs-lookup"><span data-stu-id="26183-125">-Force</span></span>
<span data-ttu-id="26183-126">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="26183-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="26183-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="26183-127">-Instance</span></span>
<span data-ttu-id="26183-128">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="26183-128">The instance input object</span></span>

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

### <span data-ttu-id="26183-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="26183-129">-InstanceName</span></span>
<span data-ttu-id="26183-130">A példány neve</span><span class="sxs-lookup"><span data-stu-id="26183-130">The instance name</span></span>

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

### <span data-ttu-id="26183-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="26183-131">-InstanceResourceId</span></span>
<span data-ttu-id="26183-132">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="26183-132">The instance resource id</span></span>

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

### <span data-ttu-id="26183-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="26183-133">-KeyId</span></span>
<span data-ttu-id="26183-134">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="26183-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="26183-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26183-135">-ResourceGroupName</span></span>
<span data-ttu-id="26183-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="26183-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="26183-137">-Type</span><span class="sxs-lookup"><span data-stu-id="26183-137">-Type</span></span>
<span data-ttu-id="26183-138">Az Azure Sql-adatbázis átlátszó adattitkosítási védelem típusa.</span><span class="sxs-lookup"><span data-stu-id="26183-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="26183-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26183-139">-Confirm</span></span>
<span data-ttu-id="26183-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26183-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26183-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26183-141">-WhatIf</span></span>
<span data-ttu-id="26183-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26183-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26183-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26183-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26183-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26183-144">CommonParameters</span></span>
<span data-ttu-id="26183-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26183-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26183-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26183-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26183-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26183-147">INPUTS</span></span>

### <span data-ttu-id="26183-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="26183-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="26183-149">System.String</span><span class="sxs-lookup"><span data-stu-id="26183-149">System.String</span></span>

## <span data-ttu-id="26183-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26183-150">OUTPUTS</span></span>

### <span data-ttu-id="26183-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="26183-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="26183-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26183-152">NOTES</span></span>

## <span data-ttu-id="26183-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26183-153">RELATED LINKS</span></span>
