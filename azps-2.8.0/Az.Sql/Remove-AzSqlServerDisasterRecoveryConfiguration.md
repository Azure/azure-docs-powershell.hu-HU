---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e70aafbf938fb8e10c36be41e0003f5310d082db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839374"
---
# <span data-ttu-id="d2724-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2724-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d2724-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2724-102">SYNOPSIS</span></span>
<span data-ttu-id="d2724-103">Eltávolítja az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d2724-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d2724-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2724-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2724-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2724-105">DESCRIPTION</span></span>
<span data-ttu-id="d2724-106">A **Remove-AzSqlServerDisasterRecoveryConfiguration** parancsmag ELTÁVOLÍTJA az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="d2724-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d2724-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2724-107">EXAMPLES</span></span>

## <span data-ttu-id="d2724-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2724-108">PARAMETERS</span></span>

### <span data-ttu-id="d2724-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2724-109">-DefaultProfile</span></span>
<span data-ttu-id="d2724-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2724-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2724-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d2724-111">-Force</span></span>
<span data-ttu-id="d2724-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d2724-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2724-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2724-113">-ResourceGroupName</span></span>
<span data-ttu-id="d2724-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2724-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2724-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d2724-115">-ServerName</span></span>
<span data-ttu-id="d2724-116">Egy SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2724-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="d2724-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d2724-117">-VirtualEndpointName</span></span>
<span data-ttu-id="d2724-118">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2724-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2724-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2724-119">-Confirm</span></span>
<span data-ttu-id="d2724-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2724-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2724-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2724-121">-WhatIf</span></span>
<span data-ttu-id="d2724-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2724-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2724-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2724-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2724-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2724-124">CommonParameters</span></span>
<span data-ttu-id="d2724-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2724-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2724-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2724-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2724-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2724-127">INPUTS</span></span>

### <span data-ttu-id="d2724-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2724-128">System.String</span></span>

## <span data-ttu-id="d2724-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2724-129">OUTPUTS</span></span>

### <span data-ttu-id="d2724-130">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="d2724-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="d2724-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2724-131">NOTES</span></span>

## <span data-ttu-id="d2724-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2724-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2724-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2724-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d2724-134">Új – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2724-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d2724-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2724-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d2724-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d2724-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
