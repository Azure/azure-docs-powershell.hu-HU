---
Module Name: Az.StackHCI
Module Guid: 8ff047e4-15bb-4b53-a728-75641c49958b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.StackHCI
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
ms.openlocfilehash: e11c0afba08bb7127551826427b5298e83245d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349961"
---
# <span data-ttu-id="86f3a-101">Az.StackHCI modul</span><span class="sxs-lookup"><span data-stu-id="86f3a-101">Az.StackHCI Module</span></span>
## <span data-ttu-id="86f3a-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="86f3a-102">Description</span></span>
<span data-ttu-id="86f3a-103">Microsoft Azure PowerShell: StackHCI parancsmagok</span><span class="sxs-lookup"><span data-stu-id="86f3a-103">Microsoft Azure PowerShell: StackHCI cmdlets</span></span>

## <span data-ttu-id="86f3a-104">Az.StackHCI parancsmagok</span><span class="sxs-lookup"><span data-stu-id="86f3a-104">Az.StackHCI Cmdlets</span></span>
### [<span data-ttu-id="86f3a-105">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="86f3a-105">Register-AzStackHCI</span></span>](Register-AzStackHCI.md)
<span data-ttu-id="86f3a-106">Register-AzStackHCI létrehoz egy Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtnek megfelelő, és regisztrálja a helyi fürtöt az Azure-zal.</span><span class="sxs-lookup"><span data-stu-id="86f3a-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

### [<span data-ttu-id="86f3a-107">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="86f3a-107">Test-AzStackHCIConnection</span></span>](Test-AzStackHCIConnection.md)
<span data-ttu-id="86f3a-108">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="86f3a-108">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

### [<span data-ttu-id="86f3a-109">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="86f3a-109">Unregister-AzStackHCI</span></span>](Unregister-AzStackHCI.md)
<span data-ttu-id="86f3a-110">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="86f3a-110">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="86f3a-111">Ha nem ad át paramétereket, a fürtön elérhető regisztrált információk a fürt regisztrációjának a nevére használatosak.</span><span class="sxs-lookup"><span data-stu-id="86f3a-111">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

