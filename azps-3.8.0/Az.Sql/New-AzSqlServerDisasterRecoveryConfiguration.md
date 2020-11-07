---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847390"
---
# <span data-ttu-id="a4dbe-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dbe-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a4dbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dbe-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="a4dbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4dbe-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4dbe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dbe-106">A **New-AzSqlServerDisasterRecoveryConfiguration** parancsmag létrehoz egy SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a4dbe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4dbe-107">EXAMPLES</span></span>

## <span data-ttu-id="a4dbe-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4dbe-108">PARAMETERS</span></span>

### <span data-ttu-id="a4dbe-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4dbe-109">-AsJob</span></span>
<span data-ttu-id="a4dbe-110">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a4dbe-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4dbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dbe-111">-DefaultProfile</span></span>
<span data-ttu-id="a4dbe-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a4dbe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4dbe-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="a4dbe-113">-FailoverPolicy</span></span>
<span data-ttu-id="a4dbe-114">A feladatátvételi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="a4dbe-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dbe-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a4dbe-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="a4dbe-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a4dbe-117">-PartnerServerName</span></span>
<span data-ttu-id="a4dbe-118">A partner kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="a4dbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4dbe-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a4dbe-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a4dbe-121">-ServerName</span></span>
<span data-ttu-id="a4dbe-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a4dbe-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a4dbe-123">-VirtualEndpointName</span></span>
<span data-ttu-id="a4dbe-124">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="a4dbe-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4dbe-125">-Confirm</span></span>
<span data-ttu-id="a4dbe-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dbe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dbe-127">-WhatIf</span></span>
<span data-ttu-id="a4dbe-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dbe-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dbe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dbe-130">CommonParameters</span></span>
<span data-ttu-id="a4dbe-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4dbe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dbe-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dbe-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4dbe-133">INPUTS</span></span>

### <span data-ttu-id="a4dbe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dbe-134">System.String</span></span>

## <span data-ttu-id="a4dbe-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4dbe-135">OUTPUTS</span></span>

### <span data-ttu-id="a4dbe-136">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="a4dbe-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="a4dbe-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4dbe-137">NOTES</span></span>

## <span data-ttu-id="a4dbe-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4dbe-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4dbe-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dbe-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a4dbe-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dbe-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a4dbe-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dbe-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a4dbe-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a4dbe-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
