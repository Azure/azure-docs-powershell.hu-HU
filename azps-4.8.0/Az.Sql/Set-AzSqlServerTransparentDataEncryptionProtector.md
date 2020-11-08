---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183853"
---
# <span data-ttu-id="3d988-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3d988-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="3d988-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d988-102">SYNOPSIS</span></span>
<span data-ttu-id="3d988-103">Az áttetsző adattitkosítást (TDE) védőt állítja be egy SQL-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="3d988-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="3d988-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d988-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d988-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d988-105">DESCRIPTION</span></span>
<span data-ttu-id="3d988-106">Az Set-AzSqlServerTransparentDataEncryptionProtector parancsmag az SQL Server TDE-oltalmazóját állítja be.</span><span class="sxs-lookup"><span data-stu-id="3d988-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="3d988-107">A TDE Protector típusának módosítása elforgatja a oltalmazót.</span><span class="sxs-lookup"><span data-stu-id="3d988-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="3d988-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3d988-108">EXAMPLES</span></span>

### <span data-ttu-id="3d988-109">1. példa: az átlátszó adattitkosítás (TDE) Protector típusának beállítása az ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="3d988-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="3d988-110">Ez a parancs a kiszolgáló TDE-Protector típusát frissíti a szolgáltatás felügyelt értékére.</span><span class="sxs-lookup"><span data-stu-id="3d988-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="3d988-111">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="3d988-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="3d988-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="3d988-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="3d988-113">2. példa: az átlátszó adattitkosítási Protector típus beállítása az Azure Key Vault szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="3d988-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="3d988-114">Ez a parancs frissíti a kiszolgálót, és a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" TDE Protector néven használja a Server Key Vault azonosítót.</span><span class="sxs-lookup"><span data-stu-id="3d988-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="3d988-115">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="3d988-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="3d988-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="3d988-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="3d988-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d988-117">PARAMETERS</span></span>

### <span data-ttu-id="3d988-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d988-118">-AsJob</span></span>
<span data-ttu-id="3d988-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d988-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d988-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d988-120">-DefaultProfile</span></span>
<span data-ttu-id="3d988-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d988-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d988-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3d988-122">-Force</span></span>
<span data-ttu-id="3d988-123">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="3d988-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3d988-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3d988-124">-KeyId</span></span>
<span data-ttu-id="3d988-125">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="3d988-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="3d988-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d988-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d988-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3d988-127">The name of the resource group</span></span>

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

### <span data-ttu-id="3d988-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3d988-128">-ServerName</span></span>
<span data-ttu-id="3d988-129">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3d988-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3d988-130">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="3d988-130">-Type</span></span>
<span data-ttu-id="3d988-131">Az Azure SQL-adatbázis TDE Protector típusa.</span><span class="sxs-lookup"><span data-stu-id="3d988-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="3d988-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d988-132">-Confirm</span></span>
<span data-ttu-id="3d988-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d988-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d988-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d988-134">-WhatIf</span></span>
<span data-ttu-id="3d988-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d988-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d988-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d988-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d988-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d988-137">CommonParameters</span></span>
<span data-ttu-id="3d988-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d988-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d988-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d988-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d988-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d988-140">INPUTS</span></span>

### <span data-ttu-id="3d988-141">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="3d988-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="3d988-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3d988-142">System.String</span></span>

## <span data-ttu-id="3d988-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d988-143">OUTPUTS</span></span>

### <span data-ttu-id="3d988-144">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="3d988-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="3d988-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d988-145">NOTES</span></span>

## <span data-ttu-id="3d988-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d988-146">RELATED LINKS</span></span>

[<span data-ttu-id="3d988-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3d988-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
