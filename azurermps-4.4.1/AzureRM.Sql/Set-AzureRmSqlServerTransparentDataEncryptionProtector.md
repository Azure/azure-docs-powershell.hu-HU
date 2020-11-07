---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680737"
---
# <span data-ttu-id="aaeb0-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aaeb0-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="aaeb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aaeb0-102">SYNOPSIS</span></span>
<span data-ttu-id="aaeb0-103">Az áttetsző adattitkosítást (TDE) védőt állítja be egy SQL-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaeb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aaeb0-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaeb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aaeb0-105">DESCRIPTION</span></span>
<span data-ttu-id="aaeb0-106">Az Set-AzureRmSqlServerTransparentDataEncryptionProtector parancsmag az SQL Server TDE-oltalmazóját állítja be.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="aaeb0-107">A TDE Protector típusának módosítása elforgatja a oltalmazót.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="aaeb0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="aaeb0-108">EXAMPLES</span></span>

### <span data-ttu-id="aaeb0-109">--------------------------Példa 1: az átlátszó adattitkosítás (TDE) Protector típusának beállítása az ServiceManaged--------------------------</span><span class="sxs-lookup"><span data-stu-id="aaeb0-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="aaeb0-110">Ez a parancs a kiszolgáló TDE-Protector típusát frissíti a szolgáltatás felügyelt értékére.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="aaeb0-111">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="aaeb0-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="aaeb0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="aaeb0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="aaeb0-113">--------------------------Példa 2: az átlátszó adattitkosítási Protector típusának beállítása az Azure Key Vault--------------------------</span><span class="sxs-lookup"><span data-stu-id="aaeb0-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="aaeb0-114">Ez a parancs frissíti a kiszolgálót, és a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '" TDE Protector néven használja a Server Key Vault azonosítót.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="aaeb0-115">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="aaeb0-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="aaeb0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="aaeb0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="aaeb0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aaeb0-117">PARAMETERS</span></span>

### <span data-ttu-id="aaeb0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aaeb0-118">-Force</span></span>
<span data-ttu-id="aaeb0-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="aaeb0-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aaeb0-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="aaeb0-120">-KeyId</span></span>
<span data-ttu-id="aaeb0-121">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="aaeb0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaeb0-122">-ResourceGroupName</span></span>
<span data-ttu-id="aaeb0-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="aaeb0-123">The name of the resource group</span></span>

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

### <span data-ttu-id="aaeb0-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="aaeb0-124">-ServerName</span></span>
<span data-ttu-id="aaeb0-125">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="aaeb0-126">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="aaeb0-126">-Type</span></span>
<span data-ttu-id="aaeb0-127">Az Azure SQL-adatbázis TDE Protector típusa.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="aaeb0-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aaeb0-128">-Confirm</span></span>
<span data-ttu-id="aaeb0-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaeb0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaeb0-130">-WhatIf</span></span>
<span data-ttu-id="aaeb0-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaeb0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaeb0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaeb0-133">-DefaultProfile</span></span>
<span data-ttu-id="aaeb0-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaeb0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaeb0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaeb0-135">CommonParameters</span></span>
<span data-ttu-id="aaeb0-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aaeb0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaeb0-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaeb0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaeb0-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaeb0-138">INPUTS</span></span>

### <span data-ttu-id="aaeb0-139">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="aaeb0-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="aaeb0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aaeb0-140">System.String</span></span>

## <span data-ttu-id="aaeb0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaeb0-141">OUTPUTS</span></span>

### <span data-ttu-id="aaeb0-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="aaeb0-142">System.Object</span></span>

## <span data-ttu-id="aaeb0-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aaeb0-143">NOTES</span></span>

## <span data-ttu-id="aaeb0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaeb0-144">RELATED LINKS</span></span>

[<span data-ttu-id="aaeb0-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aaeb0-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
