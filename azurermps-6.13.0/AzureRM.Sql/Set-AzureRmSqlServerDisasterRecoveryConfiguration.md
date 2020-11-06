---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494883"
---
# <span data-ttu-id="c1894-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1894-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="c1894-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1894-102">SYNOPSIS</span></span>
<span data-ttu-id="c1894-103">Módosítja az adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c1894-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1894-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1894-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1894-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1894-105">DESCRIPTION</span></span>
<span data-ttu-id="c1894-106">A **set-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag módosította az SQL-adatbázis kiszolgálójának helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c1894-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="c1894-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1894-107">EXAMPLES</span></span>

## <span data-ttu-id="c1894-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1894-108">PARAMETERS</span></span>

### <span data-ttu-id="c1894-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c1894-109">-AllowDataLoss</span></span>
<span data-ttu-id="c1894-110">Jelzi, hogy a feladatátvételi művelet lehetővé teszi az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="c1894-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="c1894-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1894-111">-AsJob</span></span>
<span data-ttu-id="c1894-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1894-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1894-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1894-113">-DefaultProfile</span></span>
<span data-ttu-id="c1894-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1894-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1894-115">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="c1894-115">-Failover</span></span>
<span data-ttu-id="c1894-116">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="c1894-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="c1894-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1894-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1894-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1894-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1894-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c1894-119">-ServerName</span></span>
<span data-ttu-id="c1894-120">Egy SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1894-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="c1894-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="c1894-121">-VirtualEndpointName</span></span>
<span data-ttu-id="c1894-122">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1894-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="c1894-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1894-123">-Confirm</span></span>
<span data-ttu-id="c1894-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1894-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1894-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1894-125">-WhatIf</span></span>
<span data-ttu-id="c1894-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1894-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1894-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1894-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1894-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1894-128">CommonParameters</span></span>
<span data-ttu-id="c1894-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1894-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1894-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1894-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1894-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1894-131">INPUTS</span></span>

### <span data-ttu-id="c1894-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c1894-132">System.String</span></span>

## <span data-ttu-id="c1894-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1894-133">OUTPUTS</span></span>

### <span data-ttu-id="c1894-134">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="c1894-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="c1894-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1894-135">NOTES</span></span>

## <span data-ttu-id="c1894-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1894-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1894-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1894-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c1894-138">Új – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1894-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c1894-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1894-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c1894-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c1894-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
