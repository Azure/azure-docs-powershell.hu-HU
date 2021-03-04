---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: be2017c829a97196ad5cf2cef9d3dbd71144a325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940978"
---
# <span data-ttu-id="25cab-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="25cab-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="25cab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25cab-102">SYNOPSIS</span></span>
<span data-ttu-id="25cab-103">Eltávolítja egy Azure SQL-kiszolgáló naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="25cab-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="25cab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25cab-104">SYNTAX</span></span>

### <span data-ttu-id="25cab-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25cab-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cab-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cab-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25cab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25cab-107">DESCRIPTION</span></span>
<span data-ttu-id="25cab-108">A **Remove-AzSqlServerAudit** parancsmag eltávolítja egy Azure SQL-kiszolgáló naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="25cab-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="25cab-109">A *kiszolgáló azonosításához adja* meg a ResourceGroupName és *a ServerName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="25cab-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="25cab-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25cab-110">EXAMPLES</span></span>

### <span data-ttu-id="25cab-111">1. példa: Azure SQL-kiszolgáló naplózási beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="25cab-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="25cab-112">2. példa: Azure SQL-kiszolgáló naplózási beállításainak eltávolítása folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="25cab-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="25cab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25cab-113">PARAMETERS</span></span>

### <span data-ttu-id="25cab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25cab-114">-AsJob</span></span>
<span data-ttu-id="25cab-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="25cab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25cab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cab-116">-DefaultProfile</span></span>
<span data-ttu-id="25cab-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25cab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cab-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cab-118">-ResourceGroupName</span></span>
<span data-ttu-id="25cab-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25cab-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="25cab-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25cab-120">-ServerName</span></span>
<span data-ttu-id="25cab-121">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="25cab-121">SQL server name.</span></span>

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

### <span data-ttu-id="25cab-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="25cab-122">-ServerObject</span></span>
<span data-ttu-id="25cab-123">A naplózási házirend kezeléséhez megfelelő kiszolgálóobjektum.</span><span class="sxs-lookup"><span data-stu-id="25cab-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="25cab-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25cab-124">-Confirm</span></span>
<span data-ttu-id="25cab-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25cab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cab-126">-WhatIf</span></span>
<span data-ttu-id="25cab-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25cab-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25cab-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25cab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cab-129">CommonParameters</span></span>
<span data-ttu-id="25cab-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25cab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cab-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25cab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cab-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25cab-132">INPUTS</span></span>

### <span data-ttu-id="25cab-133">System.String</span><span class="sxs-lookup"><span data-stu-id="25cab-133">System.String</span></span>

### <span data-ttu-id="25cab-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="25cab-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="25cab-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25cab-135">OUTPUTS</span></span>

### <span data-ttu-id="25cab-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25cab-136">System.Boolean</span></span>

## <span data-ttu-id="25cab-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25cab-137">NOTES</span></span>

## <span data-ttu-id="25cab-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25cab-138">RELATED LINKS</span></span>
