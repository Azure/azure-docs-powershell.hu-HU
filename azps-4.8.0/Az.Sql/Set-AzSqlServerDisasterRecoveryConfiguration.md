---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183859"
---
# <span data-ttu-id="9d63f-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d63f-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="9d63f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d63f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d63f-103">Módosítja az adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="9d63f-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="9d63f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d63f-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d63f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d63f-105">DESCRIPTION</span></span>
<span data-ttu-id="9d63f-106">A **set-AzSqlServerDisasterRecoveryConfiguration** parancsmag módosította az SQL-adatbázis kiszolgálójának helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="9d63f-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="9d63f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d63f-107">EXAMPLES</span></span>

## <span data-ttu-id="9d63f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d63f-108">PARAMETERS</span></span>

### <span data-ttu-id="9d63f-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="9d63f-109">-AllowDataLoss</span></span>
<span data-ttu-id="9d63f-110">Jelzi, hogy a feladatátvételi művelet lehetővé teszi az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="9d63f-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="9d63f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d63f-111">-AsJob</span></span>
<span data-ttu-id="9d63f-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d63f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d63f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d63f-113">-DefaultProfile</span></span>
<span data-ttu-id="9d63f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9d63f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d63f-115">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="9d63f-115">-Failover</span></span>
<span data-ttu-id="9d63f-116">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="9d63f-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="9d63f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d63f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d63f-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d63f-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d63f-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9d63f-119">-ServerName</span></span>
<span data-ttu-id="9d63f-120">Egy SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d63f-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="9d63f-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="9d63f-121">-VirtualEndpointName</span></span>
<span data-ttu-id="9d63f-122">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d63f-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="9d63f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d63f-123">-Confirm</span></span>
<span data-ttu-id="9d63f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d63f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d63f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d63f-125">-WhatIf</span></span>
<span data-ttu-id="9d63f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d63f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d63f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d63f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d63f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d63f-128">CommonParameters</span></span>
<span data-ttu-id="9d63f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d63f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d63f-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d63f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d63f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d63f-131">INPUTS</span></span>

### <span data-ttu-id="9d63f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9d63f-132">System.String</span></span>

## <span data-ttu-id="9d63f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d63f-133">OUTPUTS</span></span>

### <span data-ttu-id="9d63f-134">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="9d63f-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="9d63f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d63f-135">NOTES</span></span>

## <span data-ttu-id="9d63f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d63f-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d63f-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d63f-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9d63f-138">Új – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d63f-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9d63f-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d63f-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9d63f-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9d63f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
