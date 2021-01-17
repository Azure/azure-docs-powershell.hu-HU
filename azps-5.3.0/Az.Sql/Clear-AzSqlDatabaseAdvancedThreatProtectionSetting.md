---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375505"
---
# <span data-ttu-id="0f854-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="0f854-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="0f854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f854-102">SYNOPSIS</span></span>
<span data-ttu-id="0f854-103">Eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait az adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="0f854-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="0f854-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f854-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f854-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f854-105">DESCRIPTION</span></span>
<span data-ttu-id="0f854-106">A **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait az AzureAzure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="0f854-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="0f854-107">Ha használni szeretné ezt a parancsmagot, adja meg a *ResourceGroupName* és *a ServerName* paramétert annak az adatbázisnak a azonosításához, amelyből a parancsmag eltávolítja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="0f854-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="0f854-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f854-108">EXAMPLES</span></span>

### <span data-ttu-id="0f854-109">1. példa: Komplex veszélyforrás-védelmi beállítások eltávolítása adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="0f854-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0f854-110">Ez a parancs eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait egy Database01 nevű adatbázisból a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="0f854-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0f854-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f854-111">PARAMETERS</span></span>

### <span data-ttu-id="0f854-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f854-112">-DatabaseName</span></span>
<span data-ttu-id="0f854-113">Annak az adatbázisnak a nevét adja meg, amelyből el kell távolítani a komplex veszélyforrások elleni védelem speciális beállításait.</span><span class="sxs-lookup"><span data-stu-id="0f854-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="0f854-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f854-114">-DefaultProfile</span></span>
<span data-ttu-id="0f854-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f854-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f854-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f854-116">-PassThru</span></span>
<span data-ttu-id="0f854-117">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="0f854-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f854-118">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0f854-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f854-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f854-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f854-120">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="0f854-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="0f854-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f854-121">-ServerName</span></span>
<span data-ttu-id="0f854-122">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis fut.</span><span class="sxs-lookup"><span data-stu-id="0f854-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="0f854-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f854-123">-Confirm</span></span>
<span data-ttu-id="0f854-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f854-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f854-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f854-125">-WhatIf</span></span>
<span data-ttu-id="0f854-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f854-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f854-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f854-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f854-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f854-128">CommonParameters</span></span>
<span data-ttu-id="0f854-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f854-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f854-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f854-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f854-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f854-131">INPUTS</span></span>

### <span data-ttu-id="0f854-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0f854-132">System.String</span></span>

## <span data-ttu-id="0f854-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f854-133">OUTPUTS</span></span>

### <span data-ttu-id="0f854-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="0f854-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="0f854-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f854-135">NOTES</span></span>

## <span data-ttu-id="0f854-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f854-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f854-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0f854-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


