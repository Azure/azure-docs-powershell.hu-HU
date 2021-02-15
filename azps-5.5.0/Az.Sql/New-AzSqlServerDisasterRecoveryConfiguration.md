---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145611"
---
# <span data-ttu-id="32357-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32357-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="32357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32357-102">SYNOPSIS</span></span>
<span data-ttu-id="32357-103">Adatbázis-kiszolgálói rendszer helyreállítási konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="32357-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="32357-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32357-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32357-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32357-105">DESCRIPTION</span></span>
<span data-ttu-id="32357-106">A **New-AzSqlServerDisasterRecoveryConfiguration parancsmag** létrehoz egy SQL-adatbázis-kiszolgálói rendszer helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="32357-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="32357-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32357-107">EXAMPLES</span></span>

## <span data-ttu-id="32357-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32357-108">PARAMETERS</span></span>

### <span data-ttu-id="32357-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32357-109">-AsJob</span></span>
<span data-ttu-id="32357-110">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="32357-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32357-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32357-111">-DefaultProfile</span></span>
<span data-ttu-id="32357-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32357-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32357-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="32357-113">-FailoverPolicy</span></span>
<span data-ttu-id="32357-114">Megadja a feladatátvételi házirendet.</span><span class="sxs-lookup"><span data-stu-id="32357-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="32357-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32357-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="32357-116">A partnererőforrás-csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32357-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="32357-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="32357-117">-PartnerServerName</span></span>
<span data-ttu-id="32357-118">A partnerkiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32357-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="32357-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32357-119">-ResourceGroupName</span></span>
<span data-ttu-id="32357-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32357-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="32357-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32357-121">-ServerName</span></span>
<span data-ttu-id="32357-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32357-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="32357-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="32357-123">-VirtualEndpointName</span></span>
<span data-ttu-id="32357-124">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32357-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="32357-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32357-125">-Confirm</span></span>
<span data-ttu-id="32357-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="32357-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32357-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32357-127">-WhatIf</span></span>
<span data-ttu-id="32357-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="32357-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32357-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32357-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32357-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32357-130">CommonParameters</span></span>
<span data-ttu-id="32357-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32357-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32357-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32357-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32357-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32357-133">INPUTS</span></span>

### <span data-ttu-id="32357-134">System.String</span><span class="sxs-lookup"><span data-stu-id="32357-134">System.String</span></span>

## <span data-ttu-id="32357-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32357-135">OUTPUTS</span></span>

### <span data-ttu-id="32357-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="32357-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="32357-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32357-137">NOTES</span></span>

## <span data-ttu-id="32357-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32357-138">RELATED LINKS</span></span>

[<span data-ttu-id="32357-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32357-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32357-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32357-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32357-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32357-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32357-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="32357-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
