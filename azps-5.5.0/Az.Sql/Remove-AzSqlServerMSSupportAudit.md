---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164875"
---
# <span data-ttu-id="dcee7-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="dcee7-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="dcee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcee7-102">SYNOPSIS</span></span>
<span data-ttu-id="dcee7-103">Eltávolítja a Microsoft támogatási műveleteinek naplózási beállításait egy Azure SQL-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="dcee7-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="dcee7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcee7-104">SYNTAX</span></span>

### <span data-ttu-id="dcee7-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dcee7-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcee7-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcee7-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcee7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcee7-107">DESCRIPTION</span></span>
<span data-ttu-id="dcee7-108">A **Remove-AzSqlServerMSSupportAudit** parancsmag eltávolítja egy Azure SQL-kiszolgáló Microsoft támogatási műveleteinek naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="dcee7-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="dcee7-109">A parancsmagot a *ResourceGroupName* és *a ServerName* paraméterrel használhatja a kiszolgáló azonosításához.</span><span class="sxs-lookup"><span data-stu-id="dcee7-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="dcee7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcee7-110">EXAMPLES</span></span>

### <span data-ttu-id="dcee7-111">1. példa: A Microsoft támogatási műveleteinek naplózási beállításainak eltávolítása egy Azure SQL-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="dcee7-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="dcee7-112">2. példa: Az Azure SQL-kiszolgáló Microsoft által támogatott naplózási beállításainak eltávolítása folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="dcee7-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="dcee7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcee7-113">PARAMETERS</span></span>

### <span data-ttu-id="dcee7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcee7-114">-AsJob</span></span>
<span data-ttu-id="dcee7-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dcee7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcee7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcee7-116">-DefaultProfile</span></span>
<span data-ttu-id="dcee7-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcee7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcee7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcee7-118">-ResourceGroupName</span></span>
<span data-ttu-id="dcee7-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dcee7-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcee7-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcee7-120">-ServerName</span></span>
<span data-ttu-id="dcee7-121">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dcee7-121">SQL server name.</span></span>

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

### <span data-ttu-id="dcee7-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="dcee7-122">-ServerObject</span></span>
<span data-ttu-id="dcee7-123">A naplózási házirend kezeléséhez megfelelő kiszolgálóobjektum.</span><span class="sxs-lookup"><span data-stu-id="dcee7-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="dcee7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcee7-124">-Confirm</span></span>
<span data-ttu-id="dcee7-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcee7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcee7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcee7-126">-WhatIf</span></span>
<span data-ttu-id="dcee7-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcee7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcee7-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcee7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcee7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcee7-129">CommonParameters</span></span>
<span data-ttu-id="dcee7-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcee7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcee7-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcee7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcee7-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcee7-132">INPUTS</span></span>

### <span data-ttu-id="dcee7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dcee7-133">System.String</span></span>

### <span data-ttu-id="dcee7-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="dcee7-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="dcee7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcee7-135">OUTPUTS</span></span>

### <span data-ttu-id="dcee7-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dcee7-136">System.Boolean</span></span>

## <span data-ttu-id="dcee7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcee7-137">NOTES</span></span>

## <span data-ttu-id="dcee7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcee7-138">RELATED LINKS</span></span>
