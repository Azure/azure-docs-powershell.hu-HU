---
Module Name: Az.StackHCI
Module Guid: 8ff047e4-15bb-4b53-a728-75641c49958b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.StackHCI
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
ms.openlocfilehash: 5666172da80ec27131931aecc353c9315266b185
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143899"
---
# <span data-ttu-id="a5956-101">Az.StackHCI modul</span><span class="sxs-lookup"><span data-stu-id="a5956-101">Az.StackHCI Module</span></span>
## <span data-ttu-id="a5956-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5956-102">Description</span></span>
<span data-ttu-id="a5956-103">Microsoft Azure PowerShell: Azure Stack HCI regisztrációs parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5956-103">Microsoft Azure PowerShell: Azure Stack HCI registration cmdlets</span></span>

## <span data-ttu-id="a5956-104">Az.StackHCI parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a5956-104">Az.StackHCI Cmdlets</span></span>
### [<span data-ttu-id="a5956-105">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="a5956-105">Register-AzStackHCI</span></span>](Register-AzStackHCI.md)
<span data-ttu-id="a5956-106">Register-AzStackHCI létrehoz egy Microsoft.AzureStackHCI felhőbeli erőforrást, amely a helyi fürtnek megfelelő, és regisztrálja a helyi fürtöt az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="a5956-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

### [<span data-ttu-id="a5956-107">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="a5956-107">Test-AzStackHCIConnection</span></span>](Test-AzStackHCIConnection.md)
<span data-ttu-id="a5956-108">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="a5956-108">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

### [<span data-ttu-id="a5956-109">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="a5956-109">Unregister-AzStackHCI</span></span>](Unregister-AzStackHCI.md)
<span data-ttu-id="a5956-110">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="a5956-110">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="a5956-111">A fürtön elérhető regisztrált információk a fürt regisztrációjának a visszaszabadulnak, ha nem ad át paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a5956-111">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

