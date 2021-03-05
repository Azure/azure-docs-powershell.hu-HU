---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 98538ba503b1fa31ae4c14897d56b0e0b9daffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999302"
---
# <span data-ttu-id="19dfd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="19dfd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="19dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="19dfd-103">Az SQL által felügyelt példány átlátszó adattitkosítási (TDE) védelemre van bevéve.</span><span class="sxs-lookup"><span data-stu-id="19dfd-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="19dfd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19dfd-104">SYNTAX</span></span>

### <span data-ttu-id="19dfd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19dfd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dfd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dfd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dfd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dfd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dfd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="19dfd-109">A Get-AzSqlInstanceTransparentDataEncryptionProtector parancsmag megkapja a TDE-védelmet a megadott SQL felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="19dfd-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="19dfd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19dfd-110">EXAMPLES</span></span>

### <span data-ttu-id="19dfd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="19dfd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="19dfd-112">Ez a parancs a ContosoResourceGroup nevű erőforráscsoportban a ContosoManagedInstanceName nevű felügyelt példány TDE-védelem szolgáltatását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dfd-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="19dfd-113">2. példa: Felügyelt példány objektum használata</span><span class="sxs-lookup"><span data-stu-id="19dfd-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="19dfd-114">Ez a parancs a ContosoResourceGroup nevű erőforráscsoportban a ContosoManagedInstanceName nevű felügyelt példány TDE-védelem szolgáltatását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dfd-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="19dfd-115">3. példa: Felügyelt példány erőforrás-azonosítójának használata</span><span class="sxs-lookup"><span data-stu-id="19dfd-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="19dfd-116">Ez a parancs a ContosoResourceGroup nevű erőforráscsoportban a ContosoManagedInstanceName nevű felügyelt példány TDE-védelem szolgáltatását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dfd-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="19dfd-117">4. példa: Pipázás használata</span><span class="sxs-lookup"><span data-stu-id="19dfd-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="19dfd-118">Ez a parancs a ContosoResourceGroup nevű erőforráscsoportban a ContosoManagedInstanceName nevű felügyelt példány TDE-védelem szolgáltatását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dfd-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="19dfd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19dfd-119">PARAMETERS</span></span>

### <span data-ttu-id="19dfd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dfd-120">-DefaultProfile</span></span>
<span data-ttu-id="19dfd-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19dfd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19dfd-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="19dfd-122">-Instance</span></span>
<span data-ttu-id="19dfd-123">A példány bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="19dfd-123">The instance input object</span></span>

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

### <span data-ttu-id="19dfd-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="19dfd-124">-InstanceName</span></span>
<span data-ttu-id="19dfd-125">A példány neve</span><span class="sxs-lookup"><span data-stu-id="19dfd-125">The instance name</span></span>

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

### <span data-ttu-id="19dfd-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="19dfd-126">-InstanceResourceId</span></span>
<span data-ttu-id="19dfd-127">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="19dfd-127">The instance resource id</span></span>

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

### <span data-ttu-id="19dfd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dfd-128">-ResourceGroupName</span></span>
<span data-ttu-id="19dfd-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="19dfd-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="19dfd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19dfd-130">-Confirm</span></span>
<span data-ttu-id="19dfd-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19dfd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19dfd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dfd-132">-WhatIf</span></span>
<span data-ttu-id="19dfd-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19dfd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19dfd-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19dfd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19dfd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dfd-135">CommonParameters</span></span>
<span data-ttu-id="19dfd-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dfd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dfd-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19dfd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dfd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19dfd-138">INPUTS</span></span>

### <span data-ttu-id="19dfd-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="19dfd-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="19dfd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="19dfd-140">System.String</span></span>

## <span data-ttu-id="19dfd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19dfd-141">OUTPUTS</span></span>

### <span data-ttu-id="19dfd-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="19dfd-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="19dfd-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19dfd-143">NOTES</span></span>

## <span data-ttu-id="19dfd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19dfd-144">RELATED LINKS</span></span>
