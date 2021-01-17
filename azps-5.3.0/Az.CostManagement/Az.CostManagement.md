---
Module Name: Az.CostManagement
Module Guid: 4cd9af10-559e-4fb9-8dcd-d3e8eb9e03b7
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
ms.openlocfilehash: 0bfac4d12c15bef8b16e9ba239423b1443a9f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477326"
---
# <span data-ttu-id="21f0a-101">Az.CostManagement modul</span><span class="sxs-lookup"><span data-stu-id="21f0a-101">Az.CostManagement Module</span></span>
## <span data-ttu-id="21f0a-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="21f0a-102">Description</span></span>
<span data-ttu-id="21f0a-103">Microsoft Azure PowerShell: Költség parancsmagok</span><span class="sxs-lookup"><span data-stu-id="21f0a-103">Microsoft Azure PowerShell: Cost cmdlets</span></span>

## <span data-ttu-id="21f0a-104">Az.CostManagement parancsmagok</span><span class="sxs-lookup"><span data-stu-id="21f0a-104">Az.CostManagement Cmdlets</span></span>
### [<span data-ttu-id="21f0a-105">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="21f0a-105">Get-AzCostManagementExport</span></span>](Get-AzCostManagementExport.md)
<span data-ttu-id="21f0a-106">A megadott hatókör exportálási hatókörének exportálási nevével történő lekért művelet.</span><span class="sxs-lookup"><span data-stu-id="21f0a-106">The operation to get the export for the defined scope by export name.</span></span>

### [<span data-ttu-id="21f0a-107">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="21f0a-107">Get-AzCostManagementExportExecutionHistory</span></span>](Get-AzCostManagementExportExecutionHistory.md)
<span data-ttu-id="21f0a-108">Az exportálási előzmények lekérte a megadott hatókörű és exportálási névhez tartozó műveletet.</span><span class="sxs-lookup"><span data-stu-id="21f0a-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

### [<span data-ttu-id="21f0a-109">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="21f0a-109">Invoke-AzCostManagementExecuteExport</span></span>](Invoke-AzCostManagementExecuteExport.md)
<span data-ttu-id="21f0a-110">Az exportálás végrehajtásához szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="21f0a-110">The operation to execute an export.</span></span>

### [<span data-ttu-id="21f0a-111">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="21f0a-111">Invoke-AzCostManagementQuery</span></span>](Invoke-AzCostManagementQuery.md)
<span data-ttu-id="21f0a-112">Lekérdezi a hatókör használati adatait.</span><span class="sxs-lookup"><span data-stu-id="21f0a-112">Query the usage data for scope defined.</span></span>

### [<span data-ttu-id="21f0a-113">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="21f0a-113">New-AzCostManagementExport</span></span>](New-AzCostManagementExport.md)
<span data-ttu-id="21f0a-114">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="21f0a-114">The operation to create or update a export.</span></span>
<span data-ttu-id="21f0a-115">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="21f0a-115">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="21f0a-116">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="21f0a-116">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="21f0a-117">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="21f0a-117">Create operation does not require eTag.</span></span>

### [<span data-ttu-id="21f0a-118">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="21f0a-118">New-AzCostManagementQueryComparisonExpressionObject</span></span>](New-AzCostManagementQueryComparisonExpressionObject.md)
<span data-ttu-id="21f0a-119">Create a in-memory object for QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="21f0a-119">Create a in-memory object for QueryComparisonExpression</span></span>

### [<span data-ttu-id="21f0a-120">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="21f0a-120">New-AzCostManagementQueryFilterObject</span></span>](New-AzCostManagementQueryFilterObject.md)
<span data-ttu-id="21f0a-121">Memória-objektum létrehozása a QueryFilterhez</span><span class="sxs-lookup"><span data-stu-id="21f0a-121">Create a in-memory object for QueryFilter</span></span>

### [<span data-ttu-id="21f0a-122">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="21f0a-122">Remove-AzCostManagementExport</span></span>](Remove-AzCostManagementExport.md)
<span data-ttu-id="21f0a-123">Az exportálás törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="21f0a-123">The operation to delete a export.</span></span>

### [<span data-ttu-id="21f0a-124">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="21f0a-124">Update-AzCostManagementExport</span></span>](Update-AzCostManagementExport.md)
<span data-ttu-id="21f0a-125">Az exportálás létrehozására vagy frissítésére vonatkozó művelet.</span><span class="sxs-lookup"><span data-stu-id="21f0a-125">The operation to create or update a export.</span></span>
<span data-ttu-id="21f0a-126">A frissítési művelethez be kell állítani a legújabb eTag-et a kérelemben.</span><span class="sxs-lookup"><span data-stu-id="21f0a-126">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="21f0a-127">A get művelettel beszerezheti a legújabb eTag-et.</span><span class="sxs-lookup"><span data-stu-id="21f0a-127">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="21f0a-128">A létrehozási művelethez nincs szükség eTag gombra.</span><span class="sxs-lookup"><span data-stu-id="21f0a-128">Create operation does not require eTag.</span></span>

