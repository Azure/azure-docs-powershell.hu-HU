---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371963"
---
# <span data-ttu-id="948d3-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="948d3-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="948d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948d3-102">SYNOPSIS</span></span>
<span data-ttu-id="948d3-103">Egy adatbázis TDE-vizsgálatának előrehaladását olvassa be.</span><span class="sxs-lookup"><span data-stu-id="948d3-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="948d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="948d3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="948d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="948d3-105">DESCRIPTION</span></span>
<span data-ttu-id="948d3-106">A **Get-AzSqlDatabaseTransparentDataEncryptionActivity** parancsmag egy Azure SQL-adatbázis TDE-vizsgálatának előrehaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="948d3-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="948d3-107">Ha nem fut titkosítási időtartam, ez a parancsmag egy üres listát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="948d3-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="948d3-108">További információt az Átlátszó adattitkosítás az Azure SQL-adatbázissal https://msdn.microsoft.com/library/dn948096 ( a Microsoft Developer Network Library https://msdn.microsoft.com/library/dn948096) webhelyén) című cikk tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="948d3-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="948d3-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="948d3-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="948d3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="948d3-110">EXAMPLES</span></span>

### <span data-ttu-id="948d3-111">1. példa: TDE-tevékenység lekésése adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="948d3-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="948d3-112">Ez a parancs a database01 nevű adatbázis TDE-tevékenységét kapja meg a kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="948d3-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="948d3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="948d3-113">PARAMETERS</span></span>

### <span data-ttu-id="948d3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="948d3-114">-DatabaseName</span></span>
<span data-ttu-id="948d3-115">Annak az adatbázisnak a neve, amelyhez ez a parancsmag TDE-titkosítási tevékenységet kap.</span><span class="sxs-lookup"><span data-stu-id="948d3-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="948d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948d3-116">-DefaultProfile</span></span>
<span data-ttu-id="948d3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="948d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="948d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="948d3-119">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="948d3-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="948d3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="948d3-120">-ServerName</span></span>
<span data-ttu-id="948d3-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="948d3-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="948d3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="948d3-122">-Confirm</span></span>
<span data-ttu-id="948d3-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="948d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948d3-124">-WhatIf</span></span>
<span data-ttu-id="948d3-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="948d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948d3-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="948d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948d3-127">CommonParameters</span></span>
<span data-ttu-id="948d3-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948d3-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="948d3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948d3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="948d3-130">INPUTS</span></span>

### <span data-ttu-id="948d3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="948d3-131">System.String</span></span>

## <span data-ttu-id="948d3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="948d3-132">OUTPUTS</span></span>

### <span data-ttu-id="948d3-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="948d3-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="948d3-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="948d3-134">NOTES</span></span>

## <span data-ttu-id="948d3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="948d3-135">RELATED LINKS</span></span>

[<span data-ttu-id="948d3-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="948d3-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="948d3-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="948d3-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


