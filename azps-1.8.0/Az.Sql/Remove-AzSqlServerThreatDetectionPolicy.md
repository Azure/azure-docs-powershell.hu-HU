---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668824"
---
# <span data-ttu-id="6c008-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c008-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="6c008-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c008-102">SYNOPSIS</span></span>
<span data-ttu-id="6c008-103">Eltávolítja a fenyegetések észlelési házirendjét egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="6c008-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="6c008-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c008-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c008-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c008-105">DESCRIPTION</span></span>
<span data-ttu-id="6c008-106">A Remove-AzSqlServerThreatDetectionPolicy parancsmag eltávolítja a fenyegetés-észlelési házirendet egy Azure SQL Server-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="6c008-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="6c008-107">A parancsmag használatához adja meg a ResourceGroupName és a kiszolgálónév paramétert annak a kiszolgálónak a meghatározásához, amelyből a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="6c008-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="6c008-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6c008-108">EXAMPLES</span></span>

### <span data-ttu-id="6c008-109">1. példa: fenyegetések észlelési házirendjének eltávolítása egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="6c008-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="6c008-110">Ez a parancs eltávolítja a fenyegetések észlelése házirendet egy Server01 nevű kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="6c008-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="6c008-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c008-111">PARAMETERS</span></span>

### <span data-ttu-id="6c008-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c008-112">-DefaultProfile</span></span>
<span data-ttu-id="6c008-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6c008-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c008-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c008-114">-PassThru</span></span>
<span data-ttu-id="6c008-115">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6c008-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c008-116">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6c008-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c008-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c008-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c008-118">Annak a csoportnak a neve, amelyhez a kiszolgáló van társítva.</span><span class="sxs-lookup"><span data-stu-id="6c008-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="6c008-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6c008-119">-ServerName</span></span>
<span data-ttu-id="6c008-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c008-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="6c008-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c008-121">-Confirm</span></span>
<span data-ttu-id="6c008-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c008-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c008-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c008-123">-WhatIf</span></span>
<span data-ttu-id="6c008-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c008-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c008-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c008-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c008-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c008-126">CommonParameters</span></span>
<span data-ttu-id="6c008-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c008-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c008-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6c008-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c008-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c008-129">INPUTS</span></span>

### <span data-ttu-id="6c008-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6c008-130">System.String</span></span>

## <span data-ttu-id="6c008-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c008-131">OUTPUTS</span></span>

### <span data-ttu-id="6c008-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6c008-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="6c008-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c008-133">NOTES</span></span>

## <span data-ttu-id="6c008-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c008-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c008-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6c008-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

