---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013699"
---
# <span data-ttu-id="b8fa3-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b8fa3-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b8fa3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fa3-103">A speciális veszélyforrások elleni védelem beállításainak eltávolítása a kiszolgálókról.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="b8fa3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8fa3-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fa3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fa3-106">A Clear-AzSqlServerAdvancedThreatProtectionSetting parancsmag eltávolítja a speciális veszélyforrások elleni védelem beállításait egy Azure SQL Server-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="b8fa3-107">A parancsmag használatához adja meg a ResourceGroupName és a kiszolgálónév paramétert annak a kiszolgálónak a meghatározásához, amelyből a parancsmag eltávolítja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="b8fa3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b8fa3-108">EXAMPLES</span></span>

### <span data-ttu-id="b8fa3-109">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b8fa3-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b8fa3-110">Ez a parancs eltávolítja a Server01 nevű kiszolgáló speciális veszélyforrások elleni védelemre vonatkozó beállításait.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="b8fa3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8fa3-111">PARAMETERS</span></span>

### <span data-ttu-id="b8fa3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fa3-112">-DefaultProfile</span></span>
<span data-ttu-id="b8fa3-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8fa3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8fa3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8fa3-114">-PassThru</span></span>
<span data-ttu-id="b8fa3-115">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b8fa3-116">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8fa3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fa3-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8fa3-118">Annak a csoportnak a neve, amelyhez a kiszolgáló van társítva.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b8fa3-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b8fa3-119">-ServerName</span></span>
<span data-ttu-id="b8fa3-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b8fa3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8fa3-121">-Confirm</span></span>
<span data-ttu-id="b8fa3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fa3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fa3-123">-WhatIf</span></span>
<span data-ttu-id="b8fa3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fa3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fa3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fa3-126">CommonParameters</span></span>
<span data-ttu-id="b8fa3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8fa3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fa3-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8fa3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fa3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8fa3-129">INPUTS</span></span>

### <span data-ttu-id="b8fa3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b8fa3-130">System.String</span></span>

## <span data-ttu-id="b8fa3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8fa3-131">OUTPUTS</span></span>

### <span data-ttu-id="b8fa3-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="b8fa3-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="b8fa3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8fa3-133">NOTES</span></span>

## <span data-ttu-id="b8fa3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8fa3-134">RELATED LINKS</span></span>

[<span data-ttu-id="b8fa3-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b8fa3-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

