---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680304"
---
# <span data-ttu-id="f734d-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f734d-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f734d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f734d-102">SYNOPSIS</span></span>
<span data-ttu-id="f734d-103">Eltávolítja az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f734d-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f734d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f734d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f734d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f734d-105">DESCRIPTION</span></span>
<span data-ttu-id="f734d-106">A **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag ELTÁVOLÍTJA az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f734d-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f734d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f734d-107">EXAMPLES</span></span>

## <span data-ttu-id="f734d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f734d-108">PARAMETERS</span></span>

### <span data-ttu-id="f734d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f734d-109">-DefaultProfile</span></span>
<span data-ttu-id="f734d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f734d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f734d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f734d-111">-Force</span></span>
<span data-ttu-id="f734d-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f734d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f734d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f734d-113">-ResourceGroupName</span></span>
<span data-ttu-id="f734d-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f734d-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f734d-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f734d-115">-ServerName</span></span>
<span data-ttu-id="f734d-116">Egy SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f734d-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="f734d-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f734d-117">-VirtualEndpointName</span></span>
<span data-ttu-id="f734d-118">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f734d-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="f734d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f734d-119">-Confirm</span></span>
<span data-ttu-id="f734d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f734d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f734d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f734d-121">-WhatIf</span></span>
<span data-ttu-id="f734d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f734d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f734d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f734d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f734d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f734d-124">CommonParameters</span></span>
<span data-ttu-id="f734d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f734d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f734d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f734d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f734d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f734d-127">INPUTS</span></span>

### <span data-ttu-id="f734d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f734d-128">System.String</span></span>

## <span data-ttu-id="f734d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f734d-129">OUTPUTS</span></span>

### <span data-ttu-id="f734d-130">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="f734d-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="f734d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f734d-131">NOTES</span></span>

## <span data-ttu-id="f734d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f734d-132">RELATED LINKS</span></span>

[<span data-ttu-id="f734d-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f734d-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f734d-134">Új – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f734d-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f734d-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f734d-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f734d-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f734d-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
