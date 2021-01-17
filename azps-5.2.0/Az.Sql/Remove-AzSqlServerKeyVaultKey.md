---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322695"
---
# <span data-ttu-id="71938-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71938-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="71938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71938-102">SYNOPSIS</span></span>
<span data-ttu-id="71938-103">Eltávolít egy kulcstárkulcsot egy SQL-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="71938-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="71938-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71938-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71938-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71938-105">DESCRIPTION</span></span>
<span data-ttu-id="71938-106">A Remove-AzSqlServerKeyVaultKey parancsmag eltávolítja a kulcstár kulcsát a megadott SQL-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="71938-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="71938-107">Ne feledje, hogy az SQL-kiszolgálónak a kulcs tárolóhoz való engedélyei nem változnak.</span><span class="sxs-lookup"><span data-stu-id="71938-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="71938-108">Az engedélyeket a Set-AzKeyVaultAccessPolicy segítségével módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="71938-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="71938-109">Ne feledje, hogy ez a parancsmag nem módosítja a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="71938-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="71938-110">Ha el szeretne távolítani egy kulcsot a kulcstárból, használja a Remove-AzKeyVaultKey billentyűt.</span><span class="sxs-lookup"><span data-stu-id="71938-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="71938-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71938-111">EXAMPLES</span></span>

### <span data-ttu-id="71938-112">1. példa: Kulcstár kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="71938-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="71938-113">Ez a parancs eltávolítja a "" azonosítójú kulcskulcsot https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a megadott kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="71938-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="71938-114">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344556778990011122334455667788900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="71938-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="71938-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71938-115">PARAMETERS</span></span>

### <span data-ttu-id="71938-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71938-116">-AsJob</span></span>
<span data-ttu-id="71938-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71938-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71938-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71938-118">-DefaultProfile</span></span>
<span data-ttu-id="71938-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="71938-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71938-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="71938-120">-KeyId</span></span>
<span data-ttu-id="71938-121">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="71938-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="71938-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71938-122">-ResourceGroupName</span></span>
<span data-ttu-id="71938-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="71938-123">The name of the resource group</span></span>

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

### <span data-ttu-id="71938-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71938-124">-ServerName</span></span>
<span data-ttu-id="71938-125">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="71938-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="71938-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71938-126">-Confirm</span></span>
<span data-ttu-id="71938-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71938-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71938-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71938-128">-WhatIf</span></span>
<span data-ttu-id="71938-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71938-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71938-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71938-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71938-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71938-131">CommonParameters</span></span>
<span data-ttu-id="71938-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71938-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71938-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71938-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71938-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71938-134">INPUTS</span></span>

### <span data-ttu-id="71938-135">System.String</span><span class="sxs-lookup"><span data-stu-id="71938-135">System.String</span></span>

## <span data-ttu-id="71938-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71938-136">OUTPUTS</span></span>

### <span data-ttu-id="71938-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="71938-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="71938-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71938-138">NOTES</span></span>

## <span data-ttu-id="71938-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71938-139">RELATED LINKS</span></span>

[<span data-ttu-id="71938-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="71938-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
