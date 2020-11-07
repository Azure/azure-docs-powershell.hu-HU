---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 4c0f576d118a502b04d4effd9a1de8f98e2a3813
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838743"
---
# <span data-ttu-id="cf11b-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cf11b-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="cf11b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf11b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf11b-103">Kulcs-Vault-kulcs hozzáadása a megadott felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="cf11b-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="cf11b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf11b-104">SYNTAX</span></span>

### <span data-ttu-id="cf11b-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf11b-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf11b-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf11b-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf11b-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf11b-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf11b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf11b-108">DESCRIPTION</span></span>
<span data-ttu-id="cf11b-109">A Add-AzSqlInstanceKeyVaultKey parancsmag a megadott felügyelt példány kulcsát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cf11b-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="cf11b-110">A felügyelt példánynak "beolvasás, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a boltozathoz, az alábbi parancsfájl segítségével adjon engedélyt a felügyelt példányra.</span><span class="sxs-lookup"><span data-stu-id="cf11b-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="cf11b-111">$managedInstance Get-AzSqlInstance = "ContosoManagedInstanceName"-ResourceGroupName ' ContosoResourceGroup ' Set-AzKeyVaultAccessPolicy-VaultName ContosoVault-ObjectId $managedInstance. Identity. PrincipalId-PermissionsToKeys Get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="cf11b-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="cf11b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cf11b-112">EXAMPLES</span></span>

### <span data-ttu-id="cf11b-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf11b-113">Example 1</span></span>
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

<span data-ttu-id="cf11b-114">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoManagedInstanceName "nevű, SQL-alapú," "" nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="cf11b-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cf11b-115">2. példa: a Managed instance objektum használata</span><span class="sxs-lookup"><span data-stu-id="cf11b-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="cf11b-116">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoManagedInstanceName "nevű, SQL-alapú," "" nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="cf11b-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cf11b-117">3. példa: a felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="cf11b-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="cf11b-118">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoManagedInstanceName "nevű, SQL-alapú," "" nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="cf11b-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="cf11b-119">Példa 4: csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="cf11b-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="cf11b-120">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoManagedInstanceName "nevű, SQL-alapú," "" nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="cf11b-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="cf11b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf11b-121">PARAMETERS</span></span>

### <span data-ttu-id="cf11b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf11b-122">-DefaultProfile</span></span>
<span data-ttu-id="cf11b-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf11b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf11b-124">-Példány</span><span class="sxs-lookup"><span data-stu-id="cf11b-124">-Instance</span></span>
<span data-ttu-id="cf11b-125">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="cf11b-125">The instance input object</span></span>

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

### <span data-ttu-id="cf11b-126">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="cf11b-126">-InstanceName</span></span>
<span data-ttu-id="cf11b-127">A példány neve</span><span class="sxs-lookup"><span data-stu-id="cf11b-127">The instance name</span></span>

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

### <span data-ttu-id="cf11b-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cf11b-128">-InstanceResourceId</span></span>
<span data-ttu-id="cf11b-129">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="cf11b-129">The instance resource id</span></span>

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

### <span data-ttu-id="cf11b-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cf11b-130">-KeyId</span></span>
<span data-ttu-id="cf11b-131">AzureKeyVault-kulcs azonosítója</span><span class="sxs-lookup"><span data-stu-id="cf11b-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="cf11b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf11b-132">-ResourceGroupName</span></span>
<span data-ttu-id="cf11b-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cf11b-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="cf11b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf11b-134">-Confirm</span></span>
<span data-ttu-id="cf11b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf11b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf11b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf11b-136">-WhatIf</span></span>
<span data-ttu-id="cf11b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf11b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf11b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf11b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf11b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf11b-139">CommonParameters</span></span>
<span data-ttu-id="cf11b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf11b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf11b-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf11b-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf11b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf11b-142">INPUTS</span></span>

### <span data-ttu-id="cf11b-143">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cf11b-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="cf11b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cf11b-144">System.String</span></span>

## <span data-ttu-id="cf11b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf11b-145">OUTPUTS</span></span>

### <span data-ttu-id="cf11b-146">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="cf11b-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="cf11b-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf11b-147">NOTES</span></span>

## <span data-ttu-id="cf11b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf11b-148">RELATED LINKS</span></span>
