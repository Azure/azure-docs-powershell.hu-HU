---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012322"
---
# <span data-ttu-id="78dd2-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="78dd2-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="78dd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="78dd2-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="78dd2-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="78dd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78dd2-104">SYNTAX</span></span>

### <span data-ttu-id="78dd2-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78dd2-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78dd2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78dd2-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78dd2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78dd2-107">DESCRIPTION</span></span>
<span data-ttu-id="78dd2-108">A **Remove-AzSqlServerAudit** parancsmag eltávolítja az Azure SQL Server-kiszolgálók naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="78dd2-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="78dd2-109">Adja meg a kiszolgáló azonosítóját a *ResourceGroupName* és a *kiszolgálónév* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="78dd2-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="78dd2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="78dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="78dd2-111">1. példa: az Azure SQL Server naplózási beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="78dd2-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="78dd2-112">2. példa: az Azure SQL Server-kiszolgálók naplózási beállításainak eltávolítása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="78dd2-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="78dd2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78dd2-113">PARAMETERS</span></span>

### <span data-ttu-id="78dd2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78dd2-114">-AsJob</span></span>
<span data-ttu-id="78dd2-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="78dd2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78dd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78dd2-116">-DefaultProfile</span></span>
<span data-ttu-id="78dd2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78dd2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78dd2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78dd2-118">-ResourceGroupName</span></span>
<span data-ttu-id="78dd2-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78dd2-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78dd2-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="78dd2-120">-ServerName</span></span>
<span data-ttu-id="78dd2-121">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="78dd2-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78dd2-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="78dd2-122">-ServerObject</span></span>
<span data-ttu-id="78dd2-123">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="78dd2-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78dd2-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78dd2-124">-Confirm</span></span>
<span data-ttu-id="78dd2-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78dd2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78dd2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78dd2-126">-WhatIf</span></span>
<span data-ttu-id="78dd2-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78dd2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78dd2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78dd2-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78dd2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78dd2-129">CommonParameters</span></span>
<span data-ttu-id="78dd2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78dd2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78dd2-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78dd2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78dd2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78dd2-132">INPUTS</span></span>

### <span data-ttu-id="78dd2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="78dd2-133">System.String</span></span>

### <span data-ttu-id="78dd2-134">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="78dd2-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="78dd2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78dd2-135">OUTPUTS</span></span>

### <span data-ttu-id="78dd2-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78dd2-136">System.Boolean</span></span>

## <span data-ttu-id="78dd2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78dd2-137">NOTES</span></span>

## <span data-ttu-id="78dd2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78dd2-138">RELATED LINKS</span></span>
