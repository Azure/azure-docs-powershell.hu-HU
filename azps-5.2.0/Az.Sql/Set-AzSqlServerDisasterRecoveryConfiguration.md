---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355493"
---
# <span data-ttu-id="156be-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="156be-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="156be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156be-102">SYNOPSIS</span></span>
<span data-ttu-id="156be-103">Módosítja az adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="156be-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="156be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="156be-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="156be-105">DESCRIPTION</span></span>
<span data-ttu-id="156be-106">A **Set-AzSqlServerDisasterRecoveryConfiguration** parancsmag módosítja az SQL-adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="156be-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="156be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="156be-107">EXAMPLES</span></span>

## <span data-ttu-id="156be-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="156be-108">PARAMETERS</span></span>

### <span data-ttu-id="156be-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="156be-109">-AllowDataLoss</span></span>
<span data-ttu-id="156be-110">Azt jelzi, hogy a feladatátvételi művelet lehetővé teszi az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="156be-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="156be-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="156be-111">-AsJob</span></span>
<span data-ttu-id="156be-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="156be-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="156be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156be-113">-DefaultProfile</span></span>
<span data-ttu-id="156be-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="156be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="156be-115">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="156be-115">-Failover</span></span>
<span data-ttu-id="156be-116">Azt jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="156be-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="156be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156be-117">-ResourceGroupName</span></span>
<span data-ttu-id="156be-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="156be-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="156be-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="156be-119">-ServerName</span></span>
<span data-ttu-id="156be-120">Egy SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="156be-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="156be-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="156be-121">-VirtualEndpointName</span></span>
<span data-ttu-id="156be-122">Egy virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="156be-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="156be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="156be-123">-Confirm</span></span>
<span data-ttu-id="156be-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="156be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156be-125">-WhatIf</span></span>
<span data-ttu-id="156be-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="156be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156be-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="156be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156be-128">CommonParameters</span></span>
<span data-ttu-id="156be-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156be-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="156be-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156be-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="156be-131">INPUTS</span></span>

### <span data-ttu-id="156be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="156be-132">System.String</span></span>

## <span data-ttu-id="156be-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="156be-133">OUTPUTS</span></span>

### <span data-ttu-id="156be-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="156be-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="156be-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="156be-135">NOTES</span></span>

## <span data-ttu-id="156be-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="156be-136">RELATED LINKS</span></span>

[<span data-ttu-id="156be-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="156be-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="156be-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="156be-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="156be-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="156be-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="156be-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="156be-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
