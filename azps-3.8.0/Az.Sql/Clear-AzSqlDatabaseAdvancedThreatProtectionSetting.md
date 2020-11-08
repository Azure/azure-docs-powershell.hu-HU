---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013719"
---
# <span data-ttu-id="ac427-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ac427-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ac427-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac427-102">SYNOPSIS</span></span>
<span data-ttu-id="ac427-103">Eltávolítja a speciális veszélyforrások elleni védelem beállításait egy adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="ac427-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="ac427-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac427-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac427-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac427-105">DESCRIPTION</span></span>
<span data-ttu-id="ac427-106">A **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag eltávolítja a speciális veszélyforrások elleni védelem beállításait egy AzureAzure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="ac427-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="ac427-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak az adatbázisnak a meghatározásához, amelyből a parancsmag eltávolítja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="ac427-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="ac427-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ac427-108">EXAMPLES</span></span>

### <span data-ttu-id="ac427-109">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ac427-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ac427-110">Ez a parancs eltávolítja a Database01 nevű adatbázis speciális veszélyforrások elleni védelmét a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ac427-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ac427-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac427-111">PARAMETERS</span></span>

### <span data-ttu-id="ac427-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ac427-112">-DatabaseName</span></span>
<span data-ttu-id="ac427-113">Annak az adatbázisnak a neve, amelybe a speciális veszélyforrások elleni védelem beállításait el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="ac427-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="ac427-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac427-114">-DefaultProfile</span></span>
<span data-ttu-id="ac427-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ac427-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac427-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac427-116">-PassThru</span></span>
<span data-ttu-id="ac427-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ac427-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac427-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ac427-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac427-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac427-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac427-120">Annak a csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="ac427-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="ac427-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ac427-121">-ServerName</span></span>
<span data-ttu-id="ac427-122">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis fut.</span><span class="sxs-lookup"><span data-stu-id="ac427-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="ac427-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac427-123">-Confirm</span></span>
<span data-ttu-id="ac427-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac427-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac427-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac427-125">-WhatIf</span></span>
<span data-ttu-id="ac427-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac427-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac427-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac427-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac427-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac427-128">CommonParameters</span></span>
<span data-ttu-id="ac427-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac427-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac427-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac427-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac427-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac427-131">INPUTS</span></span>

### <span data-ttu-id="ac427-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac427-132">System.String</span></span>

## <span data-ttu-id="ac427-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac427-133">OUTPUTS</span></span>

### <span data-ttu-id="ac427-134">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ac427-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ac427-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac427-135">NOTES</span></span>

## <span data-ttu-id="ac427-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac427-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac427-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ac427-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


