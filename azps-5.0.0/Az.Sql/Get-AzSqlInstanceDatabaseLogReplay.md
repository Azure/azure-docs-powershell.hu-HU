---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195079"
---
# <span data-ttu-id="9619f-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9619f-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9619f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9619f-102">SYNOPSIS</span></span>
<span data-ttu-id="9619f-103">A log Replay szolgáltatás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9619f-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="9619f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9619f-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9619f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9619f-105">DESCRIPTION</span></span>
<span data-ttu-id="9619f-106">A **Get-AzSqlInstanceDatabaseLogReplay** parancsmag a naplózási Visszajátszási szolgáltatás állapotát a megadott adatbázisban kapja.</span><span class="sxs-lookup"><span data-stu-id="9619f-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="9619f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9619f-107">EXAMPLES</span></span>

### <span data-ttu-id="9619f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9619f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="9619f-109">Ez a parancs naplózza a Visszajátszási szolgáltatás állapotát az adott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="9619f-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="9619f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9619f-110">PARAMETERS</span></span>

### <span data-ttu-id="9619f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9619f-111">-DefaultProfile</span></span>
<span data-ttu-id="9619f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9619f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9619f-113">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="9619f-113">-InstanceName</span></span>
<span data-ttu-id="9619f-114">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="9619f-114">The name of the instance.</span></span>

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

### <span data-ttu-id="9619f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9619f-115">-Name</span></span>
<span data-ttu-id="9619f-116">A lekérdezni kívánt példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9619f-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="9619f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9619f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9619f-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9619f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9619f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9619f-119">CommonParameters</span></span>
<span data-ttu-id="9619f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9619f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9619f-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9619f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9619f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9619f-122">INPUTS</span></span>

### <span data-ttu-id="9619f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9619f-123">System.String</span></span>

## <span data-ttu-id="9619f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9619f-124">OUTPUTS</span></span>

### <span data-ttu-id="9619f-125">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="9619f-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="9619f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9619f-126">NOTES</span></span>

## <span data-ttu-id="9619f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9619f-127">RELATED LINKS</span></span>