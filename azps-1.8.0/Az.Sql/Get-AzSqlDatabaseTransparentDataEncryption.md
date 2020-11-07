---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 4dd5a90bcd20cccf605b7c831c02893e43b32ba9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669007"
---
# <span data-ttu-id="0ba2a-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0ba2a-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="0ba2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ba2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba2a-103">Az adatbázis TDE állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="0ba2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ba2a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ba2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ba2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba2a-106">A **Get-AzSqlDatabaseTransparentDataEncryption** parancsmag az Azure SQL-adatbázisok átlátszó adattitkosításának (TDE) állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="0ba2a-107">További információért olvassa el az átlátszó adattitkosítás az Azure SQL-adatbázisokkal https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) a Microsoft Developer Network Library-ban című témakört).</span><span class="sxs-lookup"><span data-stu-id="0ba2a-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="0ba2a-108">Ez a parancsmag a TDE jelenlegi állapotát kapja meg, de a titkosítás és a visszafejtés egyaránt hosszú műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="0ba2a-109">A titkosítási vizsgálat előrehaladásának megtekintéséhez futtassa az Get-AzSqlDatabaseTransparentDataEncryptionActivity parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="0ba2a-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0ba2a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0ba2a-111">EXAMPLES</span></span>

### <span data-ttu-id="0ba2a-112">Példa 1: TDE állapotának beszerzése egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="0ba2a-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="0ba2a-113">Ez a parancs a server01 nevű kiszolgálón a Database01 nevű adatbázis TDE állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="0ba2a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ba2a-114">PARAMETERS</span></span>

### <span data-ttu-id="0ba2a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0ba2a-115">-DatabaseName</span></span>
<span data-ttu-id="0ba2a-116">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a TDE állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="0ba2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba2a-117">-DefaultProfile</span></span>
<span data-ttu-id="0ba2a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ba2a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ba2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ba2a-120">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0ba2a-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0ba2a-121">-ServerName</span></span>
<span data-ttu-id="0ba2a-122">Itt adhatja meg annak az adatbázisnak a nevét, amelynek a parancsmagja a TDE állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="0ba2a-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ba2a-123">-Confirm</span></span>
<span data-ttu-id="0ba2a-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ba2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ba2a-125">-WhatIf</span></span>
<span data-ttu-id="0ba2a-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ba2a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ba2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba2a-128">CommonParameters</span></span>
<span data-ttu-id="0ba2a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ba2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba2a-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ba2a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba2a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba2a-131">INPUTS</span></span>

### <span data-ttu-id="0ba2a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba2a-132">System.String</span></span>

## <span data-ttu-id="0ba2a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba2a-133">OUTPUTS</span></span>

### <span data-ttu-id="0ba2a-134">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="0ba2a-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="0ba2a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ba2a-135">NOTES</span></span>

## <span data-ttu-id="0ba2a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ba2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="0ba2a-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="0ba2a-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="0ba2a-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0ba2a-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
