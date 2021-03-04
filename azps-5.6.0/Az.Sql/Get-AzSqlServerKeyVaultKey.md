---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942186"
---
# <span data-ttu-id="f01d9-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f01d9-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f01d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f01d9-102">SYNOPSIS</span></span>
<span data-ttu-id="f01d9-103">Egy SQL-kiszolgáló kulcstárkulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f01d9-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="f01d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f01d9-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f01d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f01d9-105">DESCRIPTION</span></span>
<span data-ttu-id="f01d9-106">A Get-AzSqlServerKeyVaultKey parancsmag információt kap az SQL-kiszolgálón található kulcstárbillentyűkről.</span><span class="sxs-lookup"><span data-stu-id="f01d9-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="f01d9-107">A keyid segítségével megtekintheti a kiszolgálón található összes billentyűt, vagy egy adott kulcsot is megtekinthet.</span><span class="sxs-lookup"><span data-stu-id="f01d9-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="f01d9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f01d9-108">EXAMPLES</span></span>

### <span data-ttu-id="f01d9-109">1. példa: Az összes kulcstárbillentyű lekérte</span><span class="sxs-lookup"><span data-stu-id="f01d9-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f01d9-110">Ez a parancs egy SQL-kiszolgáló összes kulcstárkulcsát lekérte.</span><span class="sxs-lookup"><span data-stu-id="f01d9-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="f01d9-111">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344556778990011122334455667788900 CreationDate : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 009987765544332110099887765544332211 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="f01d9-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="f01d9-112">2. példa: Adott kulcstárkulcs lekérte</span><span class="sxs-lookup"><span data-stu-id="f01d9-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f01d9-113">Ez a parancs lekérte a kulcstárkulcsot "azonosító" azonosítóval, majd tárolja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 azt a $MyServerKeyVaultKey változóban.</span><span class="sxs-lookup"><span data-stu-id="f01d9-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="f01d9-114">A kulcstárról $MyServerKeyVaultKey a tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f01d9-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="f01d9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f01d9-115">PARAMETERS</span></span>

### <span data-ttu-id="f01d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01d9-116">-DefaultProfile</span></span>
<span data-ttu-id="f01d9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f01d9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f01d9-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f01d9-118">-KeyId</span></span>
<span data-ttu-id="f01d9-119">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="f01d9-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f01d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="f01d9-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f01d9-121">The name of the resource group</span></span>

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

### <span data-ttu-id="f01d9-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f01d9-122">-ServerName</span></span>
<span data-ttu-id="f01d9-123">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="f01d9-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f01d9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f01d9-124">-Confirm</span></span>
<span data-ttu-id="f01d9-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f01d9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f01d9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f01d9-126">-WhatIf</span></span>
<span data-ttu-id="f01d9-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f01d9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f01d9-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f01d9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f01d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01d9-129">CommonParameters</span></span>
<span data-ttu-id="f01d9-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f01d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01d9-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f01d9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01d9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f01d9-132">INPUTS</span></span>

### <span data-ttu-id="f01d9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f01d9-133">System.String</span></span>

## <span data-ttu-id="f01d9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f01d9-134">OUTPUTS</span></span>

### <span data-ttu-id="f01d9-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f01d9-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f01d9-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f01d9-136">NOTES</span></span>

## <span data-ttu-id="f01d9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f01d9-137">RELATED LINKS</span></span>

[<span data-ttu-id="f01d9-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f01d9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
