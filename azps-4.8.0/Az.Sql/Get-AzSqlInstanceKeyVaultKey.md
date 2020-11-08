---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183243"
---
# <span data-ttu-id="204b1-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="204b1-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="204b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="204b1-102">SYNOPSIS</span></span>
<span data-ttu-id="204b1-103">SQL-alapú felügyelt példány fő kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="204b1-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="204b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="204b1-104">SYNTAX</span></span>

### <span data-ttu-id="204b1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="204b1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="204b1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="204b1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="204b1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="204b1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="204b1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="204b1-108">DESCRIPTION</span></span>
<span data-ttu-id="204b1-109">Az Get-AzSqlInstanceKeyVaultKey parancsmag információt kap az SQL-alapú felügyelt példány fő boltozati kulcsairól.</span><span class="sxs-lookup"><span data-stu-id="204b1-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="204b1-110">A felügyelt példány összes kulcsát megtekintheti, vagy megtekintheti az adott kulcsot a KeyId.</span><span class="sxs-lookup"><span data-stu-id="204b1-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="204b1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="204b1-111">EXAMPLES</span></span>

### <span data-ttu-id="204b1-112">1. példa: az összes kulcsos Vault-kulcs beolvasása</span><span class="sxs-lookup"><span data-stu-id="204b1-112">Example 1: Get all Key Vault keys</span></span>
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

<span data-ttu-id="204b1-113">Ez a parancs beilleszti az SQL-kezelt példány összes kulcsát.</span><span class="sxs-lookup"><span data-stu-id="204b1-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="204b1-114">2. példa: adott kulcsos Vault-kulcs beszerzése</span><span class="sxs-lookup"><span data-stu-id="204b1-114">Example 2: Get a specific Key Vault key</span></span>
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

<span data-ttu-id="204b1-115">Ez a parancs a Key Vault-kulcsot azonosító ' ' értékkel kapja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="204b1-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="204b1-116">3. példa: instance objektum használata</span><span class="sxs-lookup"><span data-stu-id="204b1-116">Example 3: Using instance object</span></span>
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

<span data-ttu-id="204b1-117">Ez a parancs a Key Vault-kulcsot azonosító ' ' értékkel kapja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="204b1-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="204b1-118">4. példa: példány-erőforrás azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="204b1-118">Example 4: Using instance resource id</span></span>
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

<span data-ttu-id="204b1-119">Ez a parancs a Key Vault-kulcsot azonosító ' ' értékkel kapja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="204b1-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="204b1-120">Példa 5: csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="204b1-120">Example 5: Using piping</span></span>
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

<span data-ttu-id="204b1-121">Ez a parancs a Key Vault-kulcsot azonosító ' ' értékkel kapja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="204b1-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="204b1-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="204b1-122">PARAMETERS</span></span>

### <span data-ttu-id="204b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204b1-123">-DefaultProfile</span></span>
<span data-ttu-id="204b1-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="204b1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204b1-125">-Példány</span><span class="sxs-lookup"><span data-stu-id="204b1-125">-Instance</span></span>
<span data-ttu-id="204b1-126">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="204b1-126">The instance input object</span></span>

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

### <span data-ttu-id="204b1-127">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="204b1-127">-InstanceName</span></span>
<span data-ttu-id="204b1-128">A példány neve</span><span class="sxs-lookup"><span data-stu-id="204b1-128">The instance name</span></span>

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

### <span data-ttu-id="204b1-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="204b1-129">-InstanceResourceId</span></span>
<span data-ttu-id="204b1-130">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="204b1-130">The instance resource id</span></span>

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

### <span data-ttu-id="204b1-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="204b1-131">-KeyId</span></span>
<span data-ttu-id="204b1-132">AzureKeyVault-kulcs azonosítója</span><span class="sxs-lookup"><span data-stu-id="204b1-132">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="204b1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="204b1-133">-ResourceGroupName</span></span>
<span data-ttu-id="204b1-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="204b1-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="204b1-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="204b1-135">-Confirm</span></span>
<span data-ttu-id="204b1-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="204b1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204b1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204b1-137">-WhatIf</span></span>
<span data-ttu-id="204b1-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="204b1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="204b1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="204b1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204b1-140">CommonParameters</span></span>
<span data-ttu-id="204b1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="204b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204b1-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="204b1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204b1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="204b1-143">INPUTS</span></span>

### <span data-ttu-id="204b1-144">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="204b1-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="204b1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="204b1-145">System.String</span></span>

## <span data-ttu-id="204b1-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="204b1-146">OUTPUTS</span></span>

### <span data-ttu-id="204b1-147">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="204b1-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="204b1-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="204b1-148">NOTES</span></span>

## <span data-ttu-id="204b1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="204b1-149">RELATED LINKS</span></span>
