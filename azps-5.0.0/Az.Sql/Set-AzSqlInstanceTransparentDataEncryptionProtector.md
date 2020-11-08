---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186962"
---
# <span data-ttu-id="a111f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a111f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="a111f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a111f-102">SYNOPSIS</span></span>
<span data-ttu-id="a111f-103">Az átlátszó adattitkosítás (TDE) Protector beállítása SQL-alapú felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="a111f-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="a111f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a111f-104">SYNTAX</span></span>

### <span data-ttu-id="a111f-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a111f-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a111f-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a111f-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a111f-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a111f-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a111f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a111f-108">DESCRIPTION</span></span>
<span data-ttu-id="a111f-109">Az Set-AzSqlInstanceTransparentDataEncryptionProtector parancsmag az SQL-alapú felügyelt példány TDE-oltalmazóját állítja be.</span><span class="sxs-lookup"><span data-stu-id="a111f-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="a111f-110">A TDE Protector típusának módosítása elforgatja a oltalmazót.</span><span class="sxs-lookup"><span data-stu-id="a111f-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="a111f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a111f-111">EXAMPLES</span></span>

### <span data-ttu-id="a111f-112">1. példa: az átlátszó adattitkosítás (TDE) Protector típusának beállítása az ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="a111f-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="a111f-113">Ez a parancs a felügyelt példányok TDE-Protector típusát frissíti a felügyelt szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="a111f-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="a111f-114">2. példa: az átlátszó adattitkosítási Protector típus beállítása az Azure Key Vault szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="a111f-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a111f-115">Ez a parancs frissíti a megadott felügyelt példányt, hogy a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" azonosítójú "" TDE Protector "néven használja a felügyelt példány kulcsát.</span><span class="sxs-lookup"><span data-stu-id="a111f-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="a111f-116">3. példa: a Managed Data Encryption Protector típus beállítása az Azure Key Vault-ba a Managed instance objektummal</span><span class="sxs-lookup"><span data-stu-id="a111f-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a111f-117">Ez a parancs frissíti a megadott felügyelt példányt, hogy a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" azonosítójú "" TDE Protector "néven használja a felügyelt példány kulcsát.</span><span class="sxs-lookup"><span data-stu-id="a111f-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="a111f-118">Példa 4: az átlátszó adattitkosítási Protector típus beállítása az Azure Key Vault-ba erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="a111f-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a111f-119">Ez a parancs frissíti a megadott felügyelt példányt, hogy a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" azonosítójú "" TDE Protector "néven használja a felügyelt példány kulcsát.</span><span class="sxs-lookup"><span data-stu-id="a111f-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="a111f-120">Példa 5: az átlátszó adattitkosítási Protector típus beállítása az Azure Key Vault-ba csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="a111f-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a111f-121">Ez a parancs frissíti a megadott felügyelt példányt, hogy a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" azonosítójú "" TDE Protector "néven használja a felügyelt példány kulcsát.</span><span class="sxs-lookup"><span data-stu-id="a111f-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="a111f-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a111f-122">PARAMETERS</span></span>

### <span data-ttu-id="a111f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a111f-123">-DefaultProfile</span></span>
<span data-ttu-id="a111f-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a111f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a111f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a111f-125">-Force</span></span>
<span data-ttu-id="a111f-126">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="a111f-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a111f-127">-Példány</span><span class="sxs-lookup"><span data-stu-id="a111f-127">-Instance</span></span>
<span data-ttu-id="a111f-128">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="a111f-128">The instance input object</span></span>

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

### <span data-ttu-id="a111f-129">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="a111f-129">-InstanceName</span></span>
<span data-ttu-id="a111f-130">A példány neve</span><span class="sxs-lookup"><span data-stu-id="a111f-130">The instance name</span></span>

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

### <span data-ttu-id="a111f-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a111f-131">-InstanceResourceId</span></span>
<span data-ttu-id="a111f-132">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a111f-132">The instance resource id</span></span>

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

### <span data-ttu-id="a111f-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a111f-133">-KeyId</span></span>
<span data-ttu-id="a111f-134">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="a111f-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="a111f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a111f-135">-ResourceGroupName</span></span>
<span data-ttu-id="a111f-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a111f-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="a111f-137">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="a111f-137">-Type</span></span>
<span data-ttu-id="a111f-138">Az Azure SQL-adatbázis átlátszó adattitkosítási Protector típusa.</span><span class="sxs-lookup"><span data-stu-id="a111f-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="a111f-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a111f-139">-Confirm</span></span>
<span data-ttu-id="a111f-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a111f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a111f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a111f-141">-WhatIf</span></span>
<span data-ttu-id="a111f-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a111f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a111f-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a111f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a111f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a111f-144">CommonParameters</span></span>
<span data-ttu-id="a111f-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a111f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a111f-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a111f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a111f-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a111f-147">INPUTS</span></span>

### <span data-ttu-id="a111f-148">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a111f-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="a111f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a111f-149">System.String</span></span>

## <span data-ttu-id="a111f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a111f-150">OUTPUTS</span></span>

### <span data-ttu-id="a111f-151">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="a111f-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="a111f-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a111f-152">NOTES</span></span>

## <span data-ttu-id="a111f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a111f-153">RELATED LINKS</span></span>
