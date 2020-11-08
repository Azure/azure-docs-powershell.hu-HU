---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185828"
---
# <span data-ttu-id="41f22-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="41f22-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="41f22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41f22-102">SYNOPSIS</span></span>
<span data-ttu-id="41f22-103">Beolvassa az átlátszó adattitkosítást (TDE) védőt egy SQL-alapú felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="41f22-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="41f22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41f22-104">SYNTAX</span></span>

### <span data-ttu-id="41f22-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41f22-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41f22-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41f22-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41f22-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41f22-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f22-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="41f22-108">DESCRIPTION</span></span>
<span data-ttu-id="41f22-109">A Get-AzSqlInstanceTransparentDataEncryptionProtector parancsmag a megadott SQL-kezelt példány TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41f22-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="41f22-110">Példák</span><span class="sxs-lookup"><span data-stu-id="41f22-110">EXAMPLES</span></span>

### <span data-ttu-id="41f22-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="41f22-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="41f22-112">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41f22-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="41f22-113">2. példa: a Managed instance objektum használata</span><span class="sxs-lookup"><span data-stu-id="41f22-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="41f22-114">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41f22-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="41f22-115">3. példa: a felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="41f22-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="41f22-116">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41f22-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="41f22-117">Példa 4: csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="41f22-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="41f22-118">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport ContosoManagedInstanceName nevű TDE-oltalmazóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41f22-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="41f22-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41f22-119">PARAMETERS</span></span>

### <span data-ttu-id="41f22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f22-120">-DefaultProfile</span></span>
<span data-ttu-id="41f22-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41f22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f22-122">-Példány</span><span class="sxs-lookup"><span data-stu-id="41f22-122">-Instance</span></span>
<span data-ttu-id="41f22-123">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="41f22-123">The instance input object</span></span>

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

### <span data-ttu-id="41f22-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="41f22-124">-InstanceName</span></span>
<span data-ttu-id="41f22-125">A példány neve</span><span class="sxs-lookup"><span data-stu-id="41f22-125">The instance name</span></span>

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

### <span data-ttu-id="41f22-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="41f22-126">-InstanceResourceId</span></span>
<span data-ttu-id="41f22-127">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="41f22-127">The instance resource id</span></span>

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

### <span data-ttu-id="41f22-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f22-128">-ResourceGroupName</span></span>
<span data-ttu-id="41f22-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="41f22-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="41f22-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41f22-130">-Confirm</span></span>
<span data-ttu-id="41f22-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41f22-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f22-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f22-132">-WhatIf</span></span>
<span data-ttu-id="41f22-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41f22-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f22-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41f22-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f22-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f22-135">CommonParameters</span></span>
<span data-ttu-id="41f22-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41f22-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f22-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41f22-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f22-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41f22-138">INPUTS</span></span>

### <span data-ttu-id="41f22-139">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="41f22-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="41f22-140">System. String</span><span class="sxs-lookup"><span data-stu-id="41f22-140">System.String</span></span>

## <span data-ttu-id="41f22-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41f22-141">OUTPUTS</span></span>

### <span data-ttu-id="41f22-142">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="41f22-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="41f22-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41f22-143">NOTES</span></span>

## <span data-ttu-id="41f22-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41f22-144">RELATED LINKS</span></span>
