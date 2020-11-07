---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 333e4b1e5f01c76947ca32277fd8ca7ff75218eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672347"
---
# <span data-ttu-id="7de30-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7de30-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="7de30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7de30-102">SYNOPSIS</span></span>
<span data-ttu-id="7de30-103">Kulcs-Vault-kulcs eltávolítása egy SQL Server-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7de30-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7de30-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7de30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7de30-105">DESCRIPTION</span></span>
<span data-ttu-id="7de30-106">A Remove-AzureRmSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóról eltávolítja a Key Vault-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7de30-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="7de30-107">Fontos tudni, hogy az SQL Server-engedélyek a kulcs boltozatára nem változnak.</span><span class="sxs-lookup"><span data-stu-id="7de30-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="7de30-108">Az engedélyek módosításához használja a set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="7de30-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="7de30-109">Ne feledje, hogy ez a parancsmag nem változtatja meg a Key Vault-t.</span><span class="sxs-lookup"><span data-stu-id="7de30-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="7de30-110">Ha el szeretne távolítani egy billentyűt a Key Vault-ról, használja a Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="7de30-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="7de30-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7de30-111">EXAMPLES</span></span>

### <span data-ttu-id="7de30-112">1. példa: kulcs-Vault-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7de30-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7de30-113">Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7de30-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="7de30-114">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="7de30-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="7de30-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7de30-115">PARAMETERS</span></span>

### <span data-ttu-id="7de30-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7de30-116">-AsJob</span></span>
<span data-ttu-id="7de30-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7de30-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="7de30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de30-118">-DefaultProfile</span></span>
<span data-ttu-id="7de30-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7de30-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7de30-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7de30-120">-KeyId</span></span>
<span data-ttu-id="7de30-121">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="7de30-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7de30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de30-122">-ResourceGroupName</span></span>
<span data-ttu-id="7de30-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7de30-123">The name of the resource group</span></span>

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

### <span data-ttu-id="7de30-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7de30-124">-ServerName</span></span>
<span data-ttu-id="7de30-125">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7de30-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7de30-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7de30-126">-Confirm</span></span>
<span data-ttu-id="7de30-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7de30-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de30-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de30-128">-WhatIf</span></span>
<span data-ttu-id="7de30-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7de30-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de30-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7de30-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de30-131">CommonParameters</span></span>
<span data-ttu-id="7de30-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7de30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de30-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de30-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de30-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de30-134">INPUTS</span></span>

### <span data-ttu-id="7de30-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7de30-135">System.String</span></span>

## <span data-ttu-id="7de30-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de30-136">OUTPUTS</span></span>

### <span data-ttu-id="7de30-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="7de30-137">System.Object</span></span>

## <span data-ttu-id="7de30-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7de30-138">NOTES</span></span>

## <span data-ttu-id="7de30-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7de30-139">RELATED LINKS</span></span>

[<span data-ttu-id="7de30-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7de30-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
