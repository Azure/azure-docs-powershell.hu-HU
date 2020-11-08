---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010578"
---
# <span data-ttu-id="f7aa8-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="f7aa8-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="f7aa8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aa8-103">Az adatbázis-kiszolgálói rendszer-helyreállítási konfiguráció tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="f7aa8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7aa8-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7aa8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7aa8-106">A **Get-AzSqlServerDisasterRecoveryConfigurationActivity** PARANCSMAG az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációjának tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f7aa8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f7aa8-107">EXAMPLES</span></span>

## <span data-ttu-id="f7aa8-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7aa8-108">PARAMETERS</span></span>

### <span data-ttu-id="f7aa8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7aa8-109">-DefaultProfile</span></span>
<span data-ttu-id="f7aa8-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7aa8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7aa8-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f7aa8-111">-OperationId</span></span>
<span data-ttu-id="f7aa8-112">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7aa8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7aa8-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7aa8-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7aa8-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f7aa8-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="f7aa8-116">A kiszolgálói rendszer-helyreállítási konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7aa8-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f7aa8-117">-ServerName</span></span>
<span data-ttu-id="f7aa8-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f7aa8-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7aa8-119">-Confirm</span></span>
<span data-ttu-id="f7aa8-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7aa8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7aa8-121">-WhatIf</span></span>
<span data-ttu-id="f7aa8-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7aa8-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7aa8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aa8-124">CommonParameters</span></span>
<span data-ttu-id="f7aa8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7aa8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aa8-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7aa8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aa8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7aa8-127">INPUTS</span></span>

### <span data-ttu-id="f7aa8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f7aa8-128">System.String</span></span>

### <span data-ttu-id="f7aa8-129">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7aa8-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7aa8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7aa8-130">OUTPUTS</span></span>

### <span data-ttu-id="f7aa8-131">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="f7aa8-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="f7aa8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7aa8-132">NOTES</span></span>

## <span data-ttu-id="f7aa8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7aa8-133">RELATED LINKS</span></span>

[<span data-ttu-id="f7aa8-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f7aa8-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
