---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368520"
---
# <span data-ttu-id="b8046-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b8046-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="b8046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8046-102">SYNOPSIS</span></span>
<span data-ttu-id="b8046-103">Adatbázist és kibontott tulajdonságértékeket kap.</span><span class="sxs-lookup"><span data-stu-id="b8046-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="b8046-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8046-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8046-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8046-105">DESCRIPTION</span></span>
<span data-ttu-id="b8046-106">A **Get-AzSqlDatabaseExpanded** parancsmag adatbázist és kibontott tulajdonságértékeket kap.</span><span class="sxs-lookup"><span data-stu-id="b8046-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="b8046-107">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="b8046-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b8046-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8046-108">EXAMPLES</span></span>

### <span data-ttu-id="b8046-109">1. példa: Szolgáltatásszintű tanácsadó adatokat tartalmazó adatbázis-objektum lekérte</span><span class="sxs-lookup"><span data-stu-id="b8046-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b8046-110">Ez a parancs visszaadja azt az adatbázist, amely kibontott tulajdonságokkal rendelkezik, amelyek a szolgáltatásszintű tanácsadó adatait tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="b8046-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="b8046-111">2. példa: Adatbázis-objektumok listába sorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="b8046-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="b8046-112">Ez a parancs kibontott adatbázis-objektumot ad vissza a Server01 kiszolgáló összes olyan adatbázisához, amely az "Adatbázis" kezdettől kezdődik.</span><span class="sxs-lookup"><span data-stu-id="b8046-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="b8046-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8046-113">PARAMETERS</span></span>

### <span data-ttu-id="b8046-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8046-114">-DatabaseName</span></span>
<span data-ttu-id="b8046-115">A lekért adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b8046-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8046-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8046-116">-DefaultProfile</span></span>
<span data-ttu-id="b8046-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8046-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8046-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8046-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8046-119">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b8046-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b8046-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8046-120">-ServerName</span></span>
<span data-ttu-id="b8046-121">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8046-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b8046-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8046-122">-Confirm</span></span>
<span data-ttu-id="b8046-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8046-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8046-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8046-124">-WhatIf</span></span>
<span data-ttu-id="b8046-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8046-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8046-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8046-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8046-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8046-127">CommonParameters</span></span>
<span data-ttu-id="b8046-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8046-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8046-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8046-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8046-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8046-130">INPUTS</span></span>

### <span data-ttu-id="b8046-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8046-131">System.String</span></span>

## <span data-ttu-id="b8046-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8046-132">OUTPUTS</span></span>

### <span data-ttu-id="b8046-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="b8046-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="b8046-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8046-134">NOTES</span></span>

## <span data-ttu-id="b8046-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8046-135">RELATED LINKS</span></span>

[<span data-ttu-id="b8046-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b8046-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
