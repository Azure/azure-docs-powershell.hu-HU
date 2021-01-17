---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467141"
---
# <span data-ttu-id="8066a-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8066a-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="8066a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8066a-102">SYNOPSIS</span></span>
<span data-ttu-id="8066a-103">Adatbázis-kiszolgálói rendszer helyreállítási konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8066a-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="8066a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8066a-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8066a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8066a-105">DESCRIPTION</span></span>
<span data-ttu-id="8066a-106">A **New-AzSqlServerDisasterRecoveryConfiguration parancsmag** létrehoz egy SQL-adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="8066a-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8066a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8066a-107">EXAMPLES</span></span>

## <span data-ttu-id="8066a-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8066a-108">PARAMETERS</span></span>

### <span data-ttu-id="8066a-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8066a-109">-AsJob</span></span>
<span data-ttu-id="8066a-110">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8066a-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8066a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8066a-111">-DefaultProfile</span></span>
<span data-ttu-id="8066a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8066a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8066a-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8066a-113">-FailoverPolicy</span></span>
<span data-ttu-id="8066a-114">Megadja a feladatátvételi házirendet.</span><span class="sxs-lookup"><span data-stu-id="8066a-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="8066a-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8066a-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8066a-116">A partnererőforrás-csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8066a-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="8066a-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="8066a-117">-PartnerServerName</span></span>
<span data-ttu-id="8066a-118">A partnerkiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8066a-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="8066a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8066a-119">-ResourceGroupName</span></span>
<span data-ttu-id="8066a-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8066a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8066a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8066a-121">-ServerName</span></span>
<span data-ttu-id="8066a-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8066a-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8066a-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="8066a-123">-VirtualEndpointName</span></span>
<span data-ttu-id="8066a-124">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8066a-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="8066a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8066a-125">-Confirm</span></span>
<span data-ttu-id="8066a-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8066a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8066a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8066a-127">-WhatIf</span></span>
<span data-ttu-id="8066a-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8066a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8066a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8066a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8066a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8066a-130">CommonParameters</span></span>
<span data-ttu-id="8066a-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8066a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8066a-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8066a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8066a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8066a-133">INPUTS</span></span>

### <span data-ttu-id="8066a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8066a-134">System.String</span></span>

## <span data-ttu-id="8066a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8066a-135">OUTPUTS</span></span>

### <span data-ttu-id="8066a-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="8066a-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="8066a-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8066a-137">NOTES</span></span>

## <span data-ttu-id="8066a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8066a-138">RELATED LINKS</span></span>

[<span data-ttu-id="8066a-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8066a-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8066a-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8066a-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8066a-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8066a-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8066a-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8066a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
