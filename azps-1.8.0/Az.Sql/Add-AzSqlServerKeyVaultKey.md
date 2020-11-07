---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669080"
---
# <span data-ttu-id="60fc5-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60fc5-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="60fc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="60fc5-103">Kulcs-Vault-kulcsot ad hozzá egy SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="60fc5-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="60fc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60fc5-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fc5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="60fc5-106">A Add-AzSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóhoz kulcsos boltozatot ad.</span><span class="sxs-lookup"><span data-stu-id="60fc5-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="60fc5-107">A kiszolgálónak "beolvasás, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="60fc5-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="60fc5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="60fc5-108">EXAMPLES</span></span>

### <span data-ttu-id="60fc5-109">Példa 1: kulcs Vault-kulcs hozzáadása</span><span class="sxs-lookup"><span data-stu-id="60fc5-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="60fc5-110">Ez a parancs hozzáadja a " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " ContosoResourceGroup "erőforráscsoport" ContosoServer "nevű SQL Server-azonosítóval rendelkező Key Vault-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="60fc5-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="60fc5-111">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="60fc5-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="60fc5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60fc5-112">PARAMETERS</span></span>

### <span data-ttu-id="60fc5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60fc5-113">-AsJob</span></span>
<span data-ttu-id="60fc5-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="60fc5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60fc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fc5-115">-DefaultProfile</span></span>
<span data-ttu-id="60fc5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="60fc5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60fc5-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="60fc5-117">-KeyId</span></span>
<span data-ttu-id="60fc5-118">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="60fc5-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="60fc5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fc5-119">-ResourceGroupName</span></span>
<span data-ttu-id="60fc5-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="60fc5-120">The name of the resource group</span></span>

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

### <span data-ttu-id="60fc5-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="60fc5-121">-ServerName</span></span>
<span data-ttu-id="60fc5-122">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="60fc5-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="60fc5-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60fc5-123">-Confirm</span></span>
<span data-ttu-id="60fc5-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60fc5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fc5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fc5-125">-WhatIf</span></span>
<span data-ttu-id="60fc5-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60fc5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60fc5-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60fc5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fc5-128">CommonParameters</span></span>
<span data-ttu-id="60fc5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60fc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fc5-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="60fc5-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fc5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60fc5-131">INPUTS</span></span>

### <span data-ttu-id="60fc5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="60fc5-132">System.String</span></span>

## <span data-ttu-id="60fc5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60fc5-133">OUTPUTS</span></span>

### <span data-ttu-id="60fc5-134">Microsoft. Azure. Command. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="60fc5-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="60fc5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60fc5-135">NOTES</span></span>

## <span data-ttu-id="60fc5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60fc5-136">RELATED LINKS</span></span>

[<span data-ttu-id="60fc5-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="60fc5-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
