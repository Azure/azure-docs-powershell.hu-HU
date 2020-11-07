---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ac62ac0307422f0015fe578937a80a03e2a730d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668946"
---
# <span data-ttu-id="e0a97-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0a97-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e0a97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0a97-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a97-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="e0a97-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="e0a97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0a97-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0a97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0a97-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a97-106">A **Get-AzSqlServerDisasterRecoveryConfiguration** parancsmag SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="e0a97-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e0a97-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0a97-107">EXAMPLES</span></span>

## <span data-ttu-id="e0a97-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0a97-108">PARAMETERS</span></span>

### <span data-ttu-id="e0a97-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a97-109">-DefaultProfile</span></span>
<span data-ttu-id="e0a97-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0a97-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0a97-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a97-111">-ResourceGroupName</span></span>
<span data-ttu-id="e0a97-112">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0a97-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e0a97-113">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e0a97-113">-ServerName</span></span>
<span data-ttu-id="e0a97-114">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0a97-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="e0a97-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e0a97-115">-VirtualEndpointName</span></span>
<span data-ttu-id="e0a97-116">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0a97-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e0a97-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0a97-117">-Confirm</span></span>
<span data-ttu-id="e0a97-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0a97-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a97-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a97-119">-WhatIf</span></span>
<span data-ttu-id="e0a97-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0a97-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0a97-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0a97-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a97-122">CommonParameters</span></span>
<span data-ttu-id="e0a97-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0a97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a97-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0a97-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a97-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0a97-125">INPUTS</span></span>

### <span data-ttu-id="e0a97-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e0a97-126">System.String</span></span>

## <span data-ttu-id="e0a97-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0a97-127">OUTPUTS</span></span>

### <span data-ttu-id="e0a97-128">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="e0a97-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="e0a97-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0a97-129">NOTES</span></span>

## <span data-ttu-id="e0a97-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0a97-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0a97-131">Új – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0a97-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0a97-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0a97-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0a97-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0a97-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0a97-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e0a97-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

