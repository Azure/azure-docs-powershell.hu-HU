---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465983"
---
# <span data-ttu-id="cc11e-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="cc11e-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="cc11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc11e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc11e-103">Módosítja egy adatbázis TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="cc11e-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="cc11e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc11e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc11e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc11e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc11e-106">A **Set-AzSqlDatabaseTransparentDataEncryption** parancsmag módosítja egy Azure SQL-adatbázis TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="cc11e-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="cc11e-107">További információt az Átlátszó adattitkosítás az Azure SQL-adatbázissal https://msdn.microsoft.com/library/dn948096 ( a Microsoft Developer Network Library https://msdn.microsoft.com/library/dn948096) webhelyén) című cikk tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cc11e-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="cc11e-108">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="cc11e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cc11e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc11e-109">EXAMPLES</span></span>

### <span data-ttu-id="cc11e-110">1. példa: TDE engedélyezése adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="cc11e-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="cc11e-111">Ez a parancs engedélyezi a TDE-t a Database01 nevű adatbázishoz a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="cc11e-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="cc11e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc11e-112">PARAMETERS</span></span>

### <span data-ttu-id="cc11e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc11e-113">-DatabaseName</span></span>
<span data-ttu-id="cc11e-114">Annak az adatbázisnak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc11e-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc11e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc11e-115">-DefaultProfile</span></span>
<span data-ttu-id="cc11e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cc11e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc11e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc11e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc11e-118">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cc11e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cc11e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc11e-119">-ServerName</span></span>
<span data-ttu-id="cc11e-120">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc11e-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="cc11e-121">-State</span><span class="sxs-lookup"><span data-stu-id="cc11e-121">-State</span></span>
<span data-ttu-id="cc11e-122">A TDE tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc11e-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="cc11e-123">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cc11e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc11e-124">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="cc11e-124">Enabled</span></span> 
- <span data-ttu-id="cc11e-125">Letiltva</span><span class="sxs-lookup"><span data-stu-id="cc11e-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc11e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc11e-126">-Confirm</span></span>
<span data-ttu-id="cc11e-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc11e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc11e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc11e-128">-WhatIf</span></span>
<span data-ttu-id="cc11e-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc11e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc11e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc11e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc11e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc11e-131">CommonParameters</span></span>
<span data-ttu-id="cc11e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc11e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc11e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc11e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc11e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc11e-134">INPUTS</span></span>

### <span data-ttu-id="cc11e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="cc11e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="cc11e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cc11e-136">System.String</span></span>

## <span data-ttu-id="cc11e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc11e-137">OUTPUTS</span></span>

### <span data-ttu-id="cc11e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="cc11e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="cc11e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc11e-139">NOTES</span></span>

## <span data-ttu-id="cc11e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc11e-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc11e-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="cc11e-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="cc11e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="cc11e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="cc11e-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cc11e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


