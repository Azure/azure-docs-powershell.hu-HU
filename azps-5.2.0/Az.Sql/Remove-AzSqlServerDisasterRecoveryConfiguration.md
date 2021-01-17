---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322724"
---
# <span data-ttu-id="6afef-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afef-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="6afef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afef-102">SYNOPSIS</span></span>
<span data-ttu-id="6afef-103">Eltávolítja az SQL-adatbázis-kiszolgáló rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6afef-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6afef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6afef-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6afef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6afef-105">DESCRIPTION</span></span>
<span data-ttu-id="6afef-106">A **Remove-AzSqlServerDisasterRecoveryConfiguration parancsmag** eltávolítja az SQL-adatbázis-kiszolgálói rendszer helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6afef-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6afef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6afef-107">EXAMPLES</span></span>

## <span data-ttu-id="6afef-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6afef-108">PARAMETERS</span></span>

### <span data-ttu-id="6afef-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afef-109">-DefaultProfile</span></span>
<span data-ttu-id="6afef-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6afef-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6afef-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6afef-111">-Force</span></span>
<span data-ttu-id="6afef-112">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="6afef-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6afef-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6afef-113">-ResourceGroupName</span></span>
<span data-ttu-id="6afef-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afef-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6afef-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6afef-115">-ServerName</span></span>
<span data-ttu-id="6afef-116">Egy SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afef-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="6afef-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="6afef-117">-VirtualEndpointName</span></span>
<span data-ttu-id="6afef-118">Egy virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afef-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="6afef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6afef-119">-Confirm</span></span>
<span data-ttu-id="6afef-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6afef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6afef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6afef-121">-WhatIf</span></span>
<span data-ttu-id="6afef-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6afef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6afef-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6afef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6afef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afef-124">CommonParameters</span></span>
<span data-ttu-id="6afef-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afef-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6afef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afef-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6afef-127">INPUTS</span></span>

### <span data-ttu-id="6afef-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6afef-128">System.String</span></span>

## <span data-ttu-id="6afef-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6afef-129">OUTPUTS</span></span>

### <span data-ttu-id="6afef-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="6afef-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="6afef-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6afef-131">NOTES</span></span>

## <span data-ttu-id="6afef-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6afef-132">RELATED LINKS</span></span>

[<span data-ttu-id="6afef-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afef-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6afef-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afef-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6afef-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afef-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6afef-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6afef-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
