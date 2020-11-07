---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8d89b966da0fc9d5f0517c5faf777cb5d16efc33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839287"
---
# <span data-ttu-id="c9eb7-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c9eb7-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c9eb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eb7-103">Módosítja az adatbázis TDE tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="c9eb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9eb7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9eb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eb7-106">A **set-AzSqlDatabaseTransparentDataEncryption** parancsmag módosította az Azure SQL-adatbázisok átlátszó adattitkosítási (TDE) tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="c9eb7-107">További információért olvassa el az átlátszó adattitkosítás az Azure SQL-adatbázisokkal https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) a Microsoft Developer Network Library-ban című témakört).</span><span class="sxs-lookup"><span data-stu-id="c9eb7-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c9eb7-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c9eb7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9eb7-109">EXAMPLES</span></span>

### <span data-ttu-id="c9eb7-110">1. példa: TDE engedélyezése adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="c9eb7-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="c9eb7-111">Ez a parancs engedélyezi a Server01 nevű kiszolgálón a Database01 nevű adatbázis TDE.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c9eb7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9eb7-112">PARAMETERS</span></span>

### <span data-ttu-id="c9eb7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9eb7-113">-DatabaseName</span></span>
<span data-ttu-id="c9eb7-114">Annak az adatbázisnak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c9eb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eb7-115">-DefaultProfile</span></span>
<span data-ttu-id="c9eb7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c9eb7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9eb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9eb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9eb7-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c9eb7-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c9eb7-119">-ServerName</span></span>
<span data-ttu-id="c9eb7-120">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c9eb7-121">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c9eb7-121">-State</span></span>
<span data-ttu-id="c9eb7-122">A TDE tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="c9eb7-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9eb7-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9eb7-124">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c9eb7-124">Enabled</span></span> 
- <span data-ttu-id="c9eb7-125">Tiltva</span><span class="sxs-lookup"><span data-stu-id="c9eb7-125">Disabled</span></span>

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

### <span data-ttu-id="c9eb7-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9eb7-126">-Confirm</span></span>
<span data-ttu-id="c9eb7-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9eb7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9eb7-128">-WhatIf</span></span>
<span data-ttu-id="c9eb7-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9eb7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9eb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eb7-131">CommonParameters</span></span>
<span data-ttu-id="c9eb7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9eb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eb7-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eb7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9eb7-134">INPUTS</span></span>

### <span data-ttu-id="c9eb7-135">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="c9eb7-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="c9eb7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c9eb7-136">System.String</span></span>

## <span data-ttu-id="c9eb7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9eb7-137">OUTPUTS</span></span>

### <span data-ttu-id="c9eb7-138">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c9eb7-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c9eb7-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9eb7-139">NOTES</span></span>

## <span data-ttu-id="c9eb7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9eb7-140">RELATED LINKS</span></span>

[<span data-ttu-id="c9eb7-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c9eb7-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="c9eb7-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c9eb7-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c9eb7-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c9eb7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


