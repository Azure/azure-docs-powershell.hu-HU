---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939385"
---
# <span data-ttu-id="65853-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65853-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="65853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65853-102">SYNOPSIS</span></span>
<span data-ttu-id="65853-103">Módosítja az adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="65853-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="65853-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65853-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65853-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65853-105">DESCRIPTION</span></span>
<span data-ttu-id="65853-106">A **Set-AzSqlServerDisasterRecoveryConfiguration** parancsmag módosítja az SQL-adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="65853-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="65853-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65853-107">EXAMPLES</span></span>

## <span data-ttu-id="65853-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65853-108">PARAMETERS</span></span>

### <span data-ttu-id="65853-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="65853-109">-AllowDataLoss</span></span>
<span data-ttu-id="65853-110">Azt jelzi, hogy a feladatátvételi művelet lehetővé teszi az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="65853-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="65853-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65853-111">-AsJob</span></span>
<span data-ttu-id="65853-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65853-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65853-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65853-113">-DefaultProfile</span></span>
<span data-ttu-id="65853-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65853-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65853-115">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="65853-115">-Failover</span></span>
<span data-ttu-id="65853-116">Azt jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="65853-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65853-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65853-117">-ResourceGroupName</span></span>
<span data-ttu-id="65853-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65853-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="65853-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="65853-119">-ServerName</span></span>
<span data-ttu-id="65853-120">Egy SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65853-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="65853-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="65853-121">-VirtualEndpointName</span></span>
<span data-ttu-id="65853-122">Egy virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65853-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65853-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65853-123">-Confirm</span></span>
<span data-ttu-id="65853-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65853-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65853-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65853-125">-WhatIf</span></span>
<span data-ttu-id="65853-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65853-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65853-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65853-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65853-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65853-128">CommonParameters</span></span>
<span data-ttu-id="65853-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65853-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65853-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65853-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65853-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65853-131">INPUTS</span></span>

### <span data-ttu-id="65853-132">System.String</span><span class="sxs-lookup"><span data-stu-id="65853-132">System.String</span></span>

## <span data-ttu-id="65853-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65853-133">OUTPUTS</span></span>

### <span data-ttu-id="65853-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="65853-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="65853-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65853-135">NOTES</span></span>

## <span data-ttu-id="65853-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65853-136">RELATED LINKS</span></span>

[<span data-ttu-id="65853-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65853-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65853-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65853-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65853-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65853-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65853-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="65853-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
