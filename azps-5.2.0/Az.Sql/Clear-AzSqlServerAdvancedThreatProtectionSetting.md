---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334806"
---
# <span data-ttu-id="8c6bf-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8c6bf-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8c6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6bf-103">Eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait a kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="8c6bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c6bf-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6bf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="8c6bf-106">A Clear-AzSqlServerAdvancedThreatProtectionSetting parancsmag eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait az Azure SQL-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="8c6bf-107">Ha használni szeretné ezt a parancsmagot, adja meg a ResourceGroupName és a ServerName paramétert annak a kiszolgálónak a azonosításához, amelyből a parancsmag eltávolítja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="8c6bf-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c6bf-108">EXAMPLES</span></span>

### <span data-ttu-id="8c6bf-109">1. példa: Komplex veszélyforrás-védelmi beállítások eltávolítása adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="8c6bf-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="8c6bf-110">Ez a parancs eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait a Server01 nevű kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="8c6bf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c6bf-111">PARAMETERS</span></span>

### <span data-ttu-id="8c6bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6bf-112">-DefaultProfile</span></span>
<span data-ttu-id="8c6bf-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c6bf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c6bf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c6bf-114">-PassThru</span></span>
<span data-ttu-id="8c6bf-115">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c6bf-116">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c6bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c6bf-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="8c6bf-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c6bf-119">-ServerName</span></span>
<span data-ttu-id="8c6bf-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6bf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c6bf-121">-Confirm</span></span>
<span data-ttu-id="8c6bf-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6bf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6bf-123">-WhatIf</span></span>
<span data-ttu-id="8c6bf-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6bf-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6bf-126">CommonParameters</span></span>
<span data-ttu-id="8c6bf-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6bf-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c6bf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6bf-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c6bf-129">INPUTS</span></span>

### <span data-ttu-id="8c6bf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8c6bf-130">System.String</span></span>

## <span data-ttu-id="8c6bf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c6bf-131">OUTPUTS</span></span>

### <span data-ttu-id="8c6bf-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="8c6bf-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="8c6bf-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c6bf-133">NOTES</span></span>

## <span data-ttu-id="8c6bf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c6bf-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c6bf-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8c6bf-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

