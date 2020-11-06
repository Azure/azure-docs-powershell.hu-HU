---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501344"
---
# <span data-ttu-id="a0313-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a0313-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a0313-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0313-102">SYNOPSIS</span></span>
<span data-ttu-id="a0313-103">Eltávolítja az SQL-adatbázisból az adott visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="a0313-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0313-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0313-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0313-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0313-105">DESCRIPTION</span></span>
<span data-ttu-id="a0313-106">A **Remove-AzureRmSqlDatabaseRestorePoint** parancsmag eltávolítja az Azure SQL-adatbázisból az adott visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="a0313-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="a0313-107">Ezt a parancsmagot jelenleg az Azure SQL-adatbázis SQL Server adattárházi szolgáltatása támogatja.</span><span class="sxs-lookup"><span data-stu-id="a0313-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="a0313-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a0313-108">EXAMPLES</span></span>

### <span data-ttu-id="a0313-109">1. példa: visszaállítási pont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a0313-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="a0313-110">Ez a parancs eltávolítja az Azure SQL-adatbázis visszaállítási pontját a Létrehozás dátuma beállítással.</span><span class="sxs-lookup"><span data-stu-id="a0313-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="a0313-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0313-111">PARAMETERS</span></span>

### <span data-ttu-id="a0313-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0313-112">-DatabaseName</span></span>
<span data-ttu-id="a0313-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0313-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0313-114">-DefaultProfile</span></span>
<span data-ttu-id="a0313-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0313-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0313-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0313-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a0313-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="a0313-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="a0313-119">A visszaállítási pont létrehozási dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0313-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a0313-120">-ServerName</span></span>
<span data-ttu-id="a0313-121">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0313-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0313-122">-Confirm</span></span>
<span data-ttu-id="a0313-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0313-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0313-124">-WhatIf</span></span>
<span data-ttu-id="a0313-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0313-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0313-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0313-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0313-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0313-127">CommonParameters</span></span>
<span data-ttu-id="a0313-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0313-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0313-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0313-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0313-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0313-130">INPUTS</span></span>

## <span data-ttu-id="a0313-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0313-131">OUTPUTS</span></span>

## <span data-ttu-id="a0313-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0313-132">NOTES</span></span>

## <span data-ttu-id="a0313-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0313-133">RELATED LINKS</span></span>
