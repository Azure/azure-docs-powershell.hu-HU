---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c583de368f549fdcd2916e7002829fc206350fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492714"
---
# <span data-ttu-id="77dd3-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="77dd3-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="77dd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="77dd3-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77dd3-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77dd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77dd3-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77dd3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77dd3-105">DESCRIPTION</span></span>
<span data-ttu-id="77dd3-106">A **New-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag létrehoz egy SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="77dd3-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="77dd3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77dd3-107">EXAMPLES</span></span>

## <span data-ttu-id="77dd3-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77dd3-108">PARAMETERS</span></span>

### <span data-ttu-id="77dd3-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77dd3-109">-AsJob</span></span>
<span data-ttu-id="77dd3-110">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="77dd3-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77dd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dd3-111">-DefaultProfile</span></span>
<span data-ttu-id="77dd3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77dd3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77dd3-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="77dd3-113">-FailoverPolicy</span></span>
<span data-ttu-id="77dd3-114">A feladatátvételi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="77dd3-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dd3-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="77dd3-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="77dd3-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="77dd3-117">-PartnerServerName</span></span>
<span data-ttu-id="77dd3-118">A partner kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="77dd3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dd3-119">-ResourceGroupName</span></span>
<span data-ttu-id="77dd3-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="77dd3-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="77dd3-121">-ServerName</span></span>
<span data-ttu-id="77dd3-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="77dd3-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="77dd3-123">-VirtualEndpointName</span></span>
<span data-ttu-id="77dd3-124">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77dd3-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="77dd3-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77dd3-125">-Confirm</span></span>
<span data-ttu-id="77dd3-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77dd3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77dd3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dd3-127">-WhatIf</span></span>
<span data-ttu-id="77dd3-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77dd3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dd3-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77dd3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77dd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dd3-130">CommonParameters</span></span>
<span data-ttu-id="77dd3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77dd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dd3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dd3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77dd3-133">INPUTS</span></span>

### <span data-ttu-id="77dd3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="77dd3-134">System.String</span></span>

## <span data-ttu-id="77dd3-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77dd3-135">OUTPUTS</span></span>

### <span data-ttu-id="77dd3-136">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="77dd3-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="77dd3-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77dd3-137">NOTES</span></span>

## <span data-ttu-id="77dd3-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77dd3-138">RELATED LINKS</span></span>

[<span data-ttu-id="77dd3-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="77dd3-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="77dd3-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="77dd3-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="77dd3-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="77dd3-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="77dd3-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="77dd3-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
