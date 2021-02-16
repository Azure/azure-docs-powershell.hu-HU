---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168707"
---
# <span data-ttu-id="2e365-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2e365-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="2e365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e365-102">SYNOPSIS</span></span>
<span data-ttu-id="2e365-103">Az Átlátszó adattitkosítás (TDE) védelme</span><span class="sxs-lookup"><span data-stu-id="2e365-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="2e365-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e365-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e365-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e365-105">DESCRIPTION</span></span>
<span data-ttu-id="2e365-106">A Get-AzSqlServerTransparentDataEncryptionProtector parancsmag információt kap a TDE-védelemről.</span><span class="sxs-lookup"><span data-stu-id="2e365-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="2e365-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e365-107">EXAMPLES</span></span>

### <span data-ttu-id="2e365-108">1. példa: Az átlátszó adattitkosítás (TDE) védelme</span><span class="sxs-lookup"><span data-stu-id="2e365-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="2e365-109">Ez a parancs a ContosoResourceGroup nevű erőforráscsoportBan a ContosoServer nevű kiszolgáló TDE-védőjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2e365-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="2e365-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="2e365-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="2e365-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="2e365-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="2e365-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e365-112">PARAMETERS</span></span>

### <span data-ttu-id="2e365-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e365-113">-DefaultProfile</span></span>
<span data-ttu-id="2e365-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e365-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e365-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e365-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e365-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2e365-116">The name of the resource group</span></span>

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

### <span data-ttu-id="2e365-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e365-117">-ServerName</span></span>
<span data-ttu-id="2e365-118">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="2e365-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2e365-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e365-119">-Confirm</span></span>
<span data-ttu-id="2e365-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e365-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e365-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e365-121">-WhatIf</span></span>
<span data-ttu-id="2e365-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e365-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e365-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e365-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e365-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e365-124">CommonParameters</span></span>
<span data-ttu-id="2e365-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e365-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e365-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e365-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e365-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e365-127">INPUTS</span></span>

### <span data-ttu-id="2e365-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2e365-128">System.String</span></span>

## <span data-ttu-id="2e365-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e365-129">OUTPUTS</span></span>

### <span data-ttu-id="2e365-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="2e365-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="2e365-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e365-131">NOTES</span></span>

## <span data-ttu-id="2e365-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e365-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e365-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2e365-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
