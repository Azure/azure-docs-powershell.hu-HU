---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ad00759bb2babb85c17ab9efe2d7e47025434607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933633"
---
# <span data-ttu-id="f5cd6-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5cd6-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f5cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cd6-103">Adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="f5cd6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f5cd6-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5cd6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f5cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="f5cd6-106">A **Get-AzSqlServerDisasterRecoveryConfiguration parancsmag** sql-adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f5cd6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f5cd6-107">EXAMPLES</span></span>

## <span data-ttu-id="f5cd6-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5cd6-108">PARAMETERS</span></span>

### <span data-ttu-id="f5cd6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cd6-109">-DefaultProfile</span></span>
<span data-ttu-id="f5cd6-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5cd6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5cd6-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cd6-111">-ResourceGroupName</span></span>
<span data-ttu-id="f5cd6-112">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f5cd6-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f5cd6-113">-ServerName</span></span>
<span data-ttu-id="f5cd6-114">Az SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="f5cd6-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f5cd6-115">-VirtualEndpointName</span></span>
<span data-ttu-id="f5cd6-116">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cd6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5cd6-117">-Confirm</span></span>
<span data-ttu-id="f5cd6-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5cd6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cd6-119">-WhatIf</span></span>
<span data-ttu-id="f5cd6-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5cd6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5cd6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cd6-122">CommonParameters</span></span>
<span data-ttu-id="f5cd6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5cd6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cd6-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5cd6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cd6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5cd6-125">INPUTS</span></span>

### <span data-ttu-id="f5cd6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f5cd6-126">System.String</span></span>

## <span data-ttu-id="f5cd6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5cd6-127">OUTPUTS</span></span>

### <span data-ttu-id="f5cd6-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="f5cd6-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="f5cd6-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f5cd6-129">NOTES</span></span>

## <span data-ttu-id="f5cd6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5cd6-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5cd6-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5cd6-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f5cd6-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5cd6-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f5cd6-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5cd6-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f5cd6-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5cd6-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

