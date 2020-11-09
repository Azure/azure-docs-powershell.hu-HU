---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296690"
---
# <span data-ttu-id="024da-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="024da-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="024da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="024da-102">SYNOPSIS</span></span>
<span data-ttu-id="024da-103">Egy adatbázis TDE-vizsgálatának előrehaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="024da-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="024da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="024da-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="024da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="024da-105">DESCRIPTION</span></span>
<span data-ttu-id="024da-106">A **Get-AzSqlDatabaseTransparentDataEncryptionActivity** parancsmag az Azure SQL-adatbázisok átlátszó adattitkosítási (TDE) vizsgálatának előrehaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="024da-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="024da-107">Ha nem fut a titkosítási tartomány, ez a parancsmag üres listát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="024da-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="024da-108">További információért olvassa el az átlátszó adattitkosítás az Azure SQL-adatbázisokkal https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) a Microsoft Developer Network Library-ban című témakört).</span><span class="sxs-lookup"><span data-stu-id="024da-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="024da-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="024da-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="024da-110">Példák</span><span class="sxs-lookup"><span data-stu-id="024da-110">EXAMPLES</span></span>

### <span data-ttu-id="024da-111">1. példa: TDE-tevékenység beszerzése egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="024da-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="024da-112">Ez a parancs a server01 nevű kiszolgálón a database01 nevű adatbázis TDE tevékenységét kapja.</span><span class="sxs-lookup"><span data-stu-id="024da-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="024da-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="024da-113">PARAMETERS</span></span>

### <span data-ttu-id="024da-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="024da-114">-DatabaseName</span></span>
<span data-ttu-id="024da-115">Annak az adatbázisnak a neve, amelyhez a parancsmag TDE-titkosítási tevékenységet kap.</span><span class="sxs-lookup"><span data-stu-id="024da-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="024da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024da-116">-DefaultProfile</span></span>
<span data-ttu-id="024da-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="024da-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="024da-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="024da-118">-ResourceGroupName</span></span>
<span data-ttu-id="024da-119">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="024da-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="024da-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="024da-120">-ServerName</span></span>
<span data-ttu-id="024da-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="024da-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="024da-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="024da-122">-Confirm</span></span>
<span data-ttu-id="024da-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="024da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="024da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="024da-124">-WhatIf</span></span>
<span data-ttu-id="024da-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="024da-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="024da-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="024da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="024da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024da-127">CommonParameters</span></span>
<span data-ttu-id="024da-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="024da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024da-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="024da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024da-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="024da-130">INPUTS</span></span>

### <span data-ttu-id="024da-131">System. String</span><span class="sxs-lookup"><span data-stu-id="024da-131">System.String</span></span>

## <span data-ttu-id="024da-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="024da-132">OUTPUTS</span></span>

### <span data-ttu-id="024da-133">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="024da-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="024da-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="024da-134">NOTES</span></span>

## <span data-ttu-id="024da-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="024da-135">RELATED LINKS</span></span>

[<span data-ttu-id="024da-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="024da-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="024da-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="024da-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


