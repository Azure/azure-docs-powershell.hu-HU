---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375562"
---
# <span data-ttu-id="717a7-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="717a7-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="717a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="717a7-102">SYNOPSIS</span></span>
<span data-ttu-id="717a7-103">Hozzáad egy kulcstárkulcsot egy SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="717a7-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="717a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="717a7-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="717a7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="717a7-105">DESCRIPTION</span></span>
<span data-ttu-id="717a7-106">A Add-AzSqlServerKeyVaultKey parancsmag hozzáad egy kulcskulcsot a megadott SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="717a7-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="717a7-107">A kiszolgálónak "get, wrapKey, unwrapKey" engedéllyel kell rendelkeznie a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="717a7-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="717a7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="717a7-108">EXAMPLES</span></span>

### <span data-ttu-id="717a7-109">1. példa: Kulcstár kulcs hozzáadása</span><span class="sxs-lookup"><span data-stu-id="717a7-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="717a7-110">Ez a parancs hozzáadja a "ContosoResourceGroup" erőforráscsoportban a "ContosoServer" nevű SQL-kiszolgálóhoz az Azonosító ' azonosítóval együtt https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 a kulcstárkulcsot.</span><span class="sxs-lookup"><span data-stu-id="717a7-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="717a7-111">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344556778990011122334455667788900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="717a7-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="717a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="717a7-112">PARAMETERS</span></span>

### <span data-ttu-id="717a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="717a7-113">-AsJob</span></span>
<span data-ttu-id="717a7-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="717a7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="717a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717a7-115">-DefaultProfile</span></span>
<span data-ttu-id="717a7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="717a7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="717a7-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="717a7-117">-KeyId</span></span>
<span data-ttu-id="717a7-118">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="717a7-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="717a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="717a7-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="717a7-120">The name of the resource group</span></span>

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

### <span data-ttu-id="717a7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="717a7-121">-ServerName</span></span>
<span data-ttu-id="717a7-122">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="717a7-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="717a7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="717a7-123">-Confirm</span></span>
<span data-ttu-id="717a7-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="717a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717a7-125">-WhatIf</span></span>
<span data-ttu-id="717a7-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="717a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717a7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="717a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717a7-128">CommonParameters</span></span>
<span data-ttu-id="717a7-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717a7-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="717a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717a7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="717a7-131">INPUTS</span></span>

### <span data-ttu-id="717a7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="717a7-132">System.String</span></span>

## <span data-ttu-id="717a7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="717a7-133">OUTPUTS</span></span>

### <span data-ttu-id="717a7-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="717a7-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="717a7-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="717a7-135">NOTES</span></span>

## <span data-ttu-id="717a7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="717a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="717a7-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="717a7-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
