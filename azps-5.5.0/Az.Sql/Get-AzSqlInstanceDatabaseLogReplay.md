---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165795"
---
# <span data-ttu-id="c56e0-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="c56e0-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="c56e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c56e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c56e0-103">A Napló visszajátszása szolgáltatás állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="c56e0-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="c56e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c56e0-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c56e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c56e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c56e0-106">A **Get-AzSqlInstanceDatabaseLogReplay** parancsmag a Log Replay szolgáltatás állapotát kapja meg a megadott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="c56e0-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="c56e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c56e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c56e0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c56e0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="c56e0-109">Ez a parancs a napló visszajátszási szolgáltatás állapotát fogja kapni az adott adatbázison.</span><span class="sxs-lookup"><span data-stu-id="c56e0-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="c56e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c56e0-110">PARAMETERS</span></span>

### <span data-ttu-id="c56e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56e0-111">-DefaultProfile</span></span>
<span data-ttu-id="c56e0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c56e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56e0-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c56e0-113">-InstanceName</span></span>
<span data-ttu-id="c56e0-114">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="c56e0-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56e0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c56e0-115">-Name</span></span>
<span data-ttu-id="c56e0-116">A visszakeresni megfelelő példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c56e0-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="c56e0-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c56e0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c56e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56e0-119">CommonParameters</span></span>
<span data-ttu-id="c56e0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56e0-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c56e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56e0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c56e0-122">INPUTS</span></span>

### <span data-ttu-id="c56e0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c56e0-123">System.String</span></span>

## <span data-ttu-id="c56e0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c56e0-124">OUTPUTS</span></span>

### <span data-ttu-id="c56e0-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="c56e0-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="c56e0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c56e0-126">NOTES</span></span>

## <span data-ttu-id="c56e0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c56e0-127">RELATED LINKS</span></span>
