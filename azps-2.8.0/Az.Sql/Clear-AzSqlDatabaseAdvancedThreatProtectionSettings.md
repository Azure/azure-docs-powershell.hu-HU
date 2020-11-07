---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: f15ccf5c397ece13a034c99c29ac6cd5f18f9f58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838742"
---
# <span data-ttu-id="946b8-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="946b8-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="946b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="946b8-102">SYNOPSIS</span></span>
<span data-ttu-id="946b8-103">Eltávolítja a speciális veszélyforrások elleni védelem beállításait egy adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="946b8-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="946b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="946b8-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="946b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="946b8-105">DESCRIPTION</span></span>
<span data-ttu-id="946b8-106">A **Clear-AzSqlDatabaseAdvancedThreatProtectionSettings** parancsmag eltávolítja a speciális veszélyforrások elleni védelem beállításait egy AzureAzure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="946b8-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="946b8-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak az adatbázisnak a meghatározásához, amelyből a parancsmag eltávolítja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="946b8-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="946b8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="946b8-108">EXAMPLES</span></span>

### <span data-ttu-id="946b8-109">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="946b8-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="946b8-110">Ez a parancs eltávolítja a Database01 nevű adatbázis speciális veszélyforrások elleni védelmét a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="946b8-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="946b8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="946b8-111">PARAMETERS</span></span>

### <span data-ttu-id="946b8-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="946b8-112">-DatabaseName</span></span>
<span data-ttu-id="946b8-113">Annak az adatbázisnak a neve, amelybe a speciális veszélyforrások elleni védelem beállításait el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="946b8-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="946b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946b8-114">-DefaultProfile</span></span>
<span data-ttu-id="946b8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="946b8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="946b8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="946b8-116">-PassThru</span></span>
<span data-ttu-id="946b8-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="946b8-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="946b8-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="946b8-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="946b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="946b8-120">Annak a csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="946b8-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="946b8-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="946b8-121">-ServerName</span></span>
<span data-ttu-id="946b8-122">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis fut.</span><span class="sxs-lookup"><span data-stu-id="946b8-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="946b8-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="946b8-123">-Confirm</span></span>
<span data-ttu-id="946b8-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="946b8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946b8-125">-WhatIf</span></span>
<span data-ttu-id="946b8-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="946b8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="946b8-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="946b8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946b8-128">CommonParameters</span></span>
<span data-ttu-id="946b8-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="946b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946b8-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946b8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946b8-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="946b8-131">INPUTS</span></span>

### <span data-ttu-id="946b8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="946b8-132">System.String</span></span>

## <span data-ttu-id="946b8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="946b8-133">OUTPUTS</span></span>

### <span data-ttu-id="946b8-134">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="946b8-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="946b8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="946b8-135">NOTES</span></span>

## <span data-ttu-id="946b8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="946b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="946b8-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="946b8-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


