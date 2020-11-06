---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: be4a4f418268d1e2523e13d5a779f911381c7309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499331"
---
# <span data-ttu-id="0a675-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0a675-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="0a675-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a675-102">SYNOPSIS</span></span>
<span data-ttu-id="0a675-103">Eltávolítja az SQL-adatbázisból az adott visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="0a675-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a675-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a675-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a675-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a675-105">DESCRIPTION</span></span>
<span data-ttu-id="0a675-106">A **Remove-AzureRmSqlDatabaseRestorePoint** parancsmag eltávolítja az Azure SQL-adatbázisból az adott visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="0a675-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="0a675-107">Ezt a parancsmagot jelenleg az Azure SQL-adatbázis SQL Server adattárházi szolgáltatása támogatja.</span><span class="sxs-lookup"><span data-stu-id="0a675-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="0a675-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0a675-108">EXAMPLES</span></span>

### <span data-ttu-id="0a675-109">1. példa: visszaállítási pont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a675-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="0a675-110">Ez a parancs eltávolítja az Azure SQL-adatbázis visszaállítási pontját a Létrehozás dátuma beállítással.</span><span class="sxs-lookup"><span data-stu-id="0a675-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="0a675-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a675-111">PARAMETERS</span></span>

### <span data-ttu-id="0a675-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a675-112">-DatabaseName</span></span>
<span data-ttu-id="0a675-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a675-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="0a675-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a675-114">-DefaultProfile</span></span>
<span data-ttu-id="0a675-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a675-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a675-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a675-116">-PassThru</span></span>
<span data-ttu-id="0a675-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0a675-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0a675-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a675-118">-ResourceGroupName</span></span>
<span data-ttu-id="0a675-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0a675-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="0a675-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="0a675-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="0a675-121">A visszaállítási pont létrehozási dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a675-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a675-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0a675-122">-ServerName</span></span>
<span data-ttu-id="0a675-123">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a675-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="0a675-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a675-124">-Confirm</span></span>
<span data-ttu-id="0a675-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a675-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a675-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a675-126">-WhatIf</span></span>
<span data-ttu-id="0a675-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a675-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a675-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a675-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a675-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a675-129">CommonParameters</span></span>
<span data-ttu-id="0a675-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a675-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a675-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a675-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a675-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a675-132">INPUTS</span></span>

### <span data-ttu-id="0a675-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0a675-133">System.DateTime</span></span>

### <span data-ttu-id="0a675-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a675-134">System.String</span></span>

## <span data-ttu-id="0a675-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a675-135">OUTPUTS</span></span>

### <span data-ttu-id="0a675-136">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="0a675-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="0a675-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a675-137">NOTES</span></span>

## <span data-ttu-id="0a675-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a675-138">RELATED LINKS</span></span>
