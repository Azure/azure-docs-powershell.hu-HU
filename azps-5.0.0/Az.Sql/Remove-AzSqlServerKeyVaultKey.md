---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186520"
---
# <span data-ttu-id="23bab-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23bab-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="23bab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23bab-102">SYNOPSIS</span></span>
<span data-ttu-id="23bab-103">Kulcs-Vault-kulcs eltávolítása egy SQL Server-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="23bab-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="23bab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23bab-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23bab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23bab-105">DESCRIPTION</span></span>
<span data-ttu-id="23bab-106">A Remove-AzSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóról eltávolítja a Key Vault-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="23bab-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="23bab-107">Fontos tudni, hogy az SQL Server-engedélyek a kulcs boltozatára nem változnak.</span><span class="sxs-lookup"><span data-stu-id="23bab-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="23bab-108">Az engedélyek módosításához használja a set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="23bab-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="23bab-109">Ne feledje, hogy ez a parancsmag nem változtatja meg a Key Vault-t.</span><span class="sxs-lookup"><span data-stu-id="23bab-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="23bab-110">Ha el szeretne távolítani egy billentyűt a Key Vault-ról, használja a Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="23bab-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="23bab-111">Példák</span><span class="sxs-lookup"><span data-stu-id="23bab-111">EXAMPLES</span></span>

### <span data-ttu-id="23bab-112">1. példa: kulcs-Vault-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="23bab-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="23bab-113">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="23bab-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="23bab-114">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="23bab-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="23bab-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23bab-115">PARAMETERS</span></span>

### <span data-ttu-id="23bab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23bab-116">-AsJob</span></span>
<span data-ttu-id="23bab-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="23bab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23bab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23bab-118">-DefaultProfile</span></span>
<span data-ttu-id="23bab-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23bab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23bab-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="23bab-120">-KeyId</span></span>
<span data-ttu-id="23bab-121">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="23bab-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="23bab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23bab-122">-ResourceGroupName</span></span>
<span data-ttu-id="23bab-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="23bab-123">The name of the resource group</span></span>

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

### <span data-ttu-id="23bab-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="23bab-124">-ServerName</span></span>
<span data-ttu-id="23bab-125">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="23bab-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="23bab-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23bab-126">-Confirm</span></span>
<span data-ttu-id="23bab-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23bab-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23bab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23bab-128">-WhatIf</span></span>
<span data-ttu-id="23bab-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23bab-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23bab-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23bab-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23bab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bab-131">CommonParameters</span></span>
<span data-ttu-id="23bab-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23bab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bab-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23bab-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bab-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23bab-134">INPUTS</span></span>

### <span data-ttu-id="23bab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="23bab-135">System.String</span></span>

## <span data-ttu-id="23bab-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23bab-136">OUTPUTS</span></span>

### <span data-ttu-id="23bab-137">Microsoft. Azure. Command. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="23bab-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="23bab-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23bab-138">NOTES</span></span>

## <span data-ttu-id="23bab-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23bab-139">RELATED LINKS</span></span>

[<span data-ttu-id="23bab-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="23bab-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)