---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504712"
---
# <span data-ttu-id="02271-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02271-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="02271-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02271-102">SYNOPSIS</span></span>
<span data-ttu-id="02271-103">Kulcs-Vault-kulcsot ad hozzá egy SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="02271-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02271-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02271-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02271-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02271-105">DESCRIPTION</span></span>
<span data-ttu-id="02271-106">A Add-AzureRmSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóhoz kulcsos boltozatot ad.</span><span class="sxs-lookup"><span data-stu-id="02271-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="02271-107">A kiszolgálónak "beolvasás, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="02271-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="02271-108">Példák</span><span class="sxs-lookup"><span data-stu-id="02271-108">EXAMPLES</span></span>

### <span data-ttu-id="02271-109">--------------------------Példa 1: kulcs Vault-kulcs hozzáadása--------------------------</span><span class="sxs-lookup"><span data-stu-id="02271-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="02271-110">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoServer "nevű SQL Server-azonosítóval rendelkező Key Vault-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="02271-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="02271-111">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="02271-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="02271-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02271-112">PARAMETERS</span></span>

### <span data-ttu-id="02271-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="02271-113">-KeyId</span></span>
<span data-ttu-id="02271-114">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="02271-114">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02271-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02271-115">-ResourceGroupName</span></span>
<span data-ttu-id="02271-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="02271-116">The name of the resource group</span></span>

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

### <span data-ttu-id="02271-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="02271-117">-ServerName</span></span>
<span data-ttu-id="02271-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="02271-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="02271-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02271-119">-Confirm</span></span>
<span data-ttu-id="02271-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02271-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02271-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02271-121">-WhatIf</span></span>
<span data-ttu-id="02271-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02271-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02271-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02271-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02271-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02271-124">-DefaultProfile</span></span>
<span data-ttu-id="02271-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02271-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02271-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02271-126">CommonParameters</span></span>
<span data-ttu-id="02271-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02271-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02271-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02271-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02271-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02271-129">INPUTS</span></span>

### <span data-ttu-id="02271-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02271-130">System.String</span></span>

## <span data-ttu-id="02271-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02271-131">OUTPUTS</span></span>

### <span data-ttu-id="02271-132">Microsoft. Azure. Command. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="02271-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="02271-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02271-133">NOTES</span></span>

## <span data-ttu-id="02271-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02271-134">RELATED LINKS</span></span>

[<span data-ttu-id="02271-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="02271-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
