---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207886"
---
# <span data-ttu-id="dcafa-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcafa-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="dcafa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcafa-102">SYNOPSIS</span></span>
<span data-ttu-id="dcafa-103">Eltávolítja az SQL-adatbázis-kiszolgáló rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="dcafa-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="dcafa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcafa-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcafa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcafa-105">DESCRIPTION</span></span>
<span data-ttu-id="dcafa-106">A **Remove-AzSqlServerDisasterRecoveryConfiguration parancsmag** eltávolítja az SQL-adatbázis-kiszolgáló rendszer-helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="dcafa-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="dcafa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcafa-107">EXAMPLES</span></span>

## <span data-ttu-id="dcafa-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcafa-108">PARAMETERS</span></span>

### <span data-ttu-id="dcafa-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcafa-109">-DefaultProfile</span></span>
<span data-ttu-id="dcafa-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dcafa-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcafa-111">-Force</span><span class="sxs-lookup"><span data-stu-id="dcafa-111">-Force</span></span>
<span data-ttu-id="dcafa-112">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="dcafa-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcafa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcafa-113">-ResourceGroupName</span></span>
<span data-ttu-id="dcafa-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcafa-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dcafa-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcafa-115">-ServerName</span></span>
<span data-ttu-id="dcafa-116">Egy SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcafa-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="dcafa-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="dcafa-117">-VirtualEndpointName</span></span>
<span data-ttu-id="dcafa-118">Egy virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcafa-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="dcafa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcafa-119">-Confirm</span></span>
<span data-ttu-id="dcafa-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcafa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcafa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcafa-121">-WhatIf</span></span>
<span data-ttu-id="dcafa-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcafa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcafa-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcafa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcafa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcafa-124">CommonParameters</span></span>
<span data-ttu-id="dcafa-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcafa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcafa-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcafa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcafa-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcafa-127">INPUTS</span></span>

### <span data-ttu-id="dcafa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="dcafa-128">System.String</span></span>

## <span data-ttu-id="dcafa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcafa-129">OUTPUTS</span></span>

### <span data-ttu-id="dcafa-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="dcafa-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="dcafa-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcafa-131">NOTES</span></span>

## <span data-ttu-id="dcafa-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcafa-132">RELATED LINKS</span></span>

[<span data-ttu-id="dcafa-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcafa-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dcafa-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcafa-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dcafa-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcafa-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dcafa-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dcafa-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
