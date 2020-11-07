---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679247"
---
# <span data-ttu-id="de32f-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="de32f-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="de32f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de32f-102">SYNOPSIS</span></span>
<span data-ttu-id="de32f-103">Új visszaállítási pont létrehozása, amelyből egy SQL-adatbázis visszaadható.</span><span class="sxs-lookup"><span data-stu-id="de32f-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de32f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de32f-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de32f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de32f-105">DESCRIPTION</span></span>
<span data-ttu-id="de32f-106">A **New-AzureRmSqlDatabaseRestorePoint** parancsmag új visszaállítási pontot hoz létre, amelyet egy Azure SQL-adatbázis vissza lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="de32f-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="de32f-107">Ezt a parancsmagot jelenleg az Azure SQL-adatbázis SQL Server adattárházi szolgáltatása támogatja.</span><span class="sxs-lookup"><span data-stu-id="de32f-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="de32f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="de32f-108">EXAMPLES</span></span>

### <span data-ttu-id="de32f-109">Példa 1: visszaállítási pont létrehozása</span><span class="sxs-lookup"><span data-stu-id="de32f-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="de32f-110">A parancs létrehozza az Azure SQL-adatbázis visszaállítási pontját, és a visszaállítási pont részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="de32f-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="de32f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de32f-111">PARAMETERS</span></span>

### <span data-ttu-id="de32f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de32f-112">-DatabaseName</span></span>
<span data-ttu-id="de32f-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de32f-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="de32f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de32f-114">-DefaultProfile</span></span>
<span data-ttu-id="de32f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de32f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de32f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de32f-116">-ResourceGroupName</span></span>
<span data-ttu-id="de32f-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="de32f-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="de32f-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="de32f-118">-RestorePointLabel</span></span>
<span data-ttu-id="de32f-119">A visszaállítási pont címkét adja meg az egyszerű azonosításhoz.</span><span class="sxs-lookup"><span data-stu-id="de32f-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de32f-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="de32f-120">-ServerName</span></span>
<span data-ttu-id="de32f-121">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de32f-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="de32f-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de32f-122">-Confirm</span></span>
<span data-ttu-id="de32f-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de32f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de32f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de32f-124">-WhatIf</span></span>
<span data-ttu-id="de32f-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de32f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de32f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de32f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de32f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de32f-127">CommonParameters</span></span>
<span data-ttu-id="de32f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de32f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de32f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de32f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de32f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de32f-130">INPUTS</span></span>

## <span data-ttu-id="de32f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de32f-131">OUTPUTS</span></span>

## <span data-ttu-id="de32f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de32f-132">NOTES</span></span>

## <span data-ttu-id="de32f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de32f-133">RELATED LINKS</span></span>
