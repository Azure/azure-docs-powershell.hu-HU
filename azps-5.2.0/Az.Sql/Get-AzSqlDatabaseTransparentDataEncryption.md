---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371977"
---
# <span data-ttu-id="e4746-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="e4746-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="e4746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4746-102">SYNOPSIS</span></span>
<span data-ttu-id="e4746-103">Egy adatbázis TDE-állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e4746-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="e4746-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4746-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4746-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4746-105">DESCRIPTION</span></span>
<span data-ttu-id="e4746-106">A **Get-AzSqlDatabaseTransparentDataEncryption** parancsmag az Átlátszó adattitkosítás (TDE) állapotát kapja egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e4746-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="e4746-107">További információt az Átlátszó adattitkosítás az Azure SQL-adatbázissal https://msdn.microsoft.com/library/dn948096 ( a Microsoft Developer Network Library https://msdn.microsoft.com/library/dn948096) webhelyén) című cikk tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e4746-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="e4746-108">Ez a parancsmag a TDE aktuális állapotát kapja meg, de a titkosítás és a visszafejtés hosszú futású művelet is lehet.</span><span class="sxs-lookup"><span data-stu-id="e4746-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="e4746-109">A titkosítási vizsgálat előrehaladásának ellenőrzéshez futtassa a Get-AzSqlDatabaseTransparentDataEncryptionActivity parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e4746-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="e4746-110">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="e4746-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e4746-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4746-111">EXAMPLES</span></span>

### <span data-ttu-id="e4746-112">1. példa: Adatbázis TDE-állapotának lekérte</span><span class="sxs-lookup"><span data-stu-id="e4746-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="e4746-113">Ez a parancs a Database01 nevű adatbázis TDE-állapotát kapja meg a kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e4746-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="e4746-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4746-114">PARAMETERS</span></span>

### <span data-ttu-id="e4746-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4746-115">-DatabaseName</span></span>
<span data-ttu-id="e4746-116">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja TDE-állapotot kap.</span><span class="sxs-lookup"><span data-stu-id="e4746-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="e4746-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4746-117">-DefaultProfile</span></span>
<span data-ttu-id="e4746-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4746-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4746-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4746-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4746-120">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e4746-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e4746-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4746-121">-ServerName</span></span>
<span data-ttu-id="e4746-122">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja TDE-állapotot kap.</span><span class="sxs-lookup"><span data-stu-id="e4746-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="e4746-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4746-123">-Confirm</span></span>
<span data-ttu-id="e4746-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4746-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4746-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4746-125">-WhatIf</span></span>
<span data-ttu-id="e4746-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4746-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4746-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4746-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4746-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4746-128">CommonParameters</span></span>
<span data-ttu-id="e4746-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4746-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4746-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4746-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4746-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4746-131">INPUTS</span></span>

### <span data-ttu-id="e4746-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e4746-132">System.String</span></span>

## <span data-ttu-id="e4746-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4746-133">OUTPUTS</span></span>

### <span data-ttu-id="e4746-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="e4746-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="e4746-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4746-135">NOTES</span></span>

## <span data-ttu-id="e4746-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4746-136">RELATED LINKS</span></span>

[<span data-ttu-id="e4746-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="e4746-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="e4746-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="e4746-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
