---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343950"
---
# <span data-ttu-id="44bf9-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="44bf9-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="44bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="44bf9-103">Megszakítja a rugalmas készlet aszinkron frissítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="44bf9-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="44bf9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44bf9-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44bf9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="44bf9-106">A **Stop-AzSqlElasticPoolActivity** parancsmag megszakítja a rugalmas készlet aszinkron frissítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="44bf9-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="44bf9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="44bf9-108">1. példa: Aszinkron frissítési művelet megszakítása rugalmas készleten</span><span class="sxs-lookup"><span data-stu-id="44bf9-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="44bf9-109">Ez a parancs megszakítja a rugalmas készlet aszinkron frissítését.</span><span class="sxs-lookup"><span data-stu-id="44bf9-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="44bf9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="44bf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bf9-111">-DefaultProfile</span></span>
<span data-ttu-id="44bf9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44bf9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44bf9-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="44bf9-113">-ElasticPoolName</span></span>
<span data-ttu-id="44bf9-114">Az Azure SQL Rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="44bf9-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="44bf9-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="44bf9-115">-OperationId</span></span>
<span data-ttu-id="44bf9-116">A visszakeresni szükséges művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44bf9-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="44bf9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44bf9-117">-PassThru</span></span>
<span data-ttu-id="44bf9-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="44bf9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="44bf9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44bf9-119">-ResourceGroupName</span></span>
<span data-ttu-id="44bf9-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44bf9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="44bf9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="44bf9-121">-ServerName</span></span>
<span data-ttu-id="44bf9-122">Annak az Azure SQL Servernek a neve, amelynél a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="44bf9-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="44bf9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44bf9-123">-Confirm</span></span>
<span data-ttu-id="44bf9-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44bf9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44bf9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44bf9-125">-WhatIf</span></span>
<span data-ttu-id="44bf9-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44bf9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44bf9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44bf9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44bf9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bf9-128">CommonParameters</span></span>
<span data-ttu-id="44bf9-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44bf9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bf9-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44bf9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bf9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44bf9-131">INPUTS</span></span>

### <span data-ttu-id="44bf9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="44bf9-132">System.String</span></span>

### <span data-ttu-id="44bf9-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44bf9-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="44bf9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44bf9-134">OUTPUTS</span></span>

### <span data-ttu-id="44bf9-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="44bf9-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="44bf9-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44bf9-136">NOTES</span></span>

## <span data-ttu-id="44bf9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44bf9-137">RELATED LINKS</span></span>
