---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158219"
---
# <span data-ttu-id="16374-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="16374-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="16374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16374-102">SYNOPSIS</span></span>
<span data-ttu-id="16374-103">Az átlátszó adattitkosítás (TDE) védelmét állítja be egy SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="16374-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="16374-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16374-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16374-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16374-105">DESCRIPTION</span></span>
<span data-ttu-id="16374-106">A Set-AzSqlServerTransparentDataEncryptionProtector parancsmag beállítja egy SQL-kiszolgáló TDE-védelmét.</span><span class="sxs-lookup"><span data-stu-id="16374-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="16374-107">A TDE-védelem típusának módosítása elforgatja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="16374-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="16374-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16374-108">EXAMPLES</span></span>

### <span data-ttu-id="16374-109">1. példa: Az Átlátszó adattitkosítás (TDE) protector típusának beállítása ServiceManaged típusra</span><span class="sxs-lookup"><span data-stu-id="16374-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="16374-110">Ez a parancs szolgáltatás által felügyelt szolgáltatásra frissíti a kiszolgáló TDE-védelem típusát.</span><span class="sxs-lookup"><span data-stu-id="16374-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="16374-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="16374-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="16374-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="16374-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="16374-113">2. példa: Az áttetsző adattitkosítási védelem típusának beállítása Azure-kulcstárra</span><span class="sxs-lookup"><span data-stu-id="16374-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="16374-114">Ez a parancs frissíti a kiszolgálót úgy, hogy a kiszolgálókulcs-tároló kulcsát tDE-védelemként használja az https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Azonosító ' azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="16374-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="16374-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="16374-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="16374-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="16374-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="16374-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16374-117">PARAMETERS</span></span>

### <span data-ttu-id="16374-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16374-118">-AsJob</span></span>
<span data-ttu-id="16374-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="16374-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16374-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16374-120">-DefaultProfile</span></span>
<span data-ttu-id="16374-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16374-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16374-122">-Force</span><span class="sxs-lookup"><span data-stu-id="16374-122">-Force</span></span>
<span data-ttu-id="16374-123">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="16374-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="16374-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="16374-124">-KeyId</span></span>
<span data-ttu-id="16374-125">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="16374-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16374-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16374-126">-ResourceGroupName</span></span>
<span data-ttu-id="16374-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="16374-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16374-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16374-128">-ServerName</span></span>
<span data-ttu-id="16374-129">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="16374-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16374-130">-Type</span><span class="sxs-lookup"><span data-stu-id="16374-130">-Type</span></span>
<span data-ttu-id="16374-131">Az Azure Sql Database TDE-védelem típusa.</span><span class="sxs-lookup"><span data-stu-id="16374-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16374-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16374-132">-Confirm</span></span>
<span data-ttu-id="16374-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="16374-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16374-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16374-134">-WhatIf</span></span>
<span data-ttu-id="16374-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="16374-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16374-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16374-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16374-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16374-137">CommonParameters</span></span>
<span data-ttu-id="16374-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16374-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16374-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16374-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16374-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16374-140">INPUTS</span></span>

### <span data-ttu-id="16374-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="16374-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="16374-142">System.String</span><span class="sxs-lookup"><span data-stu-id="16374-142">System.String</span></span>

## <span data-ttu-id="16374-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16374-143">OUTPUTS</span></span>

### <span data-ttu-id="16374-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="16374-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="16374-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16374-145">NOTES</span></span>

## <span data-ttu-id="16374-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16374-146">RELATED LINKS</span></span>

[<span data-ttu-id="16374-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="16374-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
