---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: bf82ca7804ecd3f382728217395be234155e9035
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495243"
---
# <span data-ttu-id="6dc33-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6dc33-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="6dc33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6dc33-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc33-103">Kulcs-Vault-kulcsot ad hozzá egy SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="6dc33-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dc33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6dc33-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6dc33-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc33-106">A Add-AzureRmSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóhoz kulcsos boltozatot ad.</span><span class="sxs-lookup"><span data-stu-id="6dc33-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="6dc33-107">A kiszolgálónak "beolvasás, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="6dc33-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="6dc33-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6dc33-108">EXAMPLES</span></span>

### <span data-ttu-id="6dc33-109">Példa 1: kulcs Vault-kulcs hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6dc33-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="6dc33-110">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoServer "nevű SQL Server-azonosítóval rendelkező Key Vault-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="6dc33-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="6dc33-111">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="6dc33-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="6dc33-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6dc33-112">PARAMETERS</span></span>

### <span data-ttu-id="6dc33-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dc33-113">-AsJob</span></span>
<span data-ttu-id="6dc33-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6dc33-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc33-115">-DefaultProfile</span></span>
<span data-ttu-id="6dc33-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6dc33-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6dc33-117">-KeyId</span></span>
<span data-ttu-id="6dc33-118">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="6dc33-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc33-119">-ResourceGroupName</span></span>
<span data-ttu-id="6dc33-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6dc33-120">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6dc33-121">-ServerName</span></span>
<span data-ttu-id="6dc33-122">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6dc33-122">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6dc33-123">-Confirm</span></span>
<span data-ttu-id="6dc33-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6dc33-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc33-125">-WhatIf</span></span>
<span data-ttu-id="6dc33-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6dc33-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc33-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6dc33-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc33-128">CommonParameters</span></span>
<span data-ttu-id="6dc33-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6dc33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc33-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc33-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc33-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dc33-131">INPUTS</span></span>

### <span data-ttu-id="6dc33-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc33-132">System.String</span></span>

## <span data-ttu-id="6dc33-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dc33-133">OUTPUTS</span></span>

### <span data-ttu-id="6dc33-134">Microsoft. Azure. Command. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="6dc33-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="6dc33-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6dc33-135">NOTES</span></span>

## <span data-ttu-id="6dc33-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6dc33-136">RELATED LINKS</span></span>

[<span data-ttu-id="6dc33-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6dc33-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
