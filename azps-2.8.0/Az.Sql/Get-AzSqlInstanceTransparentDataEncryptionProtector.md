---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 827c3c3d3cb87fbc3e51b8f083c74af559152115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839184"
---
# <span data-ttu-id="2491c-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2491c-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="2491c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2491c-102">SYNOPSIS</span></span>
<span data-ttu-id="2491c-103">Beolvassa az átlátszó adattitkosítást (TDE) védőt egy SQL-alapú felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="2491c-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="2491c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2491c-104">SYNTAX</span></span>

### <span data-ttu-id="2491c-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2491c-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2491c-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2491c-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2491c-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2491c-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2491c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2491c-108">DESCRIPTION</span></span>
<span data-ttu-id="2491c-109">A Get-AzSqlInstanceTransparentDataEncryptionProtector parancsmag a megadott SQL-kezelt példány TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2491c-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="2491c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2491c-110">EXAMPLES</span></span>

### <span data-ttu-id="2491c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2491c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="2491c-112">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2491c-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2491c-113">2. példa: a Managed instance objektum használata</span><span class="sxs-lookup"><span data-stu-id="2491c-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="2491c-114">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2491c-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2491c-115">3. példa: a felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="2491c-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="2491c-116">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2491c-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2491c-117">Példa 4: csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="2491c-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="2491c-118">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2491c-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="2491c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2491c-119">PARAMETERS</span></span>

### <span data-ttu-id="2491c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2491c-120">-DefaultProfile</span></span>
<span data-ttu-id="2491c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2491c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2491c-122">-Példány</span><span class="sxs-lookup"><span data-stu-id="2491c-122">-Instance</span></span>
<span data-ttu-id="2491c-123">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="2491c-123">The instance input object</span></span>

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

### <span data-ttu-id="2491c-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="2491c-124">-InstanceName</span></span>
<span data-ttu-id="2491c-125">A példány neve</span><span class="sxs-lookup"><span data-stu-id="2491c-125">The instance name</span></span>

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

### <span data-ttu-id="2491c-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="2491c-126">-InstanceResourceId</span></span>
<span data-ttu-id="2491c-127">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="2491c-127">The instance resource id</span></span>

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

### <span data-ttu-id="2491c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2491c-128">-ResourceGroupName</span></span>
<span data-ttu-id="2491c-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2491c-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="2491c-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2491c-130">-Confirm</span></span>
<span data-ttu-id="2491c-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2491c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2491c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2491c-132">-WhatIf</span></span>
<span data-ttu-id="2491c-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2491c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2491c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2491c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2491c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2491c-135">CommonParameters</span></span>
<span data-ttu-id="2491c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2491c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2491c-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2491c-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2491c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2491c-138">INPUTS</span></span>

### <span data-ttu-id="2491c-139">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2491c-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="2491c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2491c-140">System.String</span></span>

## <span data-ttu-id="2491c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2491c-141">OUTPUTS</span></span>

### <span data-ttu-id="2491c-142">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="2491c-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="2491c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2491c-143">NOTES</span></span>

## <span data-ttu-id="2491c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2491c-144">RELATED LINKS</span></span>
